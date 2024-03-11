# Initial Access (TA0001)

## Initial Access with <mark style="color:red;">Aircrack-ng</mark>

A complete suite of tools to assess WiFi network security. Used for monitoring, attacking, testing, and cracking wireless networks.

### MITRE ATT\&CK Tactics

* Initial Access
  * T1465: WiFi Access Points
* Credential Access
  * T1110: Brute Force (WPA2)
* Impact
  * T1464: Denial of Service

### More Information

Several other capabilities, such as packet replays, fake access points, and much more: [https://www.aircrack-ng.org/](https://www.aircrack-ng.org/)

WPA2 Password Lists: [https://www.wirelesshack.org/wpawpa2-word-list-dictionaries.html](https://www.wirelesshack.org/wpawpa2-word-list-dictionaries.html)



### Initial Access with <mark style="color:red;">Luckystrike</mark>

Generating a malicious macro doc is something that every pentester is well acquainted with. Malicious macros are used all the time to gain footholds when other attacks don't work. Lucky Strike attempts to automate as much as possible, allows for payload reuse, and includes as many built-in AV evasion techniques as possible.

### MITRE ATT\&CK Tactics

* Initial Access
  * T1193: Spearphishing Attachments

### More Information

Framework and resources:&#x20;

[https://github.com/curi0usJack/luckyst\
rike\
https://github.com/danielbohannon/Inv\
oke-Obfuscation](https://github.com/curi0usJack/luckystrikehttps://github.com/danielbohannon/Invoke-Obfuscation)

{% embed url="https://github.com/trustedsec/unicornhttps://github.com/rapid7/Metasploitframework/wiki" %}



### Initial Access with <mark style="color:red;">WiFi-Pumpkin</mark>

A rogue access point framework to easily create fake WiFi networks. Includes several modules, such as transparent proxy, ARP poisoning, phishing manager, and much more.

Includes several attacks out of the box

* Packet injection
* HTTP credential monitoring
* ARP poisoning and DNS spoofing
* Fake captive portals

Open source tool (GNU v3.0) https://github.com/P0cL4bs/WiFi-Pumpkin

### MITRE ATT\&CK Tactics

* Initial Access
  * T1465: Rogue WiFi Access Points
  * T1078: Valid Accounts

### How to Increase Your Success Rate

Use a convincing WiFi SSID

* “Globomantics Corporate Secure”
* “Globomantics Employees” Generate a failed authentication
* Edit the template JavaScript Cause DoS (if authorized)
* Use Aireplay-ng
* aireplay-ng --deauth 0 -a \[real\_ap\_mac] -c \[victm\_mac] wlan0mon

### More Information

#### Official Documentation&#x20;

Several other capabilities include WiFi Proxy, SSL decryption, image capture, credential capture, and more: https://github.com/P0cL4bs/WiFi-Pumpkin

#### DoS tool

Aircrack-ng: https://www.aircrack-ng.org/



### Initial Access with <mark style="color:red;">Gophish</mark>

Gophish is an open-source phishing toolkit that can be used by businesses and penetration testers to quickly set up and execute phishing campaigns. Gophish is a phishing toolkit to test an organization’s security awareness. It can be downloaded from www.getgophish.com or on GitHub. Gophish is useful due to its simplicity of installation and operation.

### MITRE ATT\&CK Tactics

* Initial Access
  * T1566: Phishing
  * T1566.001: Spearphishing Attachment
  * T1566.002: Spearphishing Link

Gophish user guide: https://docs.getgophish.com/userguide/

Automation and API documentation: https://getgophish.com/documentation

MITRE ATT\&CK initial access: https://attack.mitre.org/tactics/TA0001/



### Initial Access with <mark style="color:red;">sqlmap</mark>

Used to automate the process of detecting and exploiting SQL injection flaws. Powerful detection engine for database fingerprinting, data exfiltration, and underlying operating system access.

Scan a website to identify SQL Injection vulnerabilities, Exploit an identified vulnerability to enumerate data, Use the level and risk parameters for tuning scans, and Gain remote server access using SQLmap.

### What can we do using sqlmap:

* Scan a website to identify SQL Injection vulnerabilities&#x20;
* Exploit an identified vulnerability to enumerate data&#x20;
* Use the level and risk parameters for tuning scans&#x20;
* Gain remote server access using sqlmap

Available for download at:

&#x20;http://sqlmap.org/&#x20;

github.com/sqlmapproject/sqlmap

github.com/sqlmapproject/sqlmap/wiki/Usage

### MITRE ATT\&CK Tactics

* Initial Access
  * T1190: Exploit Public Facing Application



### Initial Access with <mark style="color:red;">King Phisher</mark>

Tooling for building complex phishing attack scenarios as well as coordinating and monitoring successful phishing campaigns. Created for testing and promoting user awareness by simulating real-world phishing attacks.

Available from the king-phisher GitHub repository: https://github.com/rsmusllp/kingphisher

Template Repository https://github.com/rsmusllp/kingphisher-templates

Reporting Functionality https://github.com/rsmusllp/kingphisher/wiki/Graphs | https://github.com/rsmusllp/kingphisher/wiki/SMS-Phishing

### MITRE ATT\&CK Tactics

* Initial Access
  * T1078: Valid Accounts
  * T1566: Phishing
    * T1566.002 Spearphishing Link
    * T1566.003 Spearphishing via Service



### Initial Access with <mark style="color:red;">Bash Bunny</mark>

The Bash Bunny is a sophisticated USB-based attack platform built by Hak5.org. Simple and easy to use for covert offensive operations against multiple target environments at the flick of a switch.

### MITRE ATT\&CK Tactics

* InInitial Access
  * T1200: Hardware Additions
* Exfiltration
  * T1052: Exfiltration Over Physical Medium
    * T1052.001: Exfiltration over USB

### More Information

Additional payloads: https://github.com/hak5/bashbunny- payloads&#x20;

Bash Bunny wiki: https://wiki.bashbunny.com&#x20;

Bash Bunny toolkits: https://bunnytoolkit.com&#x20;

Related Information Hak5 website: https://hak5.org&#x20;

