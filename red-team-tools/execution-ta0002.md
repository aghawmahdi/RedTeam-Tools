# Execution (TA0002)

## Execution with <mark style="color:red;">macro\_pack</mark>

macro\_pack is a tool used to automatize obfuscation and generation of Office documents, VB scripts, shortcuts, and other formats for pentest, demo, and social engineering assessments.

Several advanced features:

* Anti-virus bypassing
* Sandbox detection
* Weaponized templates

Open source tool (Apache V2.0): https://github.com/sevagas/macro\_pack

### MITRE ATT\&CK Tactics

#### Execution

* T1204: User Execution
  * T1204.002 Malicious File
* T1059: Command and Scripting Interpreter
  * T1059.005 Visual Basic

#### Initial Access

* T1566: Phishing
  * T1566.001 Spearphishing Attachment



## Execution with <mark style="color:red;">Donut</mark>

Donut is an open-source shellcode generation tool. The open-source tool is available on GitHub and enables in-memory execution of VBScript, JScript, EXE, DLL files, and dotNET assemblies.

Installation, usage, and external links: https://github.com/TheWover/donut

In-memory execution using shellcode: https://modexp.wordpress.com/2019/07/ 21/inmem-exec-script/

Injecting .NET assemblies as shellcode: https://thewover.github.io/IntroducingDonut/

MITRE ATT\&CK Execution TA0002: https://attack.mitre.org/tactics/TA0002

MITRE ATT\&CK Defense Evasion TA0005: https://attack.mitre.org/tactics/TA0005/

### MITRE ATT\&CK Tactics

#### Execution

* T1106: Native API

#### Defense Evasion

* T1055.001: Dynamic-link Library Injection
* T1055.002: Portable Executable Injection

