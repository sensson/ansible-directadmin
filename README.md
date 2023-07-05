sensson.directadmin
=========

This module can be used to install DirectAdmin. It does not set an admin
password so you would have to set this yourself once the server is created
or retrieve it from /usr/local/directadmin/scripts/setup.txt.

It supports Ubuntu 20, CentOS 8 stream, Rocky Linux 8 and AlmaLinux 8.

Requirements
------------

We assume you have a valid DirectAdmin license.

Role Variables
--------------

* `license`: The DirectAdmin client id.
* `directadmin_configuration`: All DirectAdmin configurations
* `directadmin_custombuild_options`: All CustomBuild options.
* `directadmin_phpextensions`: All PHP extensions.
* `directadmin_lets_encrypt_host`: Create a certificate for the host's
  domain. If set to false it will not be created. Defaults to true.
* `directadmin_include_modsecurity`: Include ModSecurity playbook.
* `modsecurity`: Set to `'yes'` to enable.
* `modsecurity_ruleset`: This is the ruleset from DirectAdmin.

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: directadmin
  roles:
    - sensson.directadmin
```

We recommend using host variables to set your license. For example:

```yaml
[directadmin]
server.fqdn.com license=abcdefghijklmnopqrstuvw
```

License
-------

MIT

Author Information
------------------

Sensson is a hosting company. We try to share our work whenever possible. We
do not intend to offer commercial support on our open source modules. We do
welcome all pull requests though and will attempt to help whenever possible.
