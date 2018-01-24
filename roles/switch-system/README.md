switch-system
=========

Configures the Domain name and hostname on a IOS or Nexus IOS switch

Requirements
------------

None

Role Variables
--------------

* The hostname is set from the ``inventory_hostname`` variable

* ``domain_name``: DNS domain

Dependencies
------------

None

Example Playbook
----------------


- hosts: all
  connection: local
  vars:
    login_info:
       host: "{{ inventory_hostname }}"
       username: "{{ ansible_user }}"
       password: "{{ vault_ansible_password }}"

  tasks:
    - role: switch-system
      domain_name: linuxsimba.local


License
-------
MIT

