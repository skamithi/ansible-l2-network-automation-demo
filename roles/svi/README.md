svi Role
=========

Configures SVI interfaces on either a Nexus Based Switch


Requirements
------------

None

Role Variables
--------------

Each ``svi_interface`` object contains the following attributes:

* ``address``: IP address of SVI interface in CIDR form. Eg 10.1.1.1/24
* ``vlan_id``: Vlan ID to associate the SVI with. Example: 222
* ``priority``: HSRP priority number.
* ``vip``: HSRP Virtual IP

Example:

```
svi_interfaces:
  - address: 10.1.1.1/24
    vlan_id: 200
    priority: 90
    vip: 10.1.1.254
```

Dependencies
------------

None

Example Playbook
----------------


Example 1

```
- hosts: all
  connection: local
  vars:
    login_info:
       host: "{{ inventory_hostname }}"
       username: "{{ ansible_user }}"
       password: "{{ vault_ansible_password }}"

  tasks:
    - role: svi
      domain_name: linuxsimba.local

```

License
-------
MIT

