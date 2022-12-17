# Lab 9-2: BGP

# Lab Pre-reqs for BGP

1. Configuring Interfaces
    1. Configure connected interfaces and ping
    2. The BTV-DIST-MultiLayer Switch is the only device using VLANs
    3. Remember - on multi-layer switches, the IP is assigned to the VLAN not the interface (ex. `int vlan 10`, `ip address 192.168.1.10 255.255.255.0`)
    4. Ports need to be assigned to the correct vlan (ex. `int range fe0/2-7`, `switchport access vlan 10`)
  
2. Configuring Routing
    1. Turn on routing (multi-layer switches only) (ex. `ip routing`)
    2. Create ospf instance (ex. `router ospf 1`)
    3. Configure instance to advertise all directly connected networks (ex. `network 192.168.1.0 0.0.0.255 area 0`)
    
* Set default route (BTV router) 0.0.0.0 0.0.0.0 to 192.168.2.1 (ISP)
* `ip route 0.0.0.0 0.0.0.0 192.168.2.1`
* `default-information originate` in OSPF config to send default route to other routers in the area
* `redistribute ospf 1` in BGP config to advertise all of the Foster 202 Co routes

OSPF for routing within Foster 202 Co


# BGP routing for ISPs, Partner, Customer and external Foster 202
1. Define router instance
    1. `router bgp AS_Number_for_Router`
2. Identify peers 
    1. `(config-router) neighbor ip_of_peer remote-as as-number_of_peer`
3. Advertise Networks within that AS

> Example:
>> `(config-router) network 10.10.52.0 mask 255.255.255.0`
>> ```   
>>    192.168.1.0/30 is in AS 1010
>>    192.168.3.0/30 and 192.168.4.0/30 are in AS 2054
