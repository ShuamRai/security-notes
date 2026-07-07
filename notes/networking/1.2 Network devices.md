## Networking Devices
## Router (Layer 3)
- Routes data from one IP to another IP within a network or different part of the world
- Connects diverse network types such as LAN, WAN

## Switch (Layer 2)
- forward network traffic based on MAC Address
- PoE

## Firewall
- Traditional filters traffic by TCP or UDP port number
- NGFW goes beyond port-based filtering to identify specific applications traversing the network, allowing administrators to allow or block them accordingly
- has VPN that enables encrpted tunnels between remote sites
- often sit at the ingress/egress points of a network, firewalls can perform routing functions, including Network Address Translation (NAT) and dynamic routing

## IDS and IPS
- systems monitor network traffic for known attacks called intrusions
- Intrusion Detection System (IDS) alerts administrators to threats
- Intrusion Prevention System (IPS) actively blocks them before they enter the network.

## Load Balancer
- networking device used to distribute incoming traffic across multiple physical servers which ensures high availability and prevents downtime, as it makes the backend infrastructure appear to the end-user as a single service
- If a server fails due to hardware or software issues, the load balancer detects the outage, removes that server from the rotation, and continues providing service using the remaining healthy servers
- They can perform TCP offloading to speed up communication and manage SSL offloading, which handles encryption and decryption tasks to reduce the processing burden on the individual servers
- By caching data on the load balancer, requests can be answered immediately without needing to query the backend servers
- uses Quality of Service (QoS) to prioritize certain types of traffic or use application-centric load balancing to route specific requests (like certain web pages) to designated servers

## Proxy
- acts as an intermediary device positioned between a user and an external network, such as the Internet,  Instead of a user communicating directly with a remote server, the proxy takes the request, performs it on the user's behalf, verifies the response, and then provides the answer back to the user
- Because the proxy sits in the middle of the conversation, it can cache content, allowing future requests for the same data to be served immediately without needing to access the Internet again
- useful for url filtering, content scanning, access control
-  Proxies can be explicit, requiring manual configuration in the user's applications or operating system, or transparent, which function invisibly without requiring any user-side configuration changes

## NAS and SAN
- Network Attached Storage (NAS): This provides file-level access, To read or modify a file, your system must pull the entire file across the network into its local memory, and then write the entire modified file back to the NAS
- Storage Area Network (SAN): This provides block-level access which behaves like reading or writing to a local storage drive. Instead of transferring an entire file, you only modify the specific blocks of data that have changed

## AP
- Access Point (AP) is a purpose-built networking device that enables wireless communication between devices and the wired network
- They act as an OSI Layer 2 (Data Link) device by bridging communication between the 802.11 wireless network and the 802.3 wired ethernet network
- In larger environments, organizations use multiple access points to provide seamless coverage. Because managing these individually is difficult, administrators use a Wireless LAN Controller (WLC) to provide a "single pane of glass" for centralized deployment, security monitoring, and configuration updates
