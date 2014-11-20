Role Name
=========

Installs minimal Postgres 9.3 on CentOS 6.5

Requirements
------------

None.

Role Variables
--------------

Default values:

* port
* listen_addresses

You can override these values on your playbook.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: dbservers
      roles:
         - { role: tcosta84.postgres }

License
-------

BSD

Author Information
------------------

This role was created by Thiago Costa