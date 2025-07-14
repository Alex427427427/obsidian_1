Category: [[Information Technology]] [[OSI Model]]
___

Layers 1-4 are what are important to understand how data flows through the internet. [[1 Physical Layer]] - bits to physics (modem), [[2 Data Link Layer]] - hop to hop (MAC), [[3 Network Layer]] host to host (IP), [[4 Transport Layer]] - service to service (Ports). 

The following is what is actually happening when a host wants to send a packet.
### Encapsulation
- A host application generates a packet of data. 
- It goes to layer 4, where the OS' network commands/syscalls add the source and destination port numbers according to either the RCP or UDP protocol. The result is called a **segment**.
- Then it goes to layer 3, where the source and destination IP addresses are added. The result is a **packet**. To layer 3, the layer 4 headers are just data, a bunch of 1s and 0s.
- Then layer 2 adds MAC addresses. [[MAC Addresses]]. The result is a **frame**. 
- Then the frame arrives on layer 1, the wire.

### Decapsulation
Reverse of the encapsulation. 
At every layer, the layer checks the header. If it's addressed to the right place, the header will be discarded and the data passed up the layers, until the transport layer checks the port and sends it to the right port. 
