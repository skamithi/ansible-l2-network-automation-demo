# L2 Network Automation Demo

Demonstrates Cisco Network L2 Automation

* ``configure_vlan.yml`` - Adds Single VLANs to both IOS and Nexus Based Cisco
  switches. The config is idempotent. Variables required are:


## Roles Used:

``vlan``: Adds a VLAN to an IOS or Nexus Switch
``switch-system``: Configure Domain name and Hostname


## Role Variables:

### ``vlan`` role

* ``vlan_id``: VLAN ID (_required_)
* ``vlan_name``: VLAN Name. (_required_)
