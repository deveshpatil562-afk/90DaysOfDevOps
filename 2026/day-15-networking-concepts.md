# 🌐 Networking Fundamentals – Practical Notes

This document covers essential networking concepts with clear explanations and real-world examples. Perfect for beginners, interview prep, or quick revision.

---

## 🧩 Task 1: DNS (Domain Name System)

### 📖 What is DNS?

The **Domain Name System (DNS)** is often called the *phonebook of the Internet*. It translates **human-friendly domain names** (like `google.com`) into **machine-friendly IP addresses** (like `142.250.190.14`).

Without DNS, we would need to remember IP addresses instead of simple domain names.

---

### 🧠 Common DNS Record Types

| Record Type | Full Form      | Purpose                                 |
| ----------- | -------------- | --------------------------------------- |
| **A**       | Address        | Maps a domain name to an IPv4 address   |
| **AAAA**    | IPv6 Address   | Maps a domain name to an IPv6 address   |
| **CNAME**   | Canonical Name | Alias that points one domain to another |
| **MX**      | Mail Exchange  | Specifies mail servers for a domain     |
| **NS**      | Name Server    | Shows authoritative DNS servers         |

---

### 🔍 Example Explanation

* **A Record** maps the domain name to IPv4 address: `142.251.141.110`
* **TTL (Time To Live)** = `160 seconds`

  * This means the DNS record can be cached for 160 seconds before it must be refreshed.

---

## 🧩 Task 2: IPv4 Addressing

### 📌 What is an IPv4 Address?

An **IPv4 address** is a unique numerical identifier assigned to devices on a network. It allows devices to locate and communicate with each other over IP networks.

An IPv4 address is divided into:

* **Network ID** → Identifies the network
* **Host ID** → Identifies the specific device on that network

#### 🧪 Example

For `192.168.1.10/24`:

* **Network ID**: `192.168.1.0`
* **Host ID**: `10`

---

### 🌍 Public vs Private IP Addresses

#### 🌐 Public IP Address

* Assigned by **ISP**
* Globally unique
* Accessible over the Internet
* Example: `203.0.113.25`

#### 🏠 Private IP Address

* Used inside **local networks** (home/office)
* Not routable on the Internet
* Example: `192.168.1.10`

---

### 🔐 Private IP Address Ranges

| Range                           | Usage                        |
| ------------------------------- | ---------------------------- |
| `10.0.0.0 – 10.255.255.255`     | Large enterprise networks    |
| `172.16.0.0 – 172.31.255.255`   | Medium-sized organizations   |
| `192.168.0.0 – 192.168.255.255` | Home & small office networks |

#### 🖼️ Private IPs from the system example

* `172.30.1.2`
* `172.17.0.1`
* `127.0.0.1` → Loopback (special local-only address)

---

## 🧩 Task 3: CIDR & Subnetting

### 🔹 What does `/24` mean in `192.168.1.0/24`?

* `/24` means **first 24 bits** are for the network
* Remaining **8 bits** are for hosts

---

### 🔢 Usable Hosts Explained

| CIDR  | Total IPs | Usable Hosts |
| ----- | --------- | ------------ |
| `/24` | 256       | 254          |
| `/16` | 65,536    | 65,534       |
| `/28` | 16        | 14           |

> ⚠️ Two IPs are always reserved: **Network address** & **Broadcast address**

---

### 🧠 Why Do We Subnet?

* Improves network management
* Reduces broadcast traffic
* Enhances security
* Efficient IP utilization

---

### 📊 CIDR Summary Table

| CIDR  | Subnet Mask     | Total IPs | Usable Hosts |
| ----- | --------------- | --------- | ------------ |
| `/24` | 255.255.255.0   | 256       | 254          |
| `/16` | 255.255.0.0     | 65,536    | 65,534       |
| `/28` | 255.255.255.240 | 16        | 14           |

---

## 🧩 Task 4: Network Ports

### 🚪 What is a Port?

A **port** is like a *doorway* on a computer that allows specific services or applications to communicate over the network.

* Each service listens on a specific port number
* Multiple services can run on the same IP using different ports

---

### ❓ Why Do We Need Ports?

* Differentiate services (Web, SSH, DB, etc.)
* Allow multiple apps on the same IP
* Enable secure and organized communication

---

### 🔌 Common Ports & Services

| Port  | Service            |
| ----- | ------------------ |
| 22    | SSH (Remote login) |
| 80    | HTTP               |
| 443   | HTTPS              |
| 53    | DNS                |
| 3306  | MySQL              |
| 6379  | Redis              |
| 27017 | MongoDB            |

---

### 🖥️ Matched from System

| Port | Service                               |
| ---- | ------------------------------------- |
| 22   | SSHD (Secure Shell Daemon)            |
| 53   | systemd-resolved (Local DNS resolver) |

---

## 🧩 Task 5: Real-World Networking Scenarios

### 🌐 Example 1: Web Request

```bash
curl http://myapp.com:8080
```

**What happens here?**

1. DNS resolves `myapp.com` → IP address
2. TCP connection is established
3. Port `8080` identifies the target service

---

### 🛠️ Example 2: App Can’t Reach Database

**Issue:** App can’t connect to `10.0.1.50:3306`

**Troubleshooting Steps:**

1. Check host reachability (`ping 10.0.1.50`)
2. Verify port `3306` is open
3. Ensure database service is running
4. Check firewall & security rules

---

## ✅ Summary

This guide connects **DNS, IP addressing, subnetting, ports, and real-world troubleshooting** into one clear picture of how networks actually work.

Happy Networking 🚀
