# Lab 2-1: Subnet Design

* Commands to navigate different modes on a Cisco Switch/Router (enable, config t...) and how you know what mode you are in
  * Cisco uses a tiered command hierarchy
  * EXEC mode
    * this is the default mode, denoted by a `>`
  * Priviledged EXEC mode
    * This can be accessed by typing `enable` in EXEC mode
    * Denoted by a `#`
  * Configuration mode
    * This can be accessed from priviledged EXEC mode by typing `config`
    * Denoted by a `(config)#`
  * Interface Commands
    * This can be accessed from configuration mode by typing `interface *interface-id*`
    * Denoted by `(config-if)#`
  * VLAN Commands
    * This can be accessed by typing `interface vlan *vlan-id*`
    * denoted by `(config-vlan)#`
* Commands to create VLANS on switch
  * `conf t`
  * `vlan *number* *name*`
  * `interface vlan *number*`
  * `switchport mode access`
  * `switchport access *port*` for assigning ports VLANs
  * `show vlan *number*`
* Configure interfaces in "ranges"
  * `interface range FastEthernet 0/*x-y*`
