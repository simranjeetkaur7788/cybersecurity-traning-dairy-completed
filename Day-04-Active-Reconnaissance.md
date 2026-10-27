# Day 4: Active Reconnaissance

**Date:** 29 June 2026  
**Training Platform:** TryHackMe  
**Topic:** Active Reconnaissance
**Room Link:** [Open Active Reconnaissance on TryHackMe](https://tryhackme.com/room/activerecon)
## 1. Introduction

On Day 4 of my cybersecurity training, I learned about active reconnaissance. It involves gathering information by directly interacting with a target system or network.

Active reconnaissance helps cybersecurity professionals understand network connectivity, identify reachable services, and observe how systems respond to network requests.

All practical testing should be performed only on authorized systems or within the assigned TryHackMe lab.

## 2. Tools and Commands Learned

### A. Ping

The `ping` command is used to test network connectivity by sending ICMP Echo Request packets and checking for replies.

**Command:**
```bash
ping -c 4 example.com
```

**What I learned:**
- How to check whether a host responds to network requests.
- How to observe response time.
- How to understand packet loss.

A host may block ping requests, so no reply does not always mean the host is offline.

### B. Traceroute

The `traceroute` command helps identify the network hops between a computer and a destination.

**Command on Linux:**
```bash
traceroute example.com
```

**Command on Windows:**
```cmd
tracert example.com
```

**What I learned:**
- How network packets travel through routers.
- How to observe intermediate hops.
- How to understand delays along a network path.

### C. Telnet

Telnet can establish a TCP connection to a specified host and port. It can also help demonstrate how network services respond.

**Command:**
```bash
telnet example.com 80
```

**What I learned:**
- How to attempt a connection to a TCP port.
- How network services communicate.
- Why Telnet is not suitable for transmitting sensitive information because it does not encrypt communication.

### D. Netcat

Netcat, commonly called `nc`, is a networking utility that can establish TCP connections and test service connectivity.

**Command:**
```bash
nc -vz example.com 80
```

**What I learned:**
- How to test whether a TCP port is reachable.
- How to understand basic network connections.
- How network utilities help with troubleshooting and security assessments.

## 3. Practical Learning

During this session, I explored active reconnaissance using the TryHackMe learning environment.

My activities included:

- Learning the difference between passive and active reconnaissance.
- Exploring Ping for connectivity testing.
- Learning how Traceroute identifies network hops.
- Exploring Telnet and TCP connections.
- Learning how Netcat can test network connectivity.
- Understanding why active reconnaissance requires authorization.

## 4. Difference Between Passive and Active Reconnaissance

| Passive Reconnaissance | Active Reconnaissance |
|---|---|
| Collects information from public sources. | Interacts directly with a target. |
| Usually avoids sending probes directly to the target. | May generate detectable network traffic. |
| Examples include public WHOIS research and DNS information gathering. | Examples include Ping, Traceroute, and authorized port-connectivity tests. |

## 5. What I Learned

- The basic concept of active reconnaissance.
- How to test network connectivity using Ping.
- How to trace a network path using Traceroute.
- How Telnet and Netcat work with TCP connections.
- How active reconnaissance differs from passive reconnaissance.
- Why ethical and authorized testing is important in cybersecurity.

