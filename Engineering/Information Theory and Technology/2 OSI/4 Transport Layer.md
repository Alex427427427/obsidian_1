Category: [[Information Technology]] [[OSI Model]]
___
### Goal
Service to service delivery. 

Consider a computer that has an IP and MAC address. There is a browser open. There is also a chat app open. There is also an online game open. Each program must send and receive data onto the "wire". They will all share the same IP add for end to end delivery, and the same MAC add for hop to hop delivery. The question is: how do we make sure the right program receives the right packets? 

Layer 4 takes incoming data and splits into separate data streams in the computer. 

### Addressing Scheme: Ports
**A port is an address for a service**. 

Two schemes. 
0-65535: TCP - favours reliability
0-65535: UDP - favours efficiency.

### Working
Source and destination ports get stamped on the packet. 

Usually servers listen to requests on pre-defined ports. While clients select random ports for each connection. The response will arrive on that port. 

Each web page on a browser has a different port on the client computer. This is why different websites open at the same time won't start displaying data meant for other websites on the same computer. 


### Implementation
Usually in the OS' kernel. Involves syscalls. 