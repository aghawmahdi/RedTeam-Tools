# Persistence (TA0003)

## Persistence with <mark style="color:red;">Empire</mark>

Empire 3 is a pure PowerShell post-exploitation framework. It merged the previous PowerShell Empire and Python EmPyre projects.

Empire Documentation: https://www.powershellempire.com/

MITRE ATT\&CK Software Page: https://attack.mitre.org/software/S0363/

### MITRE ATT\&CK Tactics

#### Persistence

* T1547.001 Boot or Logon Autostart Execution
* T1136.001 Create Account: Local Account
* T1053.002 Scheduled Task/Job
* T1546.003 Event Triggered Execution



## Persistence with <mark style="color:red;">Impacket</mark>

Impacket is a collection of Python classes focused on providing low-level programmatic access to network packets and protocols and Provides low-level access to network and protocols.

Open source software: https://github.com/SecureAuthCorp/impacket

Several other capabilities: https://github.com/SecureAuthCorp/impacket

Contains several out-of-the-box scripts for privilege escalation and persistence

* WMI Persist
* WMI Exec
* Active Directory Recon
* Mimikatz
* Secrets dump
* etc.

Other Features:

* SMB server/relays
* Network packet manipulation
* Active Directory recon

### MITRE ATT\&CK Tactics

#### Execution

* T1047: Windows Management Instrumentation

#### Persistence

* T1546: Event-Triggered Execution
  * T1546.003: Windows Management Instrumentation Event Subscription
* T1078: Valid Accounts



## Persistence with <mark style="color:red;">pwncat</mark>

pwncat is a post-exploitation platform that streamlines common red team operations while staging code from the attacker machine, not the target.

Provides a complete framework for post-exploitation

* Enumeration modules
* Privilege escalation modules
* Persistence modules (implants)

Open source software: https://github.com/calebstewart/pwncat

### MITRE ATT\&CK Tactics

#### Persistence

* T1078: Valid Accounts
  * T1078.003: Local Accounts

#### Discovery

* T1087: Account Discovery
  * T1087.001: Local Accounts
