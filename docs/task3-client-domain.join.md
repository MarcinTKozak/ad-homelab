# Task 3 – Client Configuration and Domain Join

## Objective
Configure the client machine network settings and join it to the Active Directory domain.

## Environment
- Client OS: Windows 11
- Client Name: CLIENT01
- Domain Controller: DC01
- Domain Name: lab.local

---

## Tasks completed

### 1. DNS configuration on CLIENT01
Configured the client to use the domain controller as its DNS server.

Steps:
- Opened network adapter settings
- Edited IPv4 configuration
- Set Preferred DNS server to the IP address of DC01

Configuration:
- Preferred DNS server: `192.168.56.10`
- Alternate DNS server: not configured

> Note: Correct DNS configuration is required for successful domain join.

---

### 2. Joining CLIENT01 to the domain
Joined the client machine to the Active Directory domain.

Steps:
- Opened system settings
- Changed computer membership to Domain
- Entered domain name: `lab.local`
- Authenticated using domain administrator credentials

Result:
- Received confirmation message: *Welcome to the lab.local domain*

---

### 3. System restart
- Restarted the client machine to apply domain membership changes

---

### 4. Domain user login verification
Verified successful domain join by logging in with a domain user account:

- `LAB\kowalskij`
- `kowalskij@lab.local`

---

## Result
CLIENT01 is successfully joined to the Active Directory domain and can authenticate domain users.

## Notes
- DNS misconfiguration is the most common cause of domain join failure
- Client machines must use the domain controller as their primary DNS server
