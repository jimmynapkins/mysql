mysql
========

[![Build Status](https://drone-opsdev.rax.io/github.com/rack-roles/mysql/status.svg?branch=master)](https://drone-opsdev.rax.io/github.com/rack-roles/mysql)

This is a basic role to install and configure MySQL.

Requirements
------------

No external requirements.

Role Variables
--------------

## Mandatory
These values should be overridden.
* `mysql_root_password`
* `mysql_replication_password`
* `mysql_server_id`

## Standard
* `mysql_bind_address` Defaults to 127.0.0.1
* `mysql_port` Defaults to 3306

## Replication
* `mysql_replication` False
* `mysql_replication_role` Set either `master` or `slave`.
* `mysql_replication_user` replicant
* `mysql_log_bin` "/var/lib/mysql/binary-log"
* `mysql_expire_logs_days` 5
* `mysql_relay_log` "/var/lib/mysql/relay-log"
* `mysql_relay_log_space_limit` "4G"

Dependencies
------------

`Rackspace_Automation.holland` (Optional)

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: Rackspace_Automation.mysql, x: 42 }

License
-------

BSD

Author Information
------------------

[Rackspace - the open cloud company](http://rackspace.com)

Ask about our DevOps Automation Service - [www.rackspace.com/devops](http://rackspace.com/devops)
