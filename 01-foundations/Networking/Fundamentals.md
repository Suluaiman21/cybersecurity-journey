
# Networking Fundamentals

Networking is one of the core foundations of cybersecurity. This section documents my understanding of how devices communicate, how network traffic moves, and how common protocols and services work.

## 1. OSI Model

The OSI model divides network communication into seven layers:

1. **Physical** – Cables, signals, radio and physical hardware.
2. **Data Link** – MAC addresses, Ethernet and frames.
3. **Network** – IP addressing and routing.
4. **Transport** – TCP and UDP, ports and reliable communication.
5. **Session** – Establishing and managing communication sessions.
6. **Presentation** – Data formatting, encoding and encryption.
7. **Application** – Protocols such as HTTP, DNS, FTP and SMTP.

Understanding the OSI model helps identify where a network problem or security issue is occurring.

## 2. TCP/IP Model

The TCP/IP model is commonly used to describe how real-world network communication works. It consists of:

* Application
* Transport
* Internet
* Network Access

Protocols such as HTTP, DNS, TCP, UDP and IP operate within different parts of this model.

## 3. IP Addressing

An IP address identifies a device/interface on a network.

### IPv4

IPv4 uses 32-bit addresses, for example:

```text
192.168.1.10
```

Private IPv4 ranges are commonly used inside local networks, while public IP addresses can be reachable across the Internet.

### IPv6

IPv6 uses 128-bit addresses and was introduced to provide a much larger address space than IPv4.

## 4. MAC Addresses

A MAC address is associated with a network interface and operates primarily at the Data Link layer.

Example:

```text
00:1A:2B:3C:4D:5E
```

MAC addresses are important when understanding communication within a local network.

## 5. Subnetting and CIDR

Subnetting divides a network into smaller networks.

For example:

```text
192.168.1.0/24
```

The `/24` represents the network prefix. Subnetting helps control network size, organize devices and manage IP address allocation.

## 6. TCP vs UDP

### TCP

TCP provides reliable, connection-oriented communication.

It uses mechanisms such as:

* Three-way handshake
* Acknowledgements
* Retransmission
* Sequence numbers

### UDP

UDP is connectionless and does not provide the same reliability mechanisms as TCP.

It is often used where speed and low overhead are important, such as DNS queries and certain real-time applications.

## 7. Ports

Ports allow multiple network services to operate on the same device.

Some important ports include:

| Port | Protocol | Purpose                |
| ---- | -------- | ---------------------- |
| 21   | FTP      | File Transfer          |
| 22   | SSH      | Secure Remote Access   |
| 23   | Telnet   | Remote Access          |
| 25   | SMTP     | Email                  |
| 53   | DNS      | Domain Name Resolution |
| 80   | HTTP     | Web Traffic            |
| 443  | HTTPS    | Secure Web Traffic     |
| 3389 | RDP      | Remote Desktop         |

Understanding ports is particularly important during network enumeration and vulnerability assessment.

## 8. DNS

DNS (Domain Name System) translates domain names into IP addresses.

For example:

```text
example.com → 93.184.216.34
```

Instead of remembering an IP address for every website, users can interact with human-readable domain names.

DNS is also important in cybersecurity because attackers can abuse domains, DNS records and malicious infrastructure.

## 9. DHCP

DHCP automatically provides network configuration to devices.

This can include:

* IP address
* Subnet mask
* Default gateway
* DNS server

Without DHCP, devices on many networks would need to be configured manually.

## 10. HTTP and HTTPS

HTTP is the protocol used for communication between web clients and servers.

HTTPS is HTTP protected using TLS encryption.

For example:

```text
Client → HTTPS Request → Web Server
Client ← HTTPS Response ← Web Server
```

Understanding HTTP/HTTPS is particularly important for web security and penetration testing.

## 11. ARP

ARP (Address Resolution Protocol) is used on IPv4 networks to associate an IP address with a MAC address on the local network.

For example:

```text
Who has 192.168.1.10?
→ 00:1A:2B:3C:4D:5E
```

ARP is important when studying local network communication and attacks such as ARP spoofing.

## 12. Routing

Routing determines where network packets should be sent.

A device uses a routing table to determine the appropriate path for traffic.

Useful command:

```bash
ip route
```

A default gateway is typically used when traffic needs to leave the local network.

## 13. NAT

NAT (Network Address Translation) allows private IP addresses to communicate with external networks through a public IP address.

A common example is a home router allowing multiple devices such as laptops and phones to access the Internet using one public IP.

## 14. Firewalls

A firewall controls network traffic based on defined rules.

Rules can consider things such as:

* Source IP
* Destination IP
* Port
* Protocol
* Direction of traffic

Firewalls are an important layer of network defense, although they are not a complete security solution by themselves.

## 15. Client-Server Communication

Many applications use a client-server model.

For example:

```text
Client
   ↓
DNS Resolution
   ↓
Server IP
   ↓
TCP Connection
   ↓
HTTP/HTTPS Request
   ↓
Server Response
```

Understanding this process helps connect networking fundamentals with web security.

# Useful Networking Commands

```bash
ip addr                  # Display IP addresses and interfaces
ip route                 # Display routing table
ping 8.8.8.8             # Test network connectivity
traceroute example.com   # Trace the network path
nslookup example.com     # Query DNS information
dig example.com          # Perform DNS lookups
ss -tuln                 # Display listening TCP/UDP ports
arp -a                   # Display ARP information
curl https://example.com # Send an HTTP request
```

# Cybersecurity Relevance

Networking knowledge is essential for understanding how attacks and defenses work.

These fundamentals provide the foundation for areas I am currently developing toward, including:

* Network reconnaissance
* Nmap scanning
* Web application security
* Packet analysis
* Vulnerability assessment
* SOC and SIEM investigations
* Incident response
* Network security

The goal is not just to memorize protocols and ports, but to understand **how devices communicate and where security weaknesses can appear within that communication.**
