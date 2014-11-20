Ansible Role: Postgres
======================

Installs minimal Postgres 9.3 on CentOS 6.5

Requirements
------------

None.

Role Variables
--------------

Default values:

* postgres_port: 5432
* postgres_listen_addresses: localhost
* postgres_pg_hba

Optional variables:

* postgres_pg_hba_custom
* postgres_db_name
* postgres_db_user
* postgres_db_pass
* postgres_db_pass_encrypted

You can override these values on your playbook.

Dependencies
------------

* tcosta84.yum

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: tcosta84.postgres }

With overriden default variables and optional variables

    - hosts: servers
    vars:
        - postgres_listen_addresses: '*'
        - postgres_db_name: myappdb
        - postgres_db_user: postgres
        - postgres_db_pass: md53175bce1d3201d16594cebf9d7eb3f9d
        - postgres_db_pass_encrypted: true
        - postgres_db_encoding: UTF-8
        - postgres_db_lc_collate: pt_BR.UTF-8
        - postgres_db_lc_ctype: pt_BR.UTF-8
        - postgres_db_template: template0
        - postgres_pg_hba_custom:
            - { type: host, database: myappdb, user: postgres, address: 0.0.0.0/0, method: md5 }
    roles:
        - ansible-role-postgres

License
-------

BSD

Author Information
------------------

This role was created by [Thiago Costa](http://thiagocostapy.com)
