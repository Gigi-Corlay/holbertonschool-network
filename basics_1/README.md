# Networking Basics (Linux)

This document explains some basic networking concepts in Linux.

---

# 1. What is localhost / 127.0.0.1

`localhost` refers to your own machine.

- IP address: `127.0.0.1`
- Also called **loopback address**
- Used to communicate with your computer internally (no network required)

## Example

```bash
ping localhost
```
This is equivalent to:
```bash
ping 127.0.0.1
```
**Key idea**
- It never leaves your computer
- Used for testing servers locally

## 2. What is 0.0.0.0

0.0.0.0 is a special IP address meaning:

"All IPv4 addresses on the local machine"

### Common uses
**1. Server binding**

When a server listens on ```0.0.0.0```, it means:

- It accepts connections from **any network interface**


Example:
```bash
python3 -m http.server 8080 --bind 0.0.0.0
```
This makes the server accessible from other machines.

**2. Default/unknown address**
Used when no specific IP is assigned
Represents "no particular address"

## 3. What is /etc/hosts

```/etc/hosts``` is a local file used for name resolution.

It maps domain names to IP addresses manually.

**Example**
```bash
127.0.0.1 localhost
8.8.8.8 facebook.com
```

**How it works**

When you type:
```bash
ping facebook.com

Linux checks:
```

- ```/etc/hosts``` first
- DNS server if not found

**Important**
- Overrides DNS resolution
- Changes apply immediately
- Requires root (sudo) to modify

## 4. How to display your machine's active network interfaces

Network interfaces are hardware/software connections to a network.

**Method 1: ip command (recommended)**
```bash
ip a
```
or
```bash
ip addr show
```

**Example output**
```bash
1: lo: <LOOPBACK>
    inet 127.0.0.1

2: eth0:
    inet 192.168.1.20
```

**Method 2: ifconfig (older tool)**
```bash
ifconfig
```
**⚠️ May not be installed by default on modern systems.**

Install it with:
```bash
sudo apt install net-tools
```

** What to look for**
- lo → loopback interface (localhost)
- eth0 / ens33 → wired network
- wlan0 → Wi-Fi interface
- inet → IPv4 address

## Summary

| Concept     | Description                         |
|------------|-------------------------------------|
| localhost   | Your own machine (127.0.0.1)        |
| 0.0.0.0     | All network interfaces              |
| /etc/hosts  | Local DNS mapping file             |
| ip a        | Show network interfaces            |