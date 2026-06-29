Cyber Security Internship - Task 1
Objective

The objective of this task was to discover open ports on devices connected to the local network and understand network exposure using Nmap.

Tools Used
Nmap
Command Prompt
GitHub
Procedure
1. Installed Nmap

Downloaded and installed Nmap from the official website.

2. Identified Local Network Range

Used the following command:

ipconfig

Obtained the local IPv4 address and identified the network range.

Example:

192.168.1.0/24
3. Performed TCP SYN Scan

Executed:

nmap -sS 192.168.1.0/24
4. Saved Scan Results

Executed:

nmap -sS 192.168.1.0/24 -oN scan_results.txt
5. Analyzed Open Ports

Observed active hosts and open ports available on the local network.

Common Ports and Services
Port	Service
22	SSH
53	DNS
80	HTTP
135	RPC
139	NetBIOS
443	HTTPS
445	SMB
Potential Security Risks
Unauthorized access through exposed services
Vulnerabilities in outdated software
Information disclosure
Malware propagation through open network services
Security Recommendations
Close unnecessary ports
Enable firewall protection
Use strong authentication
Keep software updated
Disable unused services
