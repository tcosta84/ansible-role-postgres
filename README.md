Ansible Role: Postgres
======================

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

* tcosta84.yum

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: tcosta84.postgres }

License
-------

BSD

Author Information
------------------

This role was created by [Thiago Costa](http://thiagocostapy.com)
