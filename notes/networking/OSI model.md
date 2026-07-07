## OSI Model (Open System Interconnection Reference Model)
- Contains 7 layers

## Layer 1 - Physical
- This layer is not about protocols but rather concerns about getting a signal from one part of network to another via physical medium such as fiber, cables.
- Moves raw data as physical signal.
- Cables, fibers, signals
- **Security angle**: physical security — cable tapping, rogue devices plugged into open ports

## Layer 2 - Data Link
- Groups bits from layer 1 into organized packages called frames and ensures they travel safely between two directly connected devices (network cards) on the same network
- Refers to the physical address of device/adapter cards as MAC address
- Frame, MAC address, Switch
- **Security angle**: MAC spoofing, ARP poisoning attacks happen here

## Layer 3 - Network
- Also called Routing Layer, Router determines how to forward traffic using this layer.
- Packages data into packets, uses complex algorithms and routing tables to inspect a packet's destination IP address and decide the next optimal network "hop".
- IP address, Router, packets
- **Security angle**: IP spoofing; firewalls/ACLs filter traffic by IP at this layer

## Layer 4 - Transport
- Responsible for the reliable end-to-end delivery of data between applications on different devices
- Uses TCP (Transmission Control Protocol) and UDP (User Datagram Protocol)
- Breaks large data files into smaller segments for transmission, and reassembles them in the exact right order on the receiving end
- TCP, UDP ports
- **Security angle**: port scanning (Nmap) targets this layer; firewalls also filter by port

## Layer 5 - Session
- Provides communication management between devices such as creating/starting session, stopping session, and restarting session.
- Control protocols, tunneling protocols
- **Security angle**: session hijacking exploits weaknesses here

## Layer 6 - Presentation
- Acts as translator with responsibilities such as character encoding, data encryption/decryption, and data compression
- Combined with application layer in practice — OSI is a teaching model, not exactly how TCP/IP is implemented
- SSL / TLS
- **Security angle**: SSL/TLS encryption lives here — this is what HTTPS relies on

## Layer 7 - Application
- Serves as the direct interface that we see on our screen, between the network and the software application being used
- HTTP, HTTPS, FTP, DNS
- **Security angle**: most web attacks (SQL injection, XSS) target this layer — it's the most attacked layer overall
