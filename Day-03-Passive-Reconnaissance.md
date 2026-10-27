# Day 3: Passive Reconnaissance

**Date:** 27 June 2026  
**Platform:** TryHackMe  
**Room:** Passive Reconnaissance  
**Room Link:**[TryHackMe — Passive Reconnaissance](https://tryhackme.com/room/passiverecon)
## 1. Introduction

On Day 3 of my cybersecurity training, I learned about passive reconnaissance. It is the process of gathering information about a target from publicly available sources without directly probing the target's systems.

Passive reconnaissance helps cybersecurity professionals understand domain information, DNS records, and publicly visible internet infrastructure.

## 2. Tools and Commands

### A. WHOIS

WHOIS is used to retrieve publicly available domain registration information.

**Command:**
```bash
whois example.com
```

**Purpose:**  
- Find the domain registrar.
- Check registration dates when available.
- View name server information.

### B. NSLOOKUP

`nslookup` is a command-line tool used to query DNS records.

**Command:**
```bash
nslookup example.com
```

**Purpose:**  
- Find IP addresses associated with a domain.
- Query DNS servers.
- Understand how domain names resolve to IP addresses.

### C. DIG

`dig` stands for Domain Information Groper. It is used to query DNS records.

**Command:**
```bash
dig example.com
```

To query a specific record type:

```bash
dig example.com MX
dig example.com NS
dig example.com TXT
```

**Purpose:**  
- `A`: Find IPv4 address records.
- `MX`: View mail server records.
- `NS`: View name server records.
- `TXT`: View publicly available text records.

### D. DNSDumpster

DNSDumpster is an online tool used to research publicly available DNS information about a domain.

**Website:** https://dnsdumpster.com/

**Practical Steps:**
1. Open DNSDumpster.
2. Enter a domain you are authorized to research.
3. Review the publicly available DNS information.
4. Observe any listed subdomains and related infrastructure.

### E. Shodan

Shodan is a search engine for internet-connected devices and services.

**Website:** https://www.shodan.io/

**Practical Steps:**
1. Open Shodan.
2. Search for a publicly documented service or device type.
3. Review the information displayed in the results.
4. Learn how internet-connected services may be exposed.

Use Shodan responsibly and do not attempt to access or test systems without permission.

## 3. Practical Command-Line Exercise

The following commands demonstrate basic domain and DNS information gathering using `example.com`, a domain reserved for documentation and examples.

```bash
# Check publicly available domain registration information
whois example.com

# Look up domain information
nslookup example.com

# Query general DNS records
dig example.com

# Query IPv4 address records
dig example.com A

# Query mail server records
dig example.com MX
