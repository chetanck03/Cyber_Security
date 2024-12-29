# Metasploitable 2

Metasploitable 2 is a vulnerable Linux virtual machine designed for testing and learning about penetration testing, ethical hacking, and security vulnerabilities. It provides a controlled environment to practice using security tools like Metasploit without harming live systems.

---

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Download and Setup](#download-and-setup)
- [Default Login Credentials](#default-login-credentials)
- [Common Vulnerabilities](#common-vulnerabilities)
- [Usage Instructions](#usage-instructions)
- [Disclaimer](#disclaimer)

---

## Introduction
Metasploitable 2 is a deliberately vulnerable VM maintained by Rapid7 to help users gain hands-on experience with penetration testing tools and techniques. It is ideal for beginners looking to explore security testing in a safe and legal environment.

---

## Features
- Pre-configured services with known vulnerabilities.
- Supports a variety of common exploits and attack scenarios.
- Designed for use with the Metasploit Framework.
- Suitable for practicing web application, network, and database exploitation.

---

## Download and Setup
1. Download the Metasploitable 2 virtual machine from the [official website](https://sourceforge.net/projects/metasploitable/).
2. Extract the downloaded file.
3. Open the extracted `.vmdk` file in a virtualization tool like VMware or VirtualBox.
4. Start the VM and access it through the terminal or an SSH client.

---

## Default Login Credentials
The default credentials for Metasploitable 2 are as follows:

- **Username**: `msfadmin`
- **Password**: `msfadmin`

*Note*: Change these credentials only if necessary, as the default configuration is intended for security testing.

---

## Common Vulnerabilities
Metasploitable 2 includes several known vulnerabilities across various services, including:

- **FTP**: Anonymous login enabled (vsftpd backdoor vulnerability).
- **SSH**: Weak configurations and outdated software.
- **Apache Tomcat**: Default credentials and deployment vulnerabilities.
- **MySQL**: Weak passwords.
- **PHP**: Remote code execution vulnerabilities.
- **Web Applications**:
  - Mutillidae: OWASP Top 10 vulnerabilities.
  - DVWA (Damn Vulnerable Web Application): SQL injection, XSS, CSRF, etc.
- **Other Services**:
  - Samba: Misconfigured shares.
  - NFS: Insecure exports.
  - Postgres: Default credentials.

---

## Usage Instructions
1. Start the VM in your virtualization tool.
2. Scan the Metasploitable 2 VM using tools like `nmap` to identify open ports and services.
3. Use the Metasploit Framework to exploit vulnerabilities. For example:
   ```bash
   msfconsole
   use exploit/unix/ftp/vsftpd_234_backdoor
   set RHOST <Metasploitable IP>
   run
   ```
4. Experiment with other tools and techniques to explore and understand the vulnerabilities.

---

## Disclaimer
Metasploitable 2 is intended for educational purposes only. It should only be used in a controlled environment, such as a local network or an isolated lab. Misusing Metasploitable 2 in a live environment is unethical and may violate laws.

---

## Resources
- [Official Metasploit Documentation](https://www.metasploit.com/)
- [Metasploitable 2 Walkthroughs and Guides](https://www.offensive-security.com/)
- [OWASP](https://owasp.org/)

---

Happy Learning!
