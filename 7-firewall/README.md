# Firewalls

A firewall is a network security device or software that monitors and controls incoming and outgoing network traffic based on predefined security rules.

## Why Do We Need Firewalls?

- Prevent unauthorized access.
- Protect systems from cyber attacks.
- Filter malicious traffic.
- Control network communication.
- Improve overall security posture.

## Types of Firewalls

### 1. Packet Filtering Firewall
- Inspects packets based on IP addresses, ports, and protocols.
- Fast and lightweight.

### 2. Stateful Firewall
- Keeps track of active connections.
- Allows only legitimate traffic.

### 3. Proxy Firewall
- Acts as an intermediary between users and servers.
- Provides additional security and anonymity.

### 4. Next-Generation Firewall (NGFW)
- Includes IDS/IPS, application awareness, and deep packet inspection.
- Commonly used in enterprises.

### 5. Web Application Firewall (WAF)
- Protects web applications from attacks like SQL Injection and XSS.

## Firewall Rules

| Rule | Action |
|------|--------|
| Allow Port 22 | SSH Access |
| Allow Port 80 | HTTP Traffic |
| Allow Port 443 | HTTPS Traffic |
| Deny Port 23 | Block Telnet |
| Allow ICMP | Ping Requests |

## Real-World Example

Imagine a company server:

- Allow SSH (22) only from office IP.
- Allow HTTP (80) for websites.
- Allow HTTPS (443) for secure communication.
- Block all other unnecessary ports.

## Linux Firewall Commands

### UFW (Ubuntu)

```bash
sudo ufw status
sudo ufw enable
sudo ufw allow 22
sudo ufw allow 80
sudo ufw allow 443
sudo ufw deny 23
```
