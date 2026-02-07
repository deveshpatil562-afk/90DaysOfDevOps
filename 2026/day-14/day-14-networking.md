# Networking Fundamentals & Hands-on Checks

## Overview

Networking is a crucial aspect of **DevOps**, as it ensures seamless communication between various components of an IT infrastructure.  
Understanding networking fundamentals enables DevOps professionals to **design, implement, monitor, and troubleshoot** systems effectively.

---

## Networking Basics

Networking refers to the practice of connecting computers, servers, and services so they can communicate and share data.  
In DevOps, networking plays a key role in:

- Application deployment
- Service discovery
- Load balancing
- Monitoring and troubleshooting
- Security and access control

---

## OSI and TCP/IP Models

### OSI Model

The **OSI (Open Systems Interconnection)** model is a conceptual framework that explains how data travels through a network.  
It consists of **seven layers**, each responsible for a specific function in the communication process:

1. Physical  
2. Data Link  
3. Network  
4. Transport  
5. Session  
6. Presentation  
7. Application  

---

### TCP/IP Model

The **TCP/IP (Transmission Control Protocol / Internet Protocol)** model is the most widely used networking model in real-world systems and the internet.

It consists of **four layers**:

1. Network Interface
2. Internet
3. Transport
4. Application

TCP/IP is the foundation of modern DevOps networking and cloud communication.

---

## OSI vs TCP/IP Model

![OSI-model-vs-TCP-IP-model](https://github.com/user-attachments/assets/35c8ab6f-1768-48a2-ae12-f8db7c07926e)

---

## Layers and Their Uses

### OSI Model (7 Layers)

| Layer | Name | Purpose |
|------|------|--------|
| L1 | Physical | Raw bits over cables or wireless media |
| L2 | Data Link | Frames, MAC addressing, error detection |
| L3 | Network | Logical addressing and routing (IP) |
| L4 | Transport | Reliable/unreliable delivery (TCP/UDP) |
| L5 | Session | Session management and synchronization |
| L6 | Presentation | Data translation, encryption, compression |
| L7 | Application | End-user services (HTTP, FTP, SMTP) |

---

### TCP/IP Stack (4 Layers)

| TCP/IP Layer | Maps to OSI | Examples |
|-------------|------------|---------|
| Link (Network Access) | L1 + L2 | Ethernet, Wi-Fi |
| Internet | L3 | IP, ICMP, ARP |
| Transport | L4 | TCP, UDP |
| Application | L5–L7 | HTTP, DNS, SMTP, TLS |

---

## Common Networking Commands (Hands-on)

| Command | Purpose | OSI Layer |
|------|--------|----------|
| `ping` | Test connectivity | Layer 3 |
| `traceroute` | Show network path/hops | Layer 3 |
| `curl` | Test application services | Layer 7 |
| `nc` (netcat) | Check port reachability | Layer 4 |
| `nslookup` / `dig` | DNS resolution | Layer 7 |
| `ip addr` / `ip route` | Check IPs and routing | Layer 3 |
| `arp -a` | MAC address resolution | Layer 2 |
| `netstat` / `ss` | View sockets and listening services | Layer 4 / 7 |

---

## Hands-on Screenshots

![Networking Screenshot 1](https://github.com/user-attachments/assets/d2ad1345-ec36-4a88-a307-69733f0def69)

![Networking Screenshot 2](https://github.com/user-attachments/assets/9656cb13-5152-4f01-b25e-9ab2d936675e)

![Networking Screenshot 3](https://github.com/user-attachments/assets/070443fa-a5d8-4fc5-be51-1e5a68237cc5)

![Networking Screenshot 4](https://github.com/user-attachments/assets/becdbde3-b4b7-42d8-b251-f146ece3eae9)

---

## Summary

Understanding networking fundamentals, OSI & TCP/IP models, and common diagnostic commands is essential for every DevOps engineer.  
These concepts form the backbone of **cloud computing, Kubernetes, CI/CD pipelines, and microservices communication**.

---
