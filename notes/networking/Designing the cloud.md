## Cloud Networking Concepts

## Network Function Virtualization (NFV)
- Physical network devices (routers, switches, firewalls) are replaced with virtual versions running in a hypervisor
- Same functionality as physical devices, just software-based and deployable on-demand
- Hypervisor, virtual appliance

## VPC (Virtual Private Cloud)
- An isolated, private section of a cloud provider's infrastructure — your own virtual data center
- Organizations often use multiple VPCs to separate applications/departments while still managing them centrally
- **Security angle**: VPC isolation is a core security boundary — misconfigured VPC peering/routing can accidentally expose resources meant to stay private

## Transit Gateway
- A central "cloud router" that connects multiple VPCs together, enabling communication between them

## VPN (cloud context)
- Same concept as traditional VPN — used to securely connect remote users/sites to private VPCs via the transit gateway

## Internet Gateway
- Allows a VPC's resources to be reachable by anyone on the public internet (used for public-facing apps/websites)

## NAT Gateway
- Allows private VPC resources to reach OUT to the internet (e.g., software updates) using a public IP
- Does NOT allow unsolicited inbound connections — outbound only
- **Security angle**: this asymmetry (outbound allowed, inbound blocked) is a deliberate security control, not just a networking feature

## VPC Endpoint
- A direct private connection between VPCs on different cloud providers, bypassing the public internet entirely

## Security Groups & Security Lists (Cloud Firewalls)
- Function like traditional firewalls but for cloud resources — rules based on TCP/UDP port numbers and IP addresses/CIDR ranges
- **Security List**: broad rules applied automatically to an entire VPC/subnet (less granular, easier to manage)
- **Security Group**: rules applied to individual network interfaces/VNICs (more granular, more admin overhead)
- Example rule: TCP port 443 (HTTPS) inbound from any IP — normal for a public web server
- Example rule: TCP port 22 (SSH) inbound from any IP — ⚠️ common real-world misconfiguration; SSH should typically be restricted to specific trusted IPs, not "any"
- **Security angle**: this is a very common cloud pentest/bug bounty finding — scanning for open SSH/RDP ports exposed to the entire internet on misconfigured cloud instances is a well-known attack surface discovery technique
