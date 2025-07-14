Category: [[Information Technology]]
___
Prerequisites: [[Firewall]] [[Ports]] [[Network Address Translation (NAT)]]
___
### Purpose
By default, private devices in a network like home network are NOT accessible (due to [[Firewall]]) or even visible (due to [[Network Address Translation (NAT)]]) to anyone else on the internet, except when the device INITIATES a communication with some service on the web.

Port forwarding allows private devices to be visible on the internet, so other hosts can connect to this device. 
### How it Works
Suppose a friend wants to send a packet to your computer. They don't have access to your device's IP. How can this be done? Their request has an IP (which will just be the public IP of your router) and a port number. 

What you could do, is use the port number to encode information of which computer needs this packet. Tell the router that, for every message with the port number x, send it to my computer. 

Configuring the router can be done by connecting to its IP on a browser.

A specific usage of [[Network Address Translation (NAT)]]. **Implemented in the NAT tables**.
### Relationship to Firewall
Port forwarding is done within the NAT process, in the router. 
But in conjunction, the firewall rules must be modified to allow those traffic. 
### Relationship to NAT and why is port forwarding considered more dangerous
In NAT, the port mappings are dynamic, always changing, different for every communication round. When no communications are happening, the mappings are null, (called **ports being closed**). This behaviour makes NAT more secure. 

In port forwarding, the port mappings are static. And always on. (**Port being always open**). 

In short, **in standard usage, NAT mappings are dynamic and temporary, while port forwarding mappings are static and persistent**.
