Category: [[Information Technology]] [[Network Devices]]
___
Prerequisite: [[3 IP Addresses]]
___
Not to be confused with [[Network Address Translation (NAT)]]

Takes a network and divides into sub networks. Each subnet can be thought to behave exactly like a network from the host side. The difference lies in the router that implements the subnet structure. 

An IP address is split into a network portion and a host portion. 

### Subnet Mask
A string of 1s and 0s to be bitwise ANDed with the total IP address to find out the network portion. 
E.g. 
IP: 172.16.1.0
Mask: 255.255.0.0 - 16 bits 
Convert to binary. Bitwise AND. 
Network portion: 172.16
Host portion: 1.0

A common notation to identify a subnet is to write out the earliest valid IP address in that subnet, followed by a "/[number of 1s in the mask]". For example, the above subnet could be identified as 172.16.0.0 / 16. 

**The entire internet is a series of subnets. This illustrates the fact that subnets behave exactly like any network.**

### Default Gateway
The gateway (router's IP in this network) of the subnet is by default the earliest valid IP address in this subnet.

### Broadcast IP Address
The final valid IP address in a subnet is reserved for broadcasting into the subnet. This will be relevant later in [[Data Journey]].
