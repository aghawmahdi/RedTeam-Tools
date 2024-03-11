# Defense Evasion (TA0005)

## Defense Evasion with <mark style="color:red;">Meterpreter</mark>

### Why Learn Defense Evasion?

* Required skill for penetration testers and red-teamers
* Better detection and protection technologies & increased adoption rates
* Know your enemies to improve your defenses
* Developing better security technologies

### How to evade detection

* On disk
* At runtime
* In Memory
* On the network

### Meterpreter Components

1. Stager
   * Shellcode
   * Tied to a specific CPU architecture
   * Position-independent
   * Written in assembly
   * Can be used to
     * Exploit memory corruption bugs in software
     * Backdoor executable files
2. Handler
   * Runs on the attacker’s machine
   * Stager connects to the handler
   * Sends the meterpreter payload to the victim’s machine
   * Enables interaction with the victim’s machine
3. Payload
   * A reflective DLL file sent back to the stager by the handler
   * Bootstrapped by the stager
   * Contains the actual meterpreter code

### Reflective DLL Injection

* Loads the DLL from memory without writing it to disk
* Essentially performs the job of the operating system loader
* Very evasive, requires memory forensics to be detected
* Used by meterpreter payloads and other extensions such as «stdapi», «incognito» or «kiwi»

### Meterpreter Initialization

* Generate the HTTP stager
* Write a shellcode runner for our stager
* Configure the handler
* Execute the shellcode runner
* Step through the code as it executes

### Antivirus and EDR Components

* **Kernel-mode drivers**: Callback routines, filter drivers, network drivers
* **User-mode services**: Collects telemetry, communicates with cloud services
* **API monitoring**: API monitoring to get extra insight into process activity
* **ETW**: Consume events from ETW providers to collect telemetry
* **Emulators & Sandboxes**: Emulate or execute files and scripts to identify malicious activity
* **AMSI providers**: Scan scripts at runtime to prevent malicious activity

### Kernel-mode Drivers

#### Callback routines

* Process operations
* DLL loading operations
* Thread operations
* Handle operations
* Registry operations

#### Filter drivers

* File-system activities

#### Network drivers

* Network activities

### API Monitoring

* Usually, a DLL that uses a hooking library such as Microsoft Detours
* Injected by Kernel-mode drivers when processes are created
* It gives the Antivirus visibility into a process’s runtime behavior
* Hooks frequently abused API functions
  * GetProcAddress
  * VirtualAlloc
  * LoadLibrary
  * WriteProcessMemory
  * CreateRemoteThread

### ETW

* Provides additional telemetry
* Microsoft-Windows-Threat-Intelligence
* Memory and thread operations
* More robust than API monitoring

### Emulators

* Emulates an executable file or script to figure out what it would do if executed
* Tries to make the executable file or script believe they are being run on a real operating system
* Artifacts are collected and may trigger a detection by the antivirus
* Emulation is expensive and usually has a termination condition
  * The number of CPU instructions emulated
  * Elapsed time
  * Number of API calls identified

### Sandboxes

* Usually a Cloud-only feature due to performance impacts
* Uploads an executable file or script to the Cloud for analysis within a sandbox
* It differs from emulation because the file or script is executed
* Artifacts are collected and may trigger a detection

### AMSI Providers

* Scan scripts at runtime
* Useful to get insight into a script at runtime

### User-mode Services

* Consolidates and correlates the telemetry from the different data sources (Drivers, API monitoring, emulators, ETW consumers, AMSI, etc...)
* Orchestrates the antivirus activities
* Triggers file analysis and scans
* Sends files and scripts to emulators
* Sends the telemetry to central monitoring consoles, cloud-based file reputation services, and sandboxes so that it can be correlated with threat-intelligence data feeds

### Antivirus and EDR Detections

* **Signatures**: Match a specific sequence of bytes on disk, in memory, or on the network
* **Hash**: A file being written to disk matches a known malicious file hash
* **Heuristics**: A process is behaving in a way that is likely to be malicious
* **ML classifiers**: A file is classified as malicious because of its characteristics
* **Threat-Intelligence**: Known malicious file names, IP addresses, and domain names

### Custom Shellcode Runner

* The stager can be embedded inside the shellcode runner
* Stealthy

### Metasploit exe Format

* Can be used by passing the –f exe flag to msfvenom
* If the –x flag is not specified, the default templates are used
* Makes use of a small stub of shellcode and VirtualAlloc.
* It copies the stager inside the section at runtime

### Metasploit exe-only Format

* Can be used by passing the –f exe-only flag to msfvenom
* If the –x flag is not specified, the default templates are used
* Insert the stager at the entry point of the executable file

### Encoders and Encryptors

* Stagers contain hardcoded shellcode which is ideal for developing signatures
* Metasploit ships with various encoders and encryptors
* Encoders can be used by passing the –e flag to msfvenom
* Encryptors can be used by passing the -- encrypt and --encrypt-key flags
* Some are polymorphic, such as the Zutto\_Dekiru encoder which is hard to detect

### Modifying the Stager Shellcode

* An alternative to using an encoder or encryptor
* Not as generic as an encoder
* More complex
* More time-consuming

### Confusing AI/ML Models

* Avoid having too few imports in the executables IAT
* Avoid having frequently-abused APIs in the executables IAT
* Avoid RWX permissions on memory sections
* Avoid high entropy inside RWX memory sections

### Evading API Monitoring

* API monitoring is performed in user-land by performing DLL injection and hooking APIs
* The DLL is injected into our malicious process. We have control over our process! We can remove the hooks or avoid them

### Evading Hooks

* Patching the hook to restore the original function’s entry point
* Copying the code from the original DLL on disk and overwriting it in memory
* Copying the original DLL and reloading it at runtime
* Performing manual syscalls

### Anti-Emulation

* Conditional code and un-emulated APIs
* Exhausting the emulator
* Conditional code which attempts to identify if emulation is occurring
* Checking CPU registry value discrepancies

### Anti-Sandboxing

* Similar techniques as those covered in anti-emulation
* Resource consumption is usually not a vector since it is probably in the Cloud
* Fingerprinting the sandbox

### Bypassing AMSI

* Occurs inside your PowerShell process
* Automatically sends buffers containing code to be scanned to the AMSI API
* The AMSI API can be tampered with because it is hosted by a DLL loaded inside our process
* Similar issue to API monitoring using DLL injection

### Evading in-memory Signatures

* Signatures are also used in memory to detect code after it has been decoded or decrypted
* We can evade them by modifying the code and artifacts that reside in memory

### Evading in-memory Signatures

* Identifying good signature candidates
* Automating the code refactoring
* Manually performing the code refactoring
* Using shared forks of the project on GitHub
* Reverse engineering the antivirus

### Encoding the Payload

* Signatures are also used on the network and can detect our payload when the handler sends it back to the stager
* We can avoid this by encoding the payload before sending it back to the stager

### SSL Certificates

* When using HTTPS stagers, make sure you don’t use the default certificate
* Some IDS and antivirus solutions have a signature on the certificate

### Ja3/Ja3s Fingerprints

* Ja3/Ja3s fingerprints can be used to identify a stager connection to a Metasploit handler
* This fingerprint can be altered by using alternate TLS ciphers.

### Tips and Tricks

* Domain fronting to evade domain categorization filters and SSL interception
* Realistic user agents, headers, and authentication
* Stage-less payloads can be used to avoid sending the payload through the network



### Defense Evasion with <mark style="color:red;">ProxyChains</mark>

A tool that forces any TCP connection made by any given application to follow through a proxy like TOR or any other SOCKS4, SOCKS5, or HTTP(S) proxy. One of the most well-known tools for traffic redirection, Allows to redirecting of TCP packets from any tool (e.g. NMap, theHarvester, SSH, etc.), Provides anonymous traffic, and bypasses defense mechanisms.

Open source software: https://github.com/haad/proxychains

### MITRE ATT\&CK Tactics

#### Defense Evasion

* T1599: Network Boundary Bridging



### Defense Evasion with <mark style="color:red;">Invoke-Obfuscation</mark>

A PowerShell v2.0+ compatible PowerShell command and script obfuscator.

Open source under Apache 2.0 License: https://github.com/danielbohannon/ Invoke-Obfuscation

### MITRE ATT\&CK Tactics

#### Defense Evasion

* T1027: Obfuscated Files or Information
* T1140: Deobfuscate/Decode Files or Information



### Defense Evasion with <mark style="color:red;">Veil</mark>

The Veil-Framework is a collection of red team security tools that implement various attack methods focused on evading detection. Allows use of custom or preexisting shellcode and leverages several obfuscation and evasion techniques to create payloads with a unique signature.

Available at: github.com/Veil- Framework/Veil/ for download and through Linux package managers

PyHerion obfuscation: https://www.veil-framwork.com/pyherion/

### MITRE ATT\&CK Tactics

#### Execution

* T1059: Command and Scripting Interpreter
  * T1059.006: Python

#### Defense Evasion

* T1027: Obfuscated files or information
  * T1027.002: Software packaging
* T1480: Execution guardrails
  * T1480.001: Environmental keying

