# Cyber Security Internship - Task 1

## Scan Your Local Network for Open Ports

### Objective
The objective of this task was to perform a TCP SYN scan on the local network using Nmap to identify active hosts, discover open ports, understand the services running on those ports, and analyze potential security risks.

---

## Tools Used

- Nmap
- Windows Command Prompt
- GitHub

---

## Procedure

### Step 1: Installed Nmap
Downloaded and installed Nmap from the official website.

### Step 2: Identified Local Network Range
Used the following command:

```cmd
ipconfig
```

The local network range was identified and **masked** for privacy.

Example:

```text
192.168.x.0/24
```

### Step 3: Performed TCP SYN Scan

Executed the following command:

```cmd
nmap -sS 192.168.x.0/24
```

### Step 4: Saved Scan Results

```cmd
nmap -sS 192.168.x.0/24 -oN scan_results.txt
```

### Step 5: Analyzed Results

The scan identified active hosts and their open TCP ports within the local network.

---

# Sample Masked Scan Output

```text
Starting Nmap 7.xx

Nmap scan report for 192.168.x.1
Host is up.

PORT      STATE SERVICE
53/tcp    open  domain
80/tcp    open  http
443/tcp   open  https

Nmap scan report for 192.168.x.10
Host is up.

PORT      STATE SERVICE
135/tcp   open  msrpc
139/tcp   open  netbios-ssn
445/tcp   open  microsoft-ds
```

---

# Common Ports and Services

| Port | Service | Description |
|------|----------|-------------|
| 22 | SSH | Secure Remote Login |
| 53 | DNS | Domain Name Service |
| 80 | HTTP | Web Server |
| 135 | RPC | Windows Remote Procedure Call |
| 139 | NetBIOS | Windows File Sharing |
| 443 | HTTPS | Secure Web Traffic |
| 445 | SMB | Windows File Sharing |

---

# Potential Security Risks

- Unauthorized access through exposed services.
- Exploitation of outdated or vulnerable applications.
- Information disclosure.
- Malware propagation across the network.
- Increased attack surface.

---

# Security Recommendations

- Close unnecessary ports.
- Enable and configure firewalls.
- Keep operating systems and software updated.
- Disable unused services.
- Use strong passwords and authentication.
- Monitor network activity regularly.

---

# Interview Questions

### 1. What is an open port?

An open port is a network communication endpoint that is actively accepting incoming connections.

### 2. How does Nmap perform a TCP SYN scan?

Nmap sends a SYN packet to a target port. If the target responds with a SYN-ACK packet, the port is considered open. Nmap then sends an RST packet instead of completing the connection.

### 3. What risks are associated with open ports?

Open ports can expose services that attackers may exploit to gain unauthorized access or gather information.

### 4. Explain the difference between TCP and UDP scanning.

TCP scanning checks connection-oriented services, while UDP scanning checks connectionless services and is generally slower due to the lack of acknowledgements.

### 5. How can open ports be secured?

Unused ports should be closed, firewalls should be configured properly, unnecessary services should be disabled, and systems should be kept updated.

### 6. What is a firewall's role regarding ports?

A firewall controls incoming and outgoing network traffic by allowing or blocking access to specific ports based on security rules.

### 7. What is a port scan and why do attackers perform it?

A port scan is the process of identifying open ports and services on a device. Attackers use port scanning to discover potential vulnerabilities and entry points.

### 8. How does Wireshark complement port scanning?

Wireshark captures and analyzes network packets, allowing users to inspect traffic generated during port scans and troubleshoot network communication.

---

# Outcome

Successfully performed a TCP SYN scan using Nmap, identified active hosts and open ports, understood the services running on those ports, and gained practical knowledge of network reconnaissance and basic network security.

> **Note:** Local IP addresses have been masked to protect network privacy.
