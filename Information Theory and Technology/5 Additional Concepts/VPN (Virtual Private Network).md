Category: [[Information Technology]]
___
### Internet without VPN
When you order internet service from your [[Internet Service Providers (ISPs)]], they will set up your internet connection. When this is complete, all your activity will be routed through your ISP's servers. They could in principle see and log all your packets. They could share this information with other parties such as the government or advertisers. 

While the data segment is often encrypted ([[Encryption]]), the source and destination IP addresses are not. ([[3 IP Addresses]]). So it's completely visible which household is trying to visit which site. In the case that the ISP translates the source IP into the IP of their own closest server to you, this can still be within a few blocks. 
### VPN
A service. [[Proxy]] with encryption and larger scope (all traffic instead of traffic for specific services)

When you connect to the internet with a VPN active, packets leaving you are already encrypted (with the VPN servers) (and don't have to wait for the destination server to share some public key with you).

This encrypted traffic still goes through your ISP's servers as usual, but the next destination is one of the VPN servers. From there on, the VPN decrypts, handles the DNS ([[[Domain Name Service (DNS)]]]) lookup, and establishes encrypted connection and starts delivering content. 

The paid VPNs usually have policies that state they do not log your data. 

### Advantages
Privacy - no logging, no one knows which service your IP is trying to access. 

Region locked content - You simply need to connect to a VPN server in the region of interest to access those content. 



