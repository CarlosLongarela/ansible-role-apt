Ansible Role: Apt
=========

Basics apps installation for other roles and system administration. This role is util for a empty xenial ubuntu before execute other roles.

Requirements
------------

None.

Role Variables
--------------

    aptget_update: true
    aptget_update_cache_valid_time: 3600

    aptget_upgrade: false
    aptget_distupgrade: false

    programas_instalar:
      - mc
      - nano
      - sysv-rc-conf
      - python-pip
      - python-dev
      - libmysqlclient-dev

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers

      gather_facts: no
      become: true

      vars:
        aptget_update_cache_valid_time: 3600
        aptget_upgrade: true

      roles:
         - { role: CarlosLongarela.apt }

License
-------

GPLv2

Author Information
------------------

This role was created in 2017, May by [Carlos Longarela](mailto:carlos@longarela.eu), from [Taberna WordPress](https://tabernawp.com/).
