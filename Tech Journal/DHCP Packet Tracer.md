# DHCP in Packet Tracer

## Creating a pool
* Go to the Services tab and enable DHCP
* Default gateway is the router address for VLAN
* Leave DNS at 0.0.0.0
* Start IP address -the first IP that you want to assign
* Subnet Mask for that VLAN
* Maximum Users - set this close to the requirements
* TFTP leave at 0.0.0.0
* Click Add

## Working with serverPool
* serverPool is the Default Pool and cannot be removed
* Use for VLAN 1 management
* Set start address to 100 in last octet

## Assigning ip helper addresses
* Enter CLI on switch that is routing
* `config t`
* `interface vlan *x*`
* `ip helper-address *server address*`
* Rinse and repeat for each VLAN

## Any issues?
* I actually had no issues for once, ***BIG*** win.
