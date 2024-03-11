# Discovery (TA0007)

## Discovery with <mark style="color:red;">BloodHound</mark>

BloodHound uses graph theory to reveal the hidden and often unintended relationships within an Active Directory environment. BloodHound allows you to find complex paths to your objective easily.

BloodHound is a single-page JavaScript web application built on a Neo4j database, allowing you to visualize and find complex attack paths in Active Directory. Available at https://github.com/BloodHoundAD/BloodHound

### MITRE ATT\&CK Tactics

#### Discovery

* T1087: Account Discovery
* T1069: Permission Groups Discovery
* T1033: System Owner/User Discovery

### More Information

Cypher Query Language https://github.com/BloodHoundAD/Blo odHound/wiki/Cypher-Query-Language

neo4j REST API https://github.com/BloodHoundAD/Blo odHound/wiki/neo4j-REST-API

BloodHound-owned https://github.com/porterhau5/BloodHound-Owned

Related Information https://adsecurity.org/

* Delegation
* Kerberoasting&#x20;

https://github.com/SpiderLabs/Responder

* Steal credentials
* Mark as owned in BH



## Discovery with <mark style="color:red;">Seatbelt</mark>

Seatbelt is a C# project that performs several security-oriented host-survey "safety checks" relevant from both offensive and defensive security perspectives.

Open source software https://github.com/GhostPack/Seatbelt

Automates several discovery tasks for red team engagements and Over 100 discovery modules, including:

* Local and domain user enumeration
* Privilege mapping
* Anti-virus detection
* OS reconnaissance
* Browser history enumeration ... and much more!

### MITRE ATT\&CK Tactics

#### Discovery

* T1518.001: Security Software Discovery
* T1082: System Information Discovery
* T1087: Account Discovery
  * T1087.001: Local Accounts
  * T1087.002: Domain Accounts

### More Information

Several other capabilities https://github.com/GhostPack/Seatbelt



## Discovery with <mark style="color:red;">Kismet</mark>

Kismet is a wireless network and device detector, sniffer, wardriving tool, and WIDS (wireless intrusion detection) framework.

Kismet is a wireless network and device detection tool that allows you to gather information from network names to lists of clients, data being transmitted, and much more. Available at https://www.kismetwireless.net/

### MITRE ATT\&CK Tactics

#### Discovery

* T1507: Network Information Discovery
* T1040: Network Sniffing
* T1439: Eavesdrop on Insecure Network Communication (ATT\&CK Mobile: Network Effects)

### More Information

Remote Packet Capture https://www.kismetwireless.net/docs/r eadme/datasources\_remote\_capture

GPS Support https://www.kismetwireless.net/docs/r eadme/gps/

Attacking WPA2 Networks https://www.krackattacks.com



## Discovery with <mark style="color:red;">ADRecon</mark>

A tool that gathers information about the Active Directory and generates a report that can provide a holistic picture of the current state of the target AD environment.

Open source tool (GNU v3.0) https://github.com/adrecon/ADRecon

Version for Azure Active Directory https://github.com/adrecon/AzureADRecon

Usually not detected by anti-virus

Does not require admin privileges

Gathers several interesting information:

* Users
* Service accounts
* Security policies
* Computers
* etc.

### MITRE ATT\&CK Tactics

#### Discovery

* T1201: Password Policy Discovery
* T1069: Permission Groups Discovery
* T1087: Account Discovery

#### Credential Access

* T1558: Steal or Forge Kerberos Tickets
  * T1558.003: Kerberoasting

#### Collection

* T1213: Data from Information Repositories

### More Information

#### Password Cracking Tools

Hashcat https://hashcat.net/

John-The-Ripper https://github.com/magnumripper/ JohnTheRipper

