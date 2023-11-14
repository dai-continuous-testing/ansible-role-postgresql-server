Continuous Testing - PostgreSQL Server Ansible Role
=========

This role installs and uninstalls PostgreSQL for Linux hosts.

Requirements
------------

This is supported for Ansible 2.4.0 and higher.

Compatibility matrix
--------------

| Distribution / PostgreSQL | <= 9.3 | 9.4 | 9.5 | 9.6 | 10 | 11 | 12 |
| ------------------------- |:---:|:---:|:---:|:---:|:--:|:--:|:--:|
| CentOS 7.x | NA | yes | yes | yes | yes | yes | upcoming |


Role Variables
--------------

| Name | Description                                                | Type | Default | Required |
|------|------------------------------------------------------------|:----:|:-----:|:-----:|
| state | Should the application be present or absent                | present, absent | present | no |
| postgresql_version | PostgreSQL version to install (check compatibility matrix) | string | 11 | no |
| postgresql_password | PostgresSQL user password for db connection                | string |  | yes |
| postgresql_port | Default PostgresSQL port number                            | number | 5432 | no |
| extra_postgresql_conf | Additional properties to be overriden in postgresql.conf   | dict | {} | no |
| postgresql_data_directory | Default PostgreSQL data directory path                     | string | /var/lib/pgsql/postgresql_version/data | no |
| backup_before_uninstall | Back up all databases before uninstall                     | boolean | False | no |


Example Playbook
----------------
### See the [working example](/example).