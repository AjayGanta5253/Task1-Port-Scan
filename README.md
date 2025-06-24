# Task 1: Port Scanning with Nmap – Cyber Security Internship

##  Objective:
The goal of this task was to understand how to identify open ports on a device connected to my local network using Nmap. This helps recognize potential security risks and improve awareness of network exposure.

---

##  Tools I Used:
- **Nmap v7.97** (installed on Windows)
- **Command Prompt (CMD)** to run Nmap commands
- Basic understanding of IP address structure and port numbers

---

##  Device Scanned:
192.168.0.104

This is my local device’s IP address within the home Wi-Fi network.

---

##  Command I Ran:
nmap -sS 192.168.0.104

This command performs a **TCP SYN scan** to detect open ports without completing the full TCP handshake.

---

## Scan Results:

Below is the list of open ports found on my system:

| Port      | State | Service         |
|-----------|-------|------------------|
| 135/tcp   | open  | msrpc            |
| 139/tcp  | open  | netbios-ssn      |
| 445/tcp  | open  | microsoft-ds     |
| 5357/tcp  | open  | wsdapi           |
| 16992/tcp | open  | amt-soap-http    |

>  The full raw scan result is saved in the file: "scan-results.txt"

---

##   Risk Observations:

Here’s what I found about each open port and the possible risks:

| Port | Service        | Risk Description |
|------|----------------|------------------|
 | 135  | msrpc          | May be abused for remote code execution if not firewalled properly. |
 | 139 | netbios-ssn    | Can leak information related to file sharing if file sharing is enabled. |
 | 445  | microsoft-ds   | Frequently targeted by ransomware (e.g., WannaCry); should be blocked externally. |
 | 5357 | wsdapi         | Used by Windows services – not always needed, may expose device info. |
 | 16992| amt-soap-http  | Intel AMT port – should be disabled if Intel AMT remote management is not used. |

---

## What I Learned:

- I learned how to install and run Nmap on Windows.
- I now understand what open ports are and how to identify them.
- I became aware of the risks associated with common services like SMB and RPC.
- This activity gave me a clearer picture of network reconnaissance and how attackers perform port scans to find vulnerabilities.

---

## Files Included in This Task:
- "README.md" – Full explanation of the task and results
- "scan-results.txt" – Actual scan output from Nmap



 *Task Completed Successfully*
