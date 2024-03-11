# Reconnaissance (TA0043)

## Reconnaissance with <mark style="color:red;">OWASP Amass</mark>

### Domain Enumeration

* DNS Queries
* Open Source Databases
* Certificates
* APIs
* Web Archive

Amass OWASP is a tool for performing network mapping of attack surfaces and external asset discovery using open-source information gathering and active reconnaissance techniques.

### Advanced Recon Techniques

1. Brute Force
   * web.globomantics.com
   * mail.globomantics.com
   * ftp.globomantics.com
2. Alterations
   * dc01.globomantics.com
   * dc02.globomantics.com
   * dc03.globomantics.com
3. Reverse WHOIS
   * john@globomantics.com => globomantics.com
4. Web Archive
   * 2008 => dev.globomantics.com

### More Information:

* Several other capabilities: https://github.com/OWASP/Amass
* Other Reconnaissance tools:
  * theHarvester
  * Sn1per

### MITRE ATT\&CK Tactics

#### Reconnaissance

* **T1596**: Search Open Technical Databases
  * **T1596.001**: DNS/Passive DNS
  * **T1596.002**: WHOIS
  * **T1596.003**: Digital Certificates



## Reconnaissance with <mark style="color:red;">Sn1per</mark>

You can find IP addresses, open ports, and even vulnerabilities on the server. a tool for discovering attack surfaces and prioritizing risks. it automates the most common reconnaissance techniques.

One of the most complete tools for reconnaissance, Leverage several of the most used recon scripts (NMap, theHarvester, WafWoof, etc.)

### Recon Data

#### Passive Information Gathering

* WHOIS records
* DNS queries
* OSINT searches
* Social media searches
* Search engine recon

#### Active Information Gathering

* NMAP Port scans
* Vulnerability scans
* Web application probing

### Download and install link:

[https://github.com/1N3/Sn1per](https://github.com/1N3/Sn1per)

[https://sn1persecurity.com/wordpress/](https://sn1persecurity.com/wordpress/)

[https://xerosecurity.com/](https://xerosecurity.com/)

In Sn1per Pro Version there are more options and in GUI mode.

### MITRE ATT\&CK Tactics

#### Reconnaissance

* **T1595**: Active Scanning
* **T1592**: Gather Victim Host Information
* **T1590**: Gather Victim Network Information
* **T1596**: Search Open Source Technical Databases
* **T1593**: Search Open Source Websites/Domains
* **T1589**: Gather Victim Identity Information



## Reconnaissance with <mark style="color:red;">theHarvester</mark>

theHarvester is a tool for open source intelligence gathering and helping to determine a company's external threat landscape on the internet. The tool gathers emails, names, subdomains, IPs, and URLs using multiple public data sources. searching on websites like Google, Yahoo, Bing, LinkedIn, etc.

Performs non-intrusive information gathering (as well as intrusive)

* DNS names
* IP addresses/ranges
* Email addresses
* Linkedin profiles
* Open ports

### Download and install link:

[https://github.com/laramies/theHarvester](https://github.com/laramies/theHarvester)

### MITRE ATT\&CK Tactics

#### Technical Information Gathering

* **T1250**: Determine domain and IP Address Space
* **T1255**: Discover target logon/email address format
* **T1251**: Obtain domain/IP registration information
* **T1254**: Conduct Active Scanning

#### People Information Gathering

* **T1273**: Mine Social Media



## Reconnaissance with <mark style="color:red;">Recon-ng</mark>

It is an open-source framework providing a powerful environment to automate open-source web-based reconnaissance. available at recon-ng.com for download.

### MITRE ATT\&CK Tactics

#### Technical Information Gathering

* T1250: Determine domain and IP address space
* T1261: Enumerate externally facing software applications technologies, languages, and dependencies

#### People Information Gathering

* T1271: Identify personnel with an authority/privilege



## Reconnaissance with <mark style="color:red;">Maltego CE</mark>

Technical Information Gathering with Maltego CE, Automating information gathering:

* Gather subdomains
* Gather DNS data
* Gather IP addresses
* Gather technology information
* Identify people information
* Identify email addresses

Maltego is an open-source intelligence (OSINT) and graphical link analysis tool for gathering and connecting information for investigative tasks. community edition version - free for download: https://www.maltego.com/

### MITRE ATT\&CK Tactics

#### Technical Information Gathering

* T1253: Conduct passive scanning
* T1250: Determine domain and IP address space

#### People Information Gathering

* T1269: Identify People of Interest



## Reconnaissance with <mark style="color:red;">Social Engineering Toolkit (SET)</mark>

The weakest link to any system is the person holding the information. Social Engineering has been around for ages. You can perform spear phishing attacks, credential harvesting attacks and much more.

Download link: [https://trustedsec.com/resources/tools/the-social-engineer-toolkit-set](https://trustedsec.com/resources/tools/the-social-engineer-toolkit-set)

It is an open-source tool, and provides multiple attack vectors:

* Spear-phishing attacks
* Website attacks
* Infectious media creation

Social Engineering Attacks include:

* Spearphishing Attacks
* Website Attacks
* Infectious Media Attacks
* Wireless AP Attacks
* Powershell Attacks

### MITRE ATT\&CK Tactics

#### Technical Information Gathering

* T1249: Conduct Social Engineering
* T1397: Spearphishing for information

#### People Information Gathering

* T1268: Conduct Social Engineering



## Reconnaissance with <mark style="color:red;">Nikto</mark>

Nikto is a free and open-source web server and web application assessment tool. The primary function of Nikto is to identify security weaknesses such as default files, misconfiguration, or published security vulnerabilities. With Nikto, you can scan a web server to find vulnerabilities, run the scans through a proxy, set static cookies, or replay individual positive findings.

Performs web server vulnerability identification:

* Identifies outdated components
* Allow for the replay of findings
* Identifies server and software misconfigurations
* finds default or insecure files
* full proxy support

### MITRE ATT\&CK Tactics

#### Technical Weakness Identification

* T1293: Analyze application security posture
* T1288: Analyze architecture and configuration posture



## Reconnaissance with <mark style="color:red;">SHODAN</mark>

A search engine for Internet-connected devices. Shodan explores systems with public IP addresses, not the web content. Available at https://www.shodan.io/

### MITRE ATT\&CK Tactics

#### Reconnaissance

* T1590: Gather Victim Network Information
  * T1590.002 DNS
  * T1590.005 IP Addresses
* T1592: Gather Victim Host Information
  * T1592.001 Hardware
  * T1592.002 Software
  * T1592.003 Firmware
  * T1592.004 Client Configurations
* T1596: Search Open Technical Databases
  * T1596.003 Digital Certificates
  * T1590.005 Scan Databases



## Reconnaissance with <mark style="color:red;">Spiderfoot</mark>

An automation platform for open-source intelligence gathering. Spiderfoot delivers reconnaissance data on targets using various internet information sources over 200 modules.

Available at https://www.spiderfoot.net

It is used in GUI mode too.

### MITRE ATT\&CK Tactics

#### Reconnaissance

* T1589: Gather Victim Identity Information
  * T1589.001 Credentials
  * T1589.002 Email Addresses
  * T1589.003 Employee Names
* T1593: Search Open Websites/Domain
  * T1593.001 Social Media
  * T1593.002 Search Engines
* T1596: Search Open Technical Databases
  * T1596.001 DNS/Passive DNS
  * T1596.002 WHOIS
  * T1596.003 Digital Certificates
  * T1596.005 Scan Databases
