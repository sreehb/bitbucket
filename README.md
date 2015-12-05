Ansible Role for BitBucket
==========================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-bitbucket.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-bitbucket)
 [![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-bitbucket.svg)](https://github.com/pantarei/ansible-role-bitbucket)
 [![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-bitbucket.svg)](https://github.com/pantarei/ansible-role-bitbucket/blob/master/LICENSE)
 [![Ansible Role](https://img.shields.io/ansible/role/5985.svg)](https://galaxy.ansible.com/detail#/role/5985)

Ansible Role for Atlassian BitBucket Installation.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">bitbucket_archive</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Download archive filename for cache during (re)install.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_catalina</td>
<td align="left">yes</td>
<td align="left">/usr/share/bitbucket</td>
<td align="left"></td>
<td align="left">Location for the BitBucket installation directory.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_connector_port</td>
<td align="left">yes</td>
<td align="left">7990</td>
<td align="left"></td>
<td align="left">BitBucket Apache Tomcat connector port.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_home</td>
<td align="left">yes</td>
<td align="left">/var/lib/bitbucket</td>
<td align="left"></td>
<td align="left">Location for the BitBucket home directory.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_jvm_maximum_memory</td>
<td align="left">yes</td>
<td align="left">1024m</td>
<td align="left"></td>
<td align="left">BitBucket JVM maximum memory usage.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_jvm_minimum_memory</td>
<td align="left">yes</td>
<td align="left">512m</td>
<td align="left"></td>
<td align="left">BitBucket JVM minimum memory usage.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_jvm_support_recommended_args</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Atlassian Support recommended JVM arguments.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_pass</td>
<td align="left">yes</td>
<td align="left">ahle4Boo</td>
<td align="left"></td>
<td align="left">Password for BitBucket system user.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_proxy_name</td>
<td align="left">no</td>
<td align="left"><code>null</code></td>
<td align="left"></td>
<td align="left">Pass value as <code>proxyName</code> to <a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/templates/usr/share/bitbucket/conf/server.xml.j2">template</a>.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_scheme</td>
<td align="left">no</td>
<td align="left"><code>null</code></td>
<td align="left"><ul>
<li><code>null</code></li>
<li>http</li>
<li>https</li>
</ul></td>
<td align="left">Install BitBucket in standalone mode if <code>null</code>, or integrating with Apache using HTTP if <code>http</code>, or integrating with Apache using HTTPS if <code>https</code>.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_server_port</td>
<td align="left">yes</td>
<td align="left">8006</td>
<td align="left"></td>
<td align="left">BitBucket Apache Tomcat server port.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_sha256</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Download archive sha256 checksum for cache during (re)install.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_upgrade</td>
<td align="left">no</td>
<td align="left"><code>false</code></td>
<td align="left"><ul>
<li><code>true</code></li>
<li><code>false</code></li>
</ul></td>
<td align="left">If <code>true</code>, trigger upgrade by stop existing BitBucket service, purge existing BitBucket installation direcoty before normal tasks.</td>
</tr>
<tr class="even">
<td align="left">bitbucket_url</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">URL for download archive.</td>
</tr>
<tr class="odd">
<td align="left">bitbucket_user</td>
<td align="left">yes</td>
<td align="left">bitbucket</td>
<td align="left"></td>
<td align="left">Username for BitBucket system user.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.bitbucket, bitbucket_user: 'bitbucket', bitbucket_pass: 'ahle4Boo', bitbucket_upgrade: 'false' }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-bitbucket/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

