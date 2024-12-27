Category: [[Information Technology]]
___
Device A needs to send a packet to device B on the same network.
A has the IP of B, but not the MAC ([[MAC Addresses]]). Thus it cannot perform a hop. 
Here is where ARP is invoked. 
### Working of the ARP
- A sends an ARP request. It contains the destination IP, and a code that encodes the instruction "if this is your IP, send back your MAC address".
- This request is a packet sent using the MAC address FF-FF-FF-FF-FF-FF. This is a special MAC address, the messages addressed to which gets broadcasted to all devices on the network. This behaviour is implemented in the switch. ([[8 Switches]]) When the switch receives a message with that address, it sends the data through all ports. 
- All other devices on the network checks the IP against their own. If they don't match, the message is dropped at that device. If they match, the device is device B. 
- Device B, having received and checked that the ARP request is meant for itself by comparing IP addresses, also notes down the source MAC address associated with the source IP address. This is used for future messaging. 
- Device B sends an ARP response containing its own MAC address, to the correct MAC address of device A. 

The process does not change if B exists on some remote network. 
The destination IP of the ARP request would be the IP of the gateway (router), and the desired MAC address is that of the router. 

**The IP-MAC mappings are stored in an ARP cache for the device.**
