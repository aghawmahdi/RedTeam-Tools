# Command and Control (TA0011)

## Command and Control with <mark style="color:red;">Covenant</mark>

For use in adversary emulation of collaborative command and control. An evolution away from burned PowerShell-based capabilities that highlight the attack surface of .NET

Available at [https://github.com/cobbr/Covenant](https://github.com/cobbr/Covenant)

### MITRE ATT\&CK Tactics

#### Defence Evasion

* T1500: Compiled after delivery

#### Command and Control

* T1043: Commonly Used Ports
* T1090: Proxied connections

### More Information

Listener Profiles: [https://github.com/cobbr/Covenant/wiki/Listener-Profiles](https://github.com/cobbr/Covenant/wiki/Listener-Profiles)

API Usage: [https://github.com/cobbr/Covenant/wiki/Using-The-API](https://github.com/cobbr/Covenant/wiki/Using-The-API)

C2-Next Generation: [https://blog.netwrix.com/2023/01/27/powershell-empire-covenant/](https://blog.netwrix.com/2023/01/27/powershell-empire-covenant/)



## Command and Control with <mark style="color:red;">Pupy</mark>

Pupy is an open-source remote administration and post-exploitation tool written in Python. Pupy executes in memory, allowing it to leave a low footprint. Pupy also offers multiple communications channel options to mask traffic.

Post exploitation tool to manage exploited clients from a central server Open source project, can be downloaded from their GitHub page Pupy has multiple advantages, including a low footprint, multiple channel encryption options, and built-in privilege escalation options.

### MITRE ATT\&CK Tactics

#### Credential Access

* T1003: Credential Dumping

#### Collection

* T1056: Input Capture

#### Command & Control

* T1032: Standard Cryptographic Protocol

### More Information

{% embed url="https://github.com/n1nj4sec/pupy" %}



## Command and Control with <mark style="color:red;">Empire</mark>

Empire 3 is a pure PowerShell post-exploitation framework. It merged the previous PowerShell Empire and Python EmPyre projects.

### MITRE ATT\&CK Tactics

#### Command & Control

* T1105: Ingress Tool Transfer
* T1219: Remote Access Software
* T1571: Non-Standard Port
* T1090.003: Proxy: Multi-Hop Proxy

### Empire Workflow

* Listeners
* Stagers
* Agents
* Modules

### More Information

Empire Documentation: https://www.powershellempire.com/

MITRE ATT\&CK Software Page: https://attack.mitre.org/software/S0363/



## Command and Control with <mark style="color:red;">Merlin</mark>

It is an open-source C2 framework written in Golang. Evade network detection during a penetration test/red team exercise by using a protocol that existing tools aren’t equipped to understand or inspect. Protocols: HTTP/1.1, HTTP/2, HTTP/3.

Available at github.com/Ne0nd0g/merlin

### MITRE ATT\&CK Tactics

#### Command & Control

* T1105: Ingress Tool Transfer
* T1071: Application Layer Protocol
  * T1071.001: Web Protocols

#### Exfiltration

* T1041: Exfiltration Over C2 Channel

### More Information

https://www.sans.org/readingroom/whitepapers/protocols/paper/ 36877

https://medium.com/@Ne0nd0g/me rlin-adds-module-supportf1211175412e

https://medium.com/@Ne0nd0g/me rlin-adds-dll-agent-powershellinvoke-merlin-script-6127b3d7cbcd

https://merlinc2.readthedocs.io/en/v0.9.0- beta/misc/blogs.html Related Information Web Protocols

&#x20;https://attack.mitre.org/techniques/T10 71/001/



## Command and Control with <mark style="color:red;">PoshC2</mark>

PoshC2 is a proxy aware Command and Control framework used to assist with red teaming, post-exploitation, and lateral movement.

Available from the PoshC2 github repository: https://github.com/nettitude/PoshC2

### MITRE ATT\&CK Tactics

#### Discovery

* T1087: Account Discovery
  * T1087.001 Local Account

#### Command & Control

* T1071: Application Layer Protocol
  * T1071.001: Web Protocols
* T1219: Remote Access Software

### More Information

Modules Scripts https://github.com/nettitude/PoshC2/t ree/master/resources/modules

Domain Fronting https://poshc2.readthedocs.io/en/lates t/install\_and\_setup/architecture.html#d omain-fronting Related Information

Documentation Guide https://poshc2.readthedocs.io/en/latest/i ndex.html



