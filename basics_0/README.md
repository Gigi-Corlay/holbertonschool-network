# Network Basics - OSI Model and Networking Concepts

## 📘 OSI Model

The **OSI (Open Systems Interconnection) model** is a conceptual framework used to describe how data is transmitted over a network.

It divides network communication into **7 layers**, from lowest to highest:

1. Physical  
2. Data Link  
3. Network  
4. Transport  
5. Session  
6. Presentation  
7. Application  

### What is the OSI model?

The OSI model is a **conceptual model** that characterizes the communication functions of a telecommunication system without regard to their underlying internal structure and technology.

### How is the OSI model organized?

It is organized **from the lowest to the highest level**.

---

## 🌐 LAN (Local Area Network)

A LAN is a network that connects computers in a small geographical area.

- Typical usage: home, school, office  
- Size: small area (building or campus)

---

## 🌍 WAN (Wide Area Network)

A WAN connects multiple LANs over large distances.

- Typical usage: Internet  
- Size: cities, countries, worldwide  

---

## 🌐 Internet

The Internet is a global network that connects millions of devices worldwide using the TCP/IP protocol.

---

## 🧭 IP Address

An IP address is a unique identifier assigned to a device on a network.

### Types:
- IPv4 (example: 192.168.1.1)
- IPv6 (example: 2001:db8::1)

---

## 🏠 Localhost

Localhost refers to the local machine itself.

- IP address: 127.0.0.1  
- Used for testing network services locally  

---

## 🔀 Subnet

A subnet is a smaller network inside a larger network, used to organize and secure traffic.

---

## 🚀 TCP vs UDP

### TCP (Transmission Control Protocol)
- Reliable
- Connection-oriented
- Slower but safe

### UDP (User Datagram Protocol)
- Fast
- No guarantee of delivery
- Used for streaming, games

---

## 🔌 Common Ports

- SSH: 22  
- HTTP: 80  
- HTTPS: 443  

---

## 📡 Network Testing Tool

The most common tool to check network connectivity is:

- `ping` (uses ICMP protocol)

---

## 🔐 SSH (Secure Shell)

SSH is a secure protocol used to access remote machines.

- Port: 22  
- Uses TCP  
- Secure encrypted communication  

---

## 🧠 Summary

Networking is based on layered communication systems (OSI model), IP addressing, and protocols like TCP/UDP that allow devices to communicate across LANs, WANs, and the Internet.