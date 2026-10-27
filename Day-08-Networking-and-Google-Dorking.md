# Day 8: Networking, Google Dorking and Nmap

**Date:** 4 July 2026

## 1. Objective

The objective of this day was to understand networking fundamentals, learn how search engines collect information, practise advanced Google search techniques, and explore Nmap scanning methods used in cybersecurity.

## 2. TryHackMe Practice — Introduction to Networking

**Room Name:** Introduction to Networking

**Room Link:** [Open my completed Introduction to Networking room](https://tryhackme.com/room/introtonetworking?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

### What I Learned

- **Networking:** How computers and other devices communicate and exchange data.
- **IP Address:** A logical address used to identify a device on an IP network.
- **MAC Address:** An address used to identify a network interface on a local network.
- **TCP:** A connection-oriented protocol that provides reliable data delivery.
- **UDP:** A connectionless protocol with lower communication overhead.
- **OSI Model:** A seven-layer model that helps explain network communication.
- **TCP/IP Model:** A model describing the main layers used for communication over the internet.

### Practical Commands

**Check network connectivity:**

```bash
ping example.com
```

**Check DNS information:**

```bash
dig example.com
```

These commands help me understand basic connectivity and domain name resolution.

## 3. TryHackMe Practice — Google Dorking

**Room Name:** Google Dorking

**Room Link:** [Open my completed Google Dorking room](https://tryhackme.com/room/googledorking?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=6a3cc3f57ef3044a2b1dff1e)

### What I Learned

**1. Search Engine Crawlers**

Crawlers are automated programs that discover web pages and collect information so search engines can index them.

**2. Search Engine Optimisation (SEO)**

SEO involves improving a website's visibility in search engine results.

**3. Robots.txt**

The `robots.txt` file provides instructions to web crawlers about which parts of a website they should or should not crawl.

Important terms include:

- `User-agent`: Specifies which crawler a rule applies to.
- `Allow`: Indicates a path that a crawler may crawl.
- `Disallow`: Indicates a path that a crawler is asked not to crawl.
- `Sitemap`: Identifies the location of a website's sitemap.

**4. Google Dorking**

Google Dorking uses advanced search operators to find specific information indexed by search engines.

Common operators include:

- `site:` — Searches within a particular website or domain.
- `filetype:` — Searches for specific file types.
- `intitle:` — Searches for words in page titles.
- Quotation marks — Search for an exact phrase.

### Practical Examples

Search within a website:

```text
site:example.com
```

Search for PDF files on a website:

```text
site:example.com filetype:pdf
```

Search for an exact phrase:

```text
"network security"
```

I learned how these operators make information gathering more efficient. I also understood the importance of using search techniques responsibly.

## 4. Introduction to Nmap

Nmap is a network scanning tool used to discover hosts, identify open ports, and investigate network services.

### Nmap Scan Types

**1. TCP Connect Scan**

This scan attempts to establish a complete TCP connection to determine whether a port is open.

```bash
nmap -sT 192.168.1.1
```

**2. SYN Scan**

This scan sends TCP SYN packets and examines responses to identify port states. It is commonly called a half-open scan.

```bash
sudo nmap -sS 192.168.1.1
```

**3. UDP Scan**

This scan checks UDP ports to determine their states.

```bash
sudo nmap -sU 192.168.1.1
```

These examples should be used only on systems and networks where scanning is authorised.

## 5. TCP and UDP Ports

Ports help identify the services running on a device.

- **TCP ports:** Used by services that communicate over TCP.
- **UDP ports:** Used by services that communicate over UDP.

Examples of common ports:

| Port | Protocol | Common Service |
|---|---|---|
| 22 | TCP | SSH |
| 53 | TCP/UDP | DNS |
| 80 | TCP | HTTP |
| 443 | TCP | HTTPS |

## 6. TCP Flags

TCP flags help control communication between devices.

- **SYN:** Initiates a TCP connection.
- **ACK:** Acknowledges received data or connection messages.
- **FIN:** Indicates that a sender wants to close a TCP connection.
- **RST:** Resets a connection.
- **PSH:** Requests that buffered data be pushed to the receiving application.
- **URG:** Indicates that the urgent pointer field is significant.

Understanding TCP flags helps explain how connections are established, maintained, and closed.

## 7. Nmap Scripts and Firewall Concepts

Nmap supports scripts that can gather additional information about network services and help identify potential security issues.

I learned that firewalls control network traffic according to security rules. Different scanning methods can produce different results depending on firewall rules and network configurations.

Network scanning and script testing should always be performed with proper authorisation.

## 8. Key Takeaways

- Networking concepts explain how devices communicate.
- The OSI and TCP/IP models help explain network communication.
- Google Dorking uses advanced search operators for targeted information gathering.
- Crawlers, SEO, `robots.txt`, and sitemaps are important concepts in web searching.
- Nmap helps identify hosts, open ports, and network services.
- TCP and UDP use different communication methods.
- TCP flags help manage network connections.
- Ethical and authorised testing is essential in cybersecurity.

## 9. Conclusion

Today, I studied networking fundamentals and completed TryHackMe activities related to networking and Google Dorking. I also learned about Nmap scanning methods, TCP and UDP ports, TCP flags, and the role of firewalls. These topics helped improve my understanding of network reconnaissance and cybersecurity investigation.
