# Day 7: Introduction to LAN

**Date:** 3 July 2026  
**Topic:** Local Area Network (LAN)

## 1. Objective

The objective of this day was to understand Local Area Networks (LANs), how devices communicate within a network, and the basic concepts of network connectivity.

## 2. TryHackMe Practice

**Room Name:** Introduction to LAN

**Room Link:** [Open my completed Introduction to LAN room](https://tryhackme.com/room/introtolan?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

I completed this room to learn how devices connect and communicate within a local network.

## 3. What I Learned

### A. Local Area Network (LAN)

A LAN is a network that connects devices within a limited geographical area, such as a home, office, college, or computer laboratory.

**Examples:**
- Computers connected in a college laboratory.
- Devices connected to the same home Wi-Fi network.
- Computers sharing resources in an office.

### B. Network Devices

**1. Switch**

A switch connects devices within a LAN and forwards data to the appropriate device using MAC addresses.

**2. Router**

A router connects different networks and forwards data between them. It commonly connects a home or college network to the internet.

**3. Computer and Server**

Computers and servers communicate over networks to exchange data and access resources.

### C. IP Address

An IP address is a logical address used to identify a device on an IP network.

Example: `192.168.1.10`

IP addresses help devices communicate with one another.

### D. MAC Address

A MAC address identifies a network interface at the data link layer. It is used in local network communication.

An IP address and a MAC address have different purposes.

### E. Network Topology

Network topology describes how devices are arranged and connected in a network.

Common topologies include:

- **Star topology:** Devices connect to a central switch or hub.
- **Bus topology:** Devices share a common communication line.
- **Ring topology:** Devices form a circular connection.
- **Mesh topology:** Devices have multiple connections to one another.

Star topology is commonly used in modern LANs.

## 4. Practical Commands

### A. Check Network Connectivity

```bash
ping 192.168.1.1
```

This command sends requests to the specified IP address to check connectivity and response time. The address is an example and should be replaced with the correct address for your network.

### B. Display IP Configuration on Windows

```cmd
ipconfig
```

This command displays network configuration details, including IP addresses and default gateways.

### C. Display IP Configuration on Linux

```bash
ip addr
```

This command displays information about network interfaces and their IP addresses.

## 5. Understanding LAN Communication

When one computer sends data to another computer on the same local network, it uses network addressing and local delivery mechanisms to communicate.

For example, computers connected to the same college network can communicate with other devices and access shared resources, depending on the network configuration and security permissions.

A switch forwards Ethernet frames within the LAN, while a router forwards packets between different IP networks.

## 6. Key Takeaways

- LAN stands for Local Area Network.
- A LAN connects devices within a limited geographical area.
- Switches connect devices within a LAN.
- Routers connect different networks.
- IP addresses are used for logical addressing.
- MAC addresses are used for communication over local links.
- Network topology describes the arrangement of network devices.
- Ping helps check network connectivity.

## 7. Conclusion

Today, I learned the fundamentals of Local Area Networks, network devices, IP and MAC addresses, and network topologies. I also practised basic networking commands to understand connectivity and network configuration. This knowledge provides a foundation for learning network security and ethical hacking.
