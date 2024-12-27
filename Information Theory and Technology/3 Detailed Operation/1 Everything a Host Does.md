Category: [[Information Technology]] [[Data Journey]]
___
Prerequisites: [[1 Hosts]]
___
The following covers all situations.
### Scenario 1: Direct Connection Host to Host 
This scenario is basically: hosts within the same network. There could be hubs and switches in between, it doesn't matter. The hosts don't see that. 

Each host has a NIC, therefore a MAC address [[MAC Addresses]], both has an IP address ([[3 IP Addresses]]) and a subnet mask ([[12 Subnets and Masks]]). 

- Host A has data to send to host B. A knows the IP address of B. This is provided by the user. (e.g. B is google.com -> DNS[[Domain Name Service (DNS)]] -> google IP)
- By checking the subnet mask, A knows B is on the **same network** as A. 
- A creates the source/dest IP addresses and stamps these as a header onto the data segment (which already has a source/dest port header attached). 
- If A does not know B's MAC address already, A resolves it using ARP ([[Address Resolution Protocol (ARP)]])
- A stamps the source and destination MAC addresses onto the packet, creating a frame.
- The frame is sent to B. 
- B checks the dest MAC is right, discards the header.
- B checks the dest IP is right, discards the header. 
- B passes the segment to the process that delivers the data to the right port. 
### Scenario 2: Hosts on opposites of a Router
This scenario is basically: hosts within different networks. There may be multiple routers in between but that doesn't affect what the hosts do. 

Host A and Host C are part of two networks connected by a router in between. All 3 devices have an IP and MAC address. 

- A knows C's IP is on a foreign network by checking against A's own subnet mask. 
- A creates layer 3 header with A's IP and C's IP.
- A knows it needs to send the packet to the router (with the gateway IP. This IP is already configured into A.)
- A does not know router's MAC address. It invokes ARP. The router's MAC (in A's network) is mapped to the router's IP, and stored in A's ARP cache. This mapping can be reused for any communication with any foreign host.
- A creates layer 2 header with A's MAC and router's MAC. 
- A sends packet to router. 
- Router discards layer 2 header, whose sole purpose is to get the data from A's NIC to router's NIC. 
- Router does whatever it does to deliver the packet to C. ([[3 Everything that a Router Does]])
- C responds. Process identical to A. 
