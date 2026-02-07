### Networking Fundamentals & Hands-on Checks:

## Networking:
               Networking is a crucial aspect of DevOps, as it ensures seamless communication between various components of an IT infrastructure.
Understanding the fundamentals of networking is essential for DevOps professionals to design, implement, and troubleshoot networks effectively.

## OSI and TCP/IP Model:

****OSI Model: ****
            The OSI (Open Systems Interconnection) model is a conceptual framework that describes how data moves through a network. 
            It consists of seven layers, each with a specific function in the communication process. 
            These layers are Physical, Data Link, Network, Transport, Session, Presentation, and Application. 

**TCP/IP Model:**
                TCP/IP (Transmission Control Protocol/Internet Protocol) is a set of communication protocols that allow computers to communicate over the internet. 
                It is the most widely used networking protocol suite in DevOps networking.
                TCP/IP is a four-layered model consisting of the Network Interface Layer, Internet Layer, Transport Layer, and Application Layer.


![OSI-model-vs-TCP-IP-model](https://github.com/user-attachments/assets/35c8ab6f-1768-48a2-ae12-f8db7c07926e)


### Layer ands there use:

## OSI Model (7 Layers)
- Physical (L1) – Raw bits over cables/wireless.
- Data Link (L2) – Frames, MAC addressing, error detection.
- Network (L3) – Logical addressing, routing (IP).
- Transport (L4) – Reliable/unreliable delivery (TCP/UDP).
- Session (L5) – Session management, synchronization.
- Presentation (L6) – Data translation, encryption, compression.
- Application (L7) – End-user services (HTTP, FTP, SMTP).
  
## TCP/IP Stack (4 Layers)
- Link (Network Access) – Combines OSI L1 + L2 (Ethernet, Wi-Fi).
- Internet – OSI L3 (IP, ICMP, ARP).
- Transport – OSI L4 (TCP, UDP).
- Application – OSI L5–L7 combined (HTTP, DNS, SMTP, TLS).

### Commands:

- ping → test connectivity (Layer 3).
- traceroute → show path/hops (Layer 3).
- curl → test application services (Layer 7).
- nc (netcat) → check port reachability (Layer 4).
- nslookup / dig → DNS resolution (Layer 7).
- ip addr / ip route → check IPs and routing (Layer 3).
- arp -a → check MAC resolution (Layer 2).
- netstat / ss → list sockets and listening services (Layer 4/7).

<img width="1300" height="737" alt="Screenshot 2026-02-07 143646" src="https://github.com/user-attachments/assets/d2ad1345-ec36-4a88-a307-69733f0def69" />
<img width="1577" height="292" alt="Screenshot 2026-02-07 143723" src="https://github.com/user-attachments/assets/9656cb13-5152-4f01-b25e-9ab2d936675e" />
<img width="827" height="127" alt="Screenshot 2026-02-07 143757" src="https://github.com/user-attachments/assets/070443fa-a5d8-4fc5-be51-1e5a68237cc5" />
<img width="666" height="205" alt="Screenshot 2026-02-07 143827" src="https://github.com/user-attachments/assets/becdbde3-b4b7-42d8-b251-f146ece3eae9" />

