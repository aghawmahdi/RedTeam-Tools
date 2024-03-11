# Lateral Movement (TA0008)

## Lateral Movement with <mark style="color:red;">Mimikatz</mark>

Mimikats is a tool to extract plain text passwords, hashes, kerberos tickets, and PIN codes from memory. In addition, Mimikatz can also used to pass the hash, pass the ticket, or create golden and silver tickets.

GitHub: https://github.com/gentilkiwi/mimikatz

### MITRE ATT\&CK Tactics

#### Defense Evasion

* T1207: DCShadow

#### Lateral Movement

* T1075: Pass the Hash
* T1097: Pass the Ticket

### Usages:

* Using Mimikatz to Pass the Hash (PTH)
* Use Mimikatz to Pass the Ticket (PTT)
* Use Mimikatz to create Golden Tickets
* Use Mimikatz to create Silver Tickets
* Register a rogue domain controller with DCShadow

### More Information

Mimikatz Wiki https://github.com/gentilkiwi/mimikatz/wiki

MITRE ATT\&CK https://attack.mitre.org/software/S0002/

Active Directory Security – Unofficial Guide to Mimikatz & Command Reference https://adsecurity.org/?p=2207

Benjamin Delpy on Twitter https://twitter.com/gentilkiwi?lang=en



## Lateral Movement with <mark style="color:red;">psexec</mark>

PsExec is one of the tools in the Sysinternals PsTools suite. PsExec is used to execute processes on remote machines without having to install additional software.

PsExec is a tool that executes processes on remote machines. You can download it as part of the PsTools suite from Microsoft. PsExec allows you to execute processes on remote Windows machines without installing additional software.

### MITRE ATT\&CK Tactics

* T1035: Service Execution
* T1077: Windows Admin Shares

### Usages:

#### Getting started with PsExec

* Copy PsExec to your compromised Windows machine
* Explore the available options

#### Use PsExec to execute commands on other Windows machines

* Run a command to obtain information about another target
* Use PsExec to copy programs to a new target

Using these features will allow you to run commands on remote workstations

#### Use PsExec to run programs on remote Windows machines

* Use PsExec to execute programs on remote machines
* Use PsExec to open a connection to the new target

PsExec allows you to run programs or scripts on remote workstations that can create additional vulnerabilities

#### Use PsExec to run command prompts and laterally move through a network

* Use PsExec to open a command prompt and interact with a remote machine
* From this command prompt, use PsExec to run commands on other machines

### More Information

PsExec usage https://docs.microsoft.com/enus/sysinternals/downloads/psexec

Original 2004 article https://www.itprotoday.com/computeengines/psexec

MITRE ATT\&CK lateral movement https://attack.mitre.org/tactics/TA0008/



## Lateral Movement with <mark style="color:red;">WMIOps</mark>

WMIOps is a PowerShell script that leverages the capabilities of WMI to perform actions on Windows hosts, either local or remote.

WMIOps is a PowerShell script that performs actions on Windows hosts and allows you to execute PowerShell commands on other Windows hosts from an exploited machine.

### MITRE ATT\&CK Tactics

#### Execution

* T1077: Windows Admin Shares

#### Lateral Movement

* T1047: Windows Management Instrumentation

### More Information

WMIOps usage https://github.com/FortyNorthSecurity /WMIOps

MITRE ATT\&CK lateral movement https://attack.mitre.org/tactics/TA0008/



## Lateral Movement with <mark style="color:red;">CrackMapExec</mark>

CrackMapExec is a collection of red team security tools that use Windows features and protocols to test domain networks.

Available at [https://github.com/byt3bl33d3r/CrackMapExec](https://github.com/byt3bl33d3r/CrackMapExec)

Allows abuse of readily available programs and protocols to map AD networks, and gather credentials and other information to further your presence on the network.

### MITRE ATT\&CK Tactics

#### Credential Access

* T1480: Steal or Forge Kerberos Tickets
  * T1558.004: AS-REP Roasting

#### Lateral Movement

* T1021: Remote Services
  * T1021.002: SMB/Windows Admin Shares
  * T1021.006: Windows Remote Management

### Also, consider these tools

{% embed url="https://github.com/gojhonny/CredCrack" %}

{% embed url="https://github.com/ShawnDEvans/smbmap" %}

{% embed url="https://www.pentestgeek.com/penetration-testing/smbexec-2-0-released" %}

### More Information

{% embed url="https://github.com/BloodHoundAD/BloodHound" %}

{% embed url="https://medium.com/@sytryx/a-comprehensive-guide-on-as-rep-roasting-red-blue-team-d3cc3aa2d6fe" %}



## Lateral Movement with <mark style="color:red;">Infection Monkey</mark>

The Infection Monkey is an open-source security tool for testing a network’s perimeter breaches and internal server infection. The Monkey uses built-in exploits to self-propagate across a system and reports success to a centralized Monkey Island server.

Infection Monkey is downloadable through Guardicore’s website in any available platform format. Infection Monkey is a self-propagating payload that scans, discovers, and compromises connected hosts on a network. The Monkey is not adversary emulation. Payloads are real.

{% embed url="https://www.akamai.com/infectionmonkey" %}

{% embed url="https://github.com/guardicore/monkey" %}

### MITRE ATT\&CK

#### Discovery

* T1018: Remote System Discovery

#### Lateral Movement

* T1210: Exploitation of Remote Services
* T1021: Remote Services
  * T1021.002: SMB/Windows Admin Shares
  * T1021.004: SSH

### More Information

Pass-the-Hash & Tunneling: https://www.guardicore.com/infectionm onkey/features.html

Zero-Trust Networking:

https://www.guardicore.com/infectionm onkey/zero-trust.html

https://www.guardicore.com/2019/10/g uardicore-infection-monkey-for-zerotrust

More Monkey with MITRE https://www.guardicore.com/2020/04/t est-your-attck-before-the-attack-withguardicore-infection-monkey/

