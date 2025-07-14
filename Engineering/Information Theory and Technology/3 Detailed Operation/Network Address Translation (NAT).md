Category: [[Information Technology]] 
___
Prerequisites: [[3 IP Addresses]]
___
Everything on the internet needs an IP address. 32 bits. This has about 4 billion unique addresses. This is no longer enough to support the current internet. The long term solution is to come up with a new address space - IPv6, with 128 bits. About 25% of the world has been converted to IPv6 since its birth in 1990s. 

In the interim of this transition, we use NAT. 
NAT's idea is that in order to conserve this address space, **we must let a certain range of IP addresses reusable.** How is this possible and how does it lead to conservation? 

For a network (where we want to implement NAT), we assign that network a unique external (or "public") IP address, which is its address in the broader internet. And for the devices inside the network, we assign internal IP addresses. Valid internal (or "private") addresses are:
- 10.0.0.0 / 8
- 172.16.0.0 / 12
- 192.168.0.0 / 16
For how masks work, check [[12 Subnets and Masks]]. 

We also must agree to **never assign those private IP addresses as the public address of any network**. So those addresses are explicitly reserved for private addresses. If we didn't do this, it would be impossible for a device to know whether the packet is going to another device in its own network or to some distant network with that IP. 

NAT translates between the private addresses into the public address. 

In extreme cases, entire ISPs ([[Internet Service Providers (ISPs)]]) may share one public IP address!

**But here's a crucial puzzle: if all computers from within a network appear as the same IP on the public network, how does the router know which computer to send an incoming packet to?**
### PAT (Port Address Translation)
What solves the above question. 

Uses the **Port** ([[Ports]]) portion of the outgoing messages (and hence incoming messages) to encode which computer AND which port is mapped to it. 

**THE PORT IS CLOSED WHEN A PACKET IS RECEIVED**. This is for security reasons. 

It is also random which port maps to whip device/port combination at any given **session** (so the mapping is constant over a session. But is immediately wiped after the session.). 

Stored in a table. 

E.g. 

| Public address   | Private address   |
| ---------------- | ----------------- |
| 98.12.7.250 : 12 | 10.0.0.1 : 65535  |
| 98.12.7.250 : 13 | 10.0.0.1 : 80     |
| 98.12.7.250 : 14 | 192.168.0.2 : 123 |
| 98.12.7.250 : 15 | 192.168.0.2 : 80  |

Because there are 65535 possible port addresses, and there are very unlikely to be more than 65535 concurrent combinations of device and ports in the private network, this scheme works. 

[[Port Forwarding]] is a specific usage of NAT / PAT. 

### Relationship to Firewall ([[Firewall]])
While NAT is a configuration within the router, it needs the firewall rules to be updated to work. Have a quick think until this is obvious. 

### Difference to Port Forwarding and why is port forwarding considered more dangerous
In NAT, the port mappings are dynamic, always changing, different for every communication round. When no communications are happening, the mappings are null, (called **ports being closed**). This behaviour makes NAT more secure. 

In port forwarding, the port mappings are static. And always on. 

In short, **in standard usage, NAT mappings are dynamic and temporary, while port forwarding mappings are static and persistent**.
