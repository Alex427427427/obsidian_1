Category: [[Information Technology]] [[OSI Model]]
___
Prerequisite: [[2 Data Link Layer]]
___
While layer 2 handles hop to hop, between the NICs of each hop, **Layer 3 handles the "end to end"**.

Uses **IP Addresses**. [[3 IP Addresses]] 
Ids each host. 

Anything with an IP address exists at Layer 3. 

### If we have IP adds at layer 3, why do we need MAC addresses at layer 2? Conversely?
Each addressing scheme serves a different purpose. 
**Layer 2 information gets created and destroyed multiple times throughout the packet's journey**. Layer 2 info - a pair of MAC addresses - only exist within **one hop** between 2 NICs. Whereas the IP address survives the whole journey. 

To link a layer 3 address to a layer 2 address, as is required multiple times during the journey of a packet, we need the **ARP (Address Resolution Protocol)**. 
