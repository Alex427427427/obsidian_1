Category: [[Information Technology]] [[Network Devices]]
___
The identity of network devices. Gets stamped on every packet of information that gets sent over the internet. 

### Example
When a client requests something to a web server using a packet of information, **the client will stamp the source and destination IP addresses** on the packet. 

When the server responds by providing the webpage, it will also stamp the source and destination IP addresses, only reversed. 

Everything sent on the internet will have a source and destination IP add. 

### Structure
To all the network devices, an IP address is just 32 bits. (in IPv4?)
For human reading, we take those 32 bits, break into 4 chunks of 8 bits (called octets), and represent each one in decimal. (0-255)

### Assignment
Addresses are typically assigned in hierarchy.
##### Example
ACME corp. Owns all IP addresses that start with 10.x.x.x. 
Their New York office will have 10.20.x.x.
Their London office could have 10.30.x.x.
Tokyo, 10.40.x.x.
Each office may have different teams each with dedicated IP. 
New York sales: 10.20.55.x (allows 256 devices)
New York Engineering: 10.20.66.x
Tokyo sales: 10.40.55.x
...
##### Implementation
Subnetting


