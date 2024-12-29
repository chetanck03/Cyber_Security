# Network Scanning for Connected Devices

## Overview
This guide explains the steps to scan a network for connected devices in an ethical hacking context. You will learn how to identify the number of devices connected to a router and retrieve relevant details like domain or public IP address.

### Prerequisites
- Basic understanding of networking.
- A system running Linux (preferably with administrative access).
- Tools: `netdiscover` and basic shell commands.

### Commands and Steps

#### Step 1: Check Network Configuration
To identify your network's details, use the following command:

```bash
ifconfig
```
This command provides information about your:
- IP address
- Subnet mask
- Default gateway

#### Step 2: Scan the Network for Connected Devices
To discover the devices connected to the same network:

1. Run `netdiscover` using the following command:
   ```bash
   sudo netdiscover -i eth0
   ```
   - `-i eth0` specifies the network interface to scan (replace `eth0` with your active network interface if needed).
   - This command lists all devices connected to the router, along with their MAC addresses and IPs.

#### Step 3: Identify the Router or Domain
From the output, identify the router's IP address (default gateway) or domain information.

#### Step 4: Test Connectivity
To test the connection with a specific device (e.g., the router):

1. Use the `ping` command:
   ```bash
   ping 192.168.66.1
   ```
   Replace `192.168.66.1` with the IP address of the target device.
   - This command sends ICMP echo requests to the target to verify its reachability and measure response time.

### Example Workflow
1. Run `ipconfig` to find your network's details.
2. Use `sudo netdiscover -i eth0` to scan for devices on the network.
3. Identify the router's IP from the output.
4. Execute `ping 192.168.66.1` to test the connection with the router.

### Important Notes
- Always ensure you have proper authorization before scanning any network.
- Use these commands responsibly and ethically.

### References
- [netdiscover Documentation](https://github.com/alexxy/netdiscover)
- [Ping Command Manual](https://linux.die.net/man/8/ping)

---
This document is for educational purposes only. Unauthorized use of these techniques is prohibited.
