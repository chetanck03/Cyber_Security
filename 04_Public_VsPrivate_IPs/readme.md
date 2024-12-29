# Public vs Private IPs

## Overview
This guide explains the difference between public and private IP addresses and demonstrates how to perform a basic penetration test to gather information about a website's IP address using various commands.

### What are IP Addresses?
An IP address (Internet Protocol address) is a unique identifier assigned to a device on a network. IP addresses are classified into two types:

#### Private IP Addresses
- **Purpose**: Used within private networks (e.g., home, office LAN).
- **Scope**: Not accessible directly from the internet.
- **Examples**:
  - `192.168.x.x`
  - `10.x.x.x`
  - `172.16.x.x` to `172.31.x.x`

#### Public IP Addresses
- **Purpose**: Used to identify devices on the internet.
- **Scope**: Globally unique and accessible from anywhere.
- **Example**: `8.8.8.8` (Google's public DNS server).

### Commands for Website Penetration Testing

#### Step 1: Identify the Website's IP Address
Use the `whatweb` command to gather information about a website and retrieve its IP address.

```bash
whatweb nmap.org
```
This command scans the website for its details, including its IP address and web server information.

#### Step 2: Test Connectivity
Once you have the IP address, use the `ping` command to verify connectivity:

```bash
ping <ip-address>
```
Replace `<ip-address>` with the IP retrieved in the previous step. This command sends ICMP echo requests to check if the IP address is reachable.

#### Step 3: Scan for Open Ports and Services
To gather more details about the website's network and open ports, use `nmap`:

```bash
nmap nmap.org
```
This command performs a network scan to identify open ports, services, and potential vulnerabilities.

### Example Workflow
1. Run `whatweb nmap.org` to find the website's IP address and other information.
2. Use `ping <ip-address>` to verify connectivity with the target.
3. Execute `nmap nmap.org` to scan for open ports and running services.

### Notes
- Always ensure you have authorization to perform penetration testing on a website.
- Unauthorized scanning of networks or websites may be illegal.

### References
- [WhatWeb Documentation](https://github.com/urbanadventurer/WhatWeb)
- [Nmap Documentation](https://nmap.org/book/)

---
This document is for educational purposes only. Use these commands responsibly and ethically.
