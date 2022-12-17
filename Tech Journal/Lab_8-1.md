# Lab 8-1

## Output of "sh ip route" on West Router

<img width="542" alt="Screenshot 2022-12-16 at 10 16 20 PM" src="https://user-images.githubusercontent.com/71239122/208221365-3b74fbcb-c103-41c3-b93d-7649cbf7df4f.png">


## Output of "sh ip route" on East Router
<img width="532" alt="Screenshot 2022-12-16 at 10 16 13 PM" src="https://user-images.githubusercontent.com/71239122/208221367-ed9ba699-17f1-41c1-ab48-2b74aa9c9164.png">

## Output of "sh ip route" on Data Center Router
<img width="534" alt="Screenshot 2022-12-16 at 10 16 06 PM" src="https://user-images.githubusercontent.com/71239122/208221368-b178c5e9-d484-4fd2-a976-71765d07efe9.png">

## Configuring OSPF

### Steps:

1. Create OSPF instance
  1. `router ospf instance_number` (I usually use 1)
3. Advertise on Area 0
  1. `#(config-router) network network_address wildcard_mask area 0` **DO THIS FOR ALL DIRECTLY CONNECTED NETWORKS**
4. Reference routing tables to ensure it is working (`sh ip route`, OSPF entries will be prefixed with an "O")

> Wildcard mask is INVERSE of subnet mask (ex. 0.0.0.255 for /24 network)
