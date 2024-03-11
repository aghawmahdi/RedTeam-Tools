# Collection (TA0009)

## Collection with <mark style="color:red;">PowerSploit</mark>

PowerSploit is a collection of Microsoft PowerShell modules that can be used to aid penetration testers during all phases of an assessment.

Open source tool (GNU v3.0) https://github.com/PowerShellMafia/PowerSploit

Already comes in most Command and Control tools

* Covenant, Pupy, etc.&#x20;

Automate collection of sensitive data

* Sensitive files
* Microphone audio
* Screenshots
* Keylogger

### MITRE ATT\&CK Tactics

#### Collection

* T1123: Audio Capture
* T1056: Input Capture
* T1113: Screen Capture
* T1039: Data from Network Shared Drive

### Anti-Virus Detection

#### Anti-Virus Bypassing

* Several techniques
* Script obfuscation
  * Course: “Defense Evasion with Invoke-Obfuscation”
* Always test in a cloned environment
* The preferred method usually does not generate logs

#### Anti-Virus Disabling

* Easiest way
* Disabling all detection mechanisms
  * Anti-virus and HIPS
  * Endpoint protection
  * Windows defender
* Usually generate logs to SIEM
* Suspicious activity

### Other PowerSploit Features

* Reconnaissance
* Code Execution
* Privilege Escalation
* Persistence
* Anti-virus Bypass
* Exfiltration
* Covers 23 tactics from the Mitre Att\&ck Framework

### More Information

Several other capabilities https://github.com/PowerShellMafia/ PowerSploit



## Collection with <mark style="color:red;">PowerUpSQL</mark>

PowerUpSQL includes functions that support SQL Server discovery, weak configuration auditing, privilege escalation on the scale, and post-exploitation actions such as OS command execution.

Open source tool https://github.com/NetSPI/PowerUpSQL&#x20;

#### Full framework for MS SQL auditing

* Reconnaissance, initial access, privilege escalation, collection, etc.&#x20;

#### Automate collection of sensitive data

* Find sensitive data
* Find credit card information
* Dump databases

### MITRE ATT\&CK Tactics

#### Initial Access

* T1078: Valid Accounts

#### Collection

* T1005: Data From Local System

#### Impact

* T1485: Data Destruction
* T1565.001: Stored Data Manipulation

### Other PowerUpSQL Features

* Discovery
* Initial Access
* Insecure Configurations
* Privilege Escalation
* Persistence
* Exfiltration

{% embed url="https://github.com/NetSPI/PowerUpSQL/wiki/PowerUpSQL-Cheat-Sheet" %}

### More Information

Several other capabilities https://github.com/NetSPI /PowerUpSQL/wiki

BlackHat 2018 https://www.youtube.com/ watch?v=UX\_tBJQtqW0

