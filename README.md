Experitest - PostgreSQL Server Ansible Role
=========

This role will install \ uninstall postgresql server for linux hosts

Requirements
------------

This has been tested on Ansible 2.4.0 and higher.

Compatibility matrix
--------------

| Distribution / PostgreSQL | <= 9.3 | 9.4 | 9.5 | 9.6 | 10 | 11 | 12 |
| ------------------------- |:---:|:---:|:---:|:---:|:--:|:--:|:--:|
| CentOS 7.x | NA | yes | yes | yes | yes | yes | upcoming |


Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| state | should the application be present or absent | present, absent | present | no |
| postgresql_version | postgresql version to install (check compatibility matrix) | string | 11 | no |
| postgresql_password | postgres user password for db connection | string |  | yes |
| postgresql_port | default postgresql port number | number | 5432 | no |
| extra_postgresql_conf | additional props to be override in postgresql.conf file | dict | {} | no |
| postgresql_data_directory | default postgresql data directory path | string | /var/lib/pgsql/postgresql_version/data | no |
| backup_before_uninstall | should take backup all database before uninstall | boolean | False | no |


Example Playbook
----------------
### [see working example](/example)