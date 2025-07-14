Category: [[Information Technology]] [[Network Devices]]
___
[[6 Hubs]] have a problem of unnecessarily generating too much traffic. 

Instead of having one giant network at a single hub, we break them into multiple smaller networks each with a hub. 

Imagine two. 

Connecting the two hubs, is a device called a bridge. This contains the traffic to each side. 

### Working
The hub regenerates the packet at all ports. One of them reaches the bridge. The bridge has memory to know which IP addresses are on which side of the bridge. So if the destination IP is on the same side that the packet came from, the bridge won't do anything. Else, the bridge will forward it to the other hub. 

The bridge is the first device that contains traffic into regions. 

The bridge only works between hubs that all lie within one network. They do not enable different networks to connect to each other. This fact will be more obvious by the [[9 Routers]] article.