Category: [[Information Technology]] [[Data Journey]]
___
Prerequisites: [[8 Switches]] [[1 Everything a Host Does]] [[MAC Addresses]] [[3 IP Addresses]]
___
Switching is moving data within a network. 

### Setup
Multiple devices (A,B,C,D) are connected in a network by a central switch. Each device has an IP and MAC address. **The theoretical switch does not have either**.

The switch is blind to layer 3 headers. Only layer 2. It doesn't even know if a device is a host or a router. 

Switches use and maintain **MAC Address Table**. Which maps switch ports to MAC addresses.

The MAC address table starts out empty. 

### Actions
Switches only perform 3 actions:
- Learn - update MAC Address Table with mapping of port to source MAC in the appropriate entry. This happens whenever a message arrives on a port. 
- Flood - duplicate and send frame out all switch ports except for the source port. This happens when the MAC Address Table does not contain entries of the destination MAC address. This can also happen when the destination MAC address is all F's, which is a deliberate broadcast, such as during ARP. ([[Address Resolution Protocol (ARP)]])
- Forward - when the MAC Address Table contains the destination MAC address's port, the switch just sends the frame to that port. 

This is enough to cover all communication. 

### Caveat - Switches can have their own MAC and IP
The switch CAN have its own MAC and IP address. This is required when you want to send and receive data TO and FROM the switch (perhaps using Telnet [[Telnet (Teletype Network)]] or SSH [[SSH (Secure Shell)]] to log into the switch). Most of the time, data goes THROUGH the switch, so its MAC and IP are ignored. 

### Unicast vs Broadcast
Unicast = when destination MAC is not FFFFF....
Broadcast = when destination MAC is FFFFFF....
"Unicast flooding" = the special case where a unicast message's dest MAC is not in the table, and flooding is required for the switch to learn. 

### VLANs (Virtual Local Area Networks)
[[Virtual Local Area Networks (VLANs)]]

### Multiple Switches
It's possible to have multiple switches at the nexus of a network, connected to each other directly. 
MAC Address Table is populated in exactly the same way. Some quick thought reveals that communication happens as normal. The rows in the MAC address table will just have multiple entries.

