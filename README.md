Ansible Role for BitBucket
==========================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-bitbucket.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-bitbucket)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-bitbucket.svg)](https://github.com/pantarei/ansible-role-bitbucket)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-bitbucket.svg)](https://github.com/pantarei/ansible-role-bitbucket/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/5985.svg)](https://galaxy.ansible.com/detail#/role/5985)

Ansible Role for Atlassian BitBucket Installation.

Requirements
------------

This role require Ansible 2.0 or higher.

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
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>bitbucket_archive</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Download archive filename for cache during (re)install.</td>
</tr>
<tr class="even">
<td>bitbucket_catalina</td>
<td>yes</td>
<td>/usr/share/bitbucket</td>
<td></td>
<td>Location for the BitBucket installation directory.</td>
</tr>
<tr class="odd">
<td>bitbucket_checksum</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Download archive sha256 checksum for cache during (re)install.</td>
</tr>
<tr class="even">
<td>bitbucket_connector_port</td>
<td>yes</td>
<td>7990</td>
<td></td>
<td>BitBucket Apache Tomcat connector port.</td>
</tr>
<tr class="odd">
<td>bitbucket_context_path</td>
<td>no</td>
<td><code>null</code></td>
<td></td>
<td>Pass value as <code>path</code> to <a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/templates/usr/share/bitbucket/conf/server.xml.j2">template</a>.</td>
</tr>
<tr class="even">
<td>bitbucket_gid</td>
<td>no</td>
<td></td>
<td></td>
<td>Specifying the GID for shared storage. NOTE: This value should only be set once before deploying and then never changed.</td>
</tr>
<tr class="odd">
<td>bitbucket_hash_salt</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Specific password hash salt for sha512.</td>
</tr>
<tr class="even">
<td>bitbucket_home</td>
<td>yes</td>
<td>/var/lib/bitbucket</td>
<td></td>
<td>Location for the BitBucket home directory.</td>
</tr>
<tr class="odd">
<td>bitbucket_jvm_maximum_memory</td>
<td>yes</td>
<td>1024m</td>
<td></td>
<td>BitBucket JVM maximum memory usage.</td>
</tr>
<tr class="even">
<td>bitbucket_jvm_minimum_memory</td>
<td>yes</td>
<td>512m</td>
<td></td>
<td>BitBucket JVM minimum memory usage.</td>
</tr>
<tr class="odd">
<td>bitbucket_jvm_support_recommended_args</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Atlassian Support recommended JVM arguments.</td>
</tr>
<tr class="even">
<td>bitbucket_pass</td>
<td>yes</td>
<td>ahle4Boo</td>
<td></td>
<td>Password for BitBucket system user.</td>
</tr>
<tr class="odd">
<td>bitbucket_proxy_name</td>
<td>no</td>
<td><code>null</code></td>
<td></td>
<td>Pass value as <code>proxyName</code> to <a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/templates/usr/share/bitbucket/conf/server.xml.j2">template</a>.</td>
</tr>
<tr class="even">
<td>bitbucket_scheme</td>
<td>no</td>
<td><code>null</code></td>
<td><ul>
<li><code>null</code></li>
<li>http</li>
<li>https</li>
</ul></td>
<td>Install BitBucket in standalone mode if <code>null</code>, or integrating with Apache using HTTP if <code>http</code>, or integrating with Apache using HTTPS if <code>https</code>.</td>
</tr>
<tr class="odd">
<td>bitbucket_server_port</td>
<td>yes</td>
<td>8006</td>
<td></td>
<td>BitBucket Apache Tomcat server port.</td>
</tr>
<tr class="even">
<td>bitbucket_uid</td>
<td>no</td>
<td></td>
<td></td>
<td>Specifying the UID for shared storage. NOTE: This value should only be set once before deploying and then never changed.</td>
</tr>
<tr class="odd">
<td>bitbucket_url</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-bitbucket/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>URL for download archive.</td>
</tr>
<tr class="even">
<td>bitbucket_user</td>
<td>yes</td>
<td>bitbucket</td>
<td></td>
<td>Username for BitBucket system user.</td>
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
        - { role: hswong3i.bitbucket }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-bitbucket/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

