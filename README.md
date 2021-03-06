Ansible Role: Supervisor
========================

[![Build Status](https://travis-ci.org/kevincoakley/ansible-role-supervisor.svg?branch=master)](https://travis-ci.org/kevincoakley/ansible-role-supervisor)

Ansible role to install and manage supervisord

Requirements
------------

None

Role Variables
--------------

List of programs that should be managed by supervisord:

    supervisor_programs:
        - { name: "program_name", command: "/usr/bin/program -d", directory: "/tmp/" }

Dependencies
------------

None

Example Playbook
----------------

Example supervisor_playbook.yml:

    - hosts: servers
    
      vars:
        supervisor_programs:
          - { name: "mysql", command: "/usr/bin/mysqld_safe" }
          
      roles:
         - supervisor

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)
