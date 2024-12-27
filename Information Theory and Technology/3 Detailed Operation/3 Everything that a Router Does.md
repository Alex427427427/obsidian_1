Category: [[Information Technology]] [[Data Journey]]
___
Prerequisites: [[1 Everything a Host Does]] [[9 Routers]]
___
### What a Router is
In RFC (Request for comment) 2406: "A node is a device that implements IPv6"
"A router is a node that forwards IPv6 packets not explicitly addressed to itself."
"A host is any node that is not a router."

So a router is anything that forwards packets not addressed to itself. 

A router has an IP address and MAC address for every network interface. 
### Routing Table
A map kept within the router, that maps IP addresses to network interfaces. 
Each router has a routing table. 
##### When a Network is Directly Connected 
The routing table immediately populates the network IPs with the interface mapping. E.g. 10.0.55.0/24 -> left; 10.0.55.0/24 -> right. 
### When a Network is not Directly attached
If an incoming packet has a destination IP whose network portion does not match any entry in the routing table, the router **drops** the packet. This is not ideal. 
##### Static Route 
A network administrator may manually populate the routing table with an entry. This is one way to handle foreign networks. 
##### Dynamic Route 
Routers automatically tell each other about routes. The routes are transitively worked out and applied to each routing table. 

**Note that for NOT directly connected networks, the routing table entry needs to be more specific than "which interface". It actually needs the IP address of the next router that the packet needs to be forwarded to. This is different to the Direct case, where it suffices to specify "left" or "right" interface.**
##### Dynamic Route Protocols (DRP)
What facilitates the sharing of dynamic routes. It may also resolve when multiple routing options exist for the same destination IP. 
### A Note on Memory - Route Summarisation
A router functionally needs to be able to handle every possible destination IP. But it does not need to store an entry per IP address in the address space. This is because the internet is hierarchical, and split into subnets. The prefixes of IP addresses dictate where they go. The total unique prefixes come out to be able 700 thousand (instead of 4 billion if we assume all IP addresses need a separate entry), which is comfortably held by a 2GB memory. 
### ARPs [[Address Resolution Protocol (ARP)]]
Every router also has an ARP, as required like in [[1 Everything a Host Does]]. 
### Hierarchy
Routers are deployed in a fractal tree-like hierarchy. This makes traversal way more efficient than other topologies. 
This is also what allows for **route summarisation** as discussed in the section "A note on memory".
