# Exfiltration (TA0010)

## Exfiltration with <mark style="color:red;">Dnscat2</mark>

This tool is designed to create an encrypted command-and-control (C\&C) channel over the DNS protocol, which is an effective tunnel out of almost every network.

Available on GitHub: https://github.com/iagox86/dnscat2

### MITRE ATT\&CK Tactics

#### Command & Control

* T1071: Application Layer Protocol
  * T1071.004: DNS

#### Exfiltration

* T1048: Exfiltration Over Alternative Protocol
  * T1048.001: Exfiltration Over Symmetric Encrypted Non-C2 Protocol

### Basic Commands for Dnscat

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Common Issues

* Due to firewall restrictions, individual clients may be blocked
* This can be detected by monitoring clients for increased DNS traffic

### Establishing a DNS Tunnel

* Requires a publicly registered domain name
* Dnscat server will act as the authoritative DNS server

### Avoiding Detection

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### More Information

Dnscat2 documentation https://github.com/iagox86/dnscat2/tre e/master/doc

Authoritative DNS server setup https://github.com/iagox86/dnscat2/bl ob/master/doc/authoritative\_dns\_setup .md

Dnscat2 PowerShell Client https://github.com/lukebaggett/dnscat 2-powershell



## Exfiltration with <mark style="color:red;">CloakifyFactory</mark>

CloakifyFactory transforms any file type (e.g. .zip, .exe, .xls, etc.) into a list of harmless-looking strings. This lets you hide the file in plain sight and transfer the file without triggering alerts.

Available on https://github.com/TryCatchHCF/Cloakify

### MITRE ATT\&CK Tactics

#### Exfiltration

* T1041: Exfiltration over C2
* T1567.002: Exfiltration over Web Service
* T1048.001: Exfiltration over alternative protocol

### More Information

Defcon 24 https://github.com/TryCatchHCF/Cloa kify/blob/master/DefCon24Slides/Def Con24\_Cloakify\_Exfiltration\_Toolset.pd f



## Exfiltration with <mark style="color:red;">Powershell-RAT</mark>

There is a tool that can be used as a backdoor to monitor a user's activity, by taking screenshots and sending them via email to the attacker. This tool is written in Python and is used after a system has been exploited. The attacker has to find a way to install it on the victim's computer so that it can periodically send screenshots to a Gmail account. PowerShell is heavily used in this type of attack, as it can be used to carry out data breaches, take screenshots, create scheduled tasks, and send emails. Attackers and Red Team members often use PowerShell for attacks and penetration testing, as it can interact with many components of the operating system. The Python script is usually the first step in executing this type of attack.

### Techniques

* T1113 - Screen Capture
* T1053.005 - Scheduled, Task/Job: Scheduled Task
* T1020 - Automated Exfiltration
* T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol

### Prerequisites

Python needs to be installed on the system.

Gmail account to send and receive emails.

### More Information

Powershell RAT https://github.com/Viralmaniar/Powers hell-RAT/blob/master/README.md

PyInstaller https://github.com/pyinstaller/pyinstall er/blob/develop/README.rst

