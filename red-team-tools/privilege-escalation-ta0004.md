# Privilege Escalation (TA0004)

## Privilege Escalation with <mark style="color:red;">Rubeus</mark>

A tool for raw Kerberos interaction and abuses. Automates several privilege escalation attacks:

* Kerberoasting
* AS-REP Roasting
* Pass the Hash / Pass the Ticket
* Golden Ticket
* Silver Ticket

Open source software: https://github.com/GhostPack/Rubeus

### MITRE ATT\&CK Tactics

#### Privilege Escalation

* T1134: Access Token Manipulation

#### Credential Access

* T1558: Steal or Forge Kerberos Tickets
  * T1558.003: Kerberoasting
  * T1558.004: AS-REP Roasting



## Privilege Escalation with <mark style="color:red;">UACMe</mark>

Privilege escalation tool to defeat Microsoft Windows User Account Control. It has over 60 exploits that can be used to bypass the Windows UAC consent box. This is a small command line tool that performs the task consistently.

You can get it from this repo www.github.com/hfiref0x/UACME

### MITRE ATT\&CK Tactics

#### Privilege Escalation - Defense Evasion

* T1548: Abuse Elevation Control Mechanism
  * T1548.002: Bypass User Account Control

https://attack.mitre.org/techniques/T1548 /002/



## Privilege Escalation with <mark style="color:red;">SharpUp</mark>

SharpUp is a C# port of various PowerUp features. It is a useful tool to discover misconfigurations that could lead to privilege escalation. Focused on Windows privilege escalation 13 modules, including:

* AlwaysInstallElevated
* CachedGPPPassword
* HijackablePaths
* RegistryAutoruns
* UnquotedServicePath
* … and much more!

Open source software: https://github.com/GhostPack/SharpUp

### MITRE ATT\&CK Tactics

#### Privilege Escalation

* T1574: Hijack Execution Flow
  * T1574.005: Executable Installer File Permissions Weakness
* T1547: Boot or Logon Autostart Execution
  * T1547.001: Registry Run Keys / Startup Folder

