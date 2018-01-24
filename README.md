# L2 Network Automation Demo

Demonstrates Cisco Network L2 Automation

* ``configure_vlan.yml`` - Adds Single VLANs to both IOS and Nexus Based Cisco
  switches. The config is idempotent. Variables required are:

 `` configure_svi.yml`` - Adds single SVI interface to either IOS or Nexus Based
Switch

## Roles Used:

``vlan``: Adds a VLAN to an IOS or Nexus Switch
``switch-system``: Configure Domain name and Hostname
``svi``: Create SVI interfaces with HSRP configuration


## Example Ansible Playbook Calls

* Creating a VLAN and then a SVI

```
ansible-playbook configure_svi.yml
```

* Creating a VLAN

```
ansible-playbook configure_vlan.yml
```

