Category: [[Information Technology]] [[Network Devices]]
___
Prerequisites: [[8 Switches]]
___
Switches can only facilitate communication within their own network. What happens when different networks want to communicate with one another? 

That's what routers do. Most routers today come with **switches** in-built.
### Def
A device that facilitates comms between networks. 
### Security Policies
Routers provide traffic control points between networks. 
Routers sit on the boundary between networks. This makes it a logical place to implement security policies, or traffic filtering, or even redirecting traffic elsewhere. 
### Working
Routers learn which networks **they are attached to**. This knowledge is a **route**. All routes are stored on a **routing table**. That is all the networks that the router needs to know to funnel traffic out of the appropriate interface. 

A router has an IP address in every network they are attached to. You can configure your router just by typing in its IP into your browser. 
##### Example
the left network: 172.16.20.x
the right network: 172.16.30.x
The router sits inbetween. 

In the left network, the router has the identity 172.16.20.1
In the right network, the router has the id 172.16.30.254.
These two IP addresses are the **gateways** of each network. They are the hosts' way out of their respective networks. 

E.g. A computer in the left network has IP 172.16.20.33. This hosts knows it has to go through a router, and the IP address of that router is stored as the host's default gateway: 172.16.20.1.

### Routers Create Hierarchy in Networks ([[4 Networks]])
Every **subnet** [[12 Subnets and Masks]] has a gateway. The New York sales network will have a gateway to the new york network, which then forwards to the gateway of the new york engineering network. 

**For routers in working in detail, see [[3 Everything that a Router Does]] during data transit**.

