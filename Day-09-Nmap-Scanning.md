# Day 9: Nmap Scanning and Port Enumeration

**Date:** 6 July 2026  
**Topics:** Nmap, TCP Connect Scan, SYN Scan, UDP Scan, TCP Flags, Ports, and Firewall Concepts

## 1. Objective

The objective of this day was to learn how to use Nmap for network scanning, identify open ports, understand TCP and UDP protocols, and explore different scanning techniques used in cybersecurity.

## 2. TryHackMe Practice — Further Nmap

**Room Name:** Further Nmap

**Room Link:** [Open my completed Further Nmap room](https://tryhackme.com/room/furthernmap?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

### What I Learned

- **Nmap:** A network scanning tool used to discover hosts, identify open ports, and examine network services.
- **Port Scanning:** The process of checking ports on a target system to understand which services may be accessible.
- **Nmap Switches:** Command-line options that control how Nmap performs scans.
- **Service Detection:** Identifying services running on discovered ports.
- **Nmap Scripting Engine (NSE):** A feature that uses scripts to perform additional network discovery and security checks.
- **Firewall Concepts:** Firewalls filter network traffic according to security rules and can affect scan results.

### Practical Commands

**Display Nmap help:**

```bash
nmap -h
```

This command displays available options and scanning switches.

**Scan a host for common ports:**

```bash
nmap <target-ip>
```

This command scans a target IP address for common ports.

**Detect service versions:**

```bash
nmap -sV <target-ip>
```

This option attempts to identify services and their versions on discovered ports.

**Save scan results to a text file:**

**nmap -oN scan-results.txt <target-ip>**
This command saves the scan output in a text file.

## 3. TryHackMe Practice — Nmap Basic Port Scans

**Room Name:** Nmap Basic Port Scans (Nmap 02)

**Room Link:** [Open my completed Nmap 02 room](https://tryhackme.com/room/nmap02?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

### What I Learned

I learned about different TCP and UDP port-scanning techniques and how Nmap interprets responses from a target system.

### A. TCP Connect Scan

A TCP Connect Scan attempts to establish a complete TCP connection with the target port.

**Command:**

```bash
nmap -sT <target-ip>
```

It can be useful when a user does not have the privileges required to perform certain raw-packet scans.

### B. TCP SYN Scan

A SYN Scan sends TCP SYN packets and examines the responses without completing the normal TCP three-way handshake.

**Command:**
**sudo nmap -sS <target-ip>**

This scan is commonly used for TCP port discovery when the required privileges are available.

### C. UDP Scan

A UDP Scan checks UDP ports to determine whether services may be listening on them.

**Command:**
**sudo nmap -sU <target-ip>**

UDP scans may take longer because some UDP services do not respond to probes, making port states harder to determine.

## 4. TCP and UDP Ports

A port number helps identify a particular service or application on a device.

## 5. TCP Flags

TCP flags are control bits in TCP headers that help manage network communication.

- **SYN:** Initiates a TCP connection.
- **ACK:** Acknowledges received data or connection messages.
- **FIN:** Indicates that a sender has finished sending data.
- **RST:** Resets a TCP connection.
- **PSH:** Requests that buffered data be delivered promptly to the application.
- **URG:** Indicates that the urgent pointer field is significant.

Understanding TCP flags helps explain how TCP connections are established, maintained, and closed.



## 9. Conclusion

Today, I studied Nmap and practised understanding different port-scanning techniques through TryHackMe. I learned about TCP Connect Scans, SYN Scans, UDP Scans, TCP flags, common ports, and firewall concepts. I also explored Nmap switches for identifying services and saving scan results. This practice improved my understanding of network reconnaissance and basic security assessment.
