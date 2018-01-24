trunk Role
=========

Configures a set of trunk interfaces with a single VLAN. The vlan does not
replace any existing VLANs. Additionally logic is added to add idempotency

Requirements
------------

None

Role Variables
--------------

* ``vlan_id``: Vlan ID to associate the SVI with. Example: 222

* ``trunk_ifaces``. List of trunk interfaces to update. Configure this variable
  as a group variable or host variable

Example:

```
trunk_ifaces:
  - PortChannel10
  - PortChannel11
  - Ethernet2/2
```

Dependencies
------------

None

Example Playbook
----------------


Pass the ``vlan_id`` variable as an extra variable

```
- hosts: all
  connection: local
  vars:
    login_info:
       host: "{{ inventory_hostname }}"
       username: "{{ ansible_user }}"
       password: "{{ vault_ansible_password }}"

  tasks:
    - role: trunk

```

License
-------
MIT

