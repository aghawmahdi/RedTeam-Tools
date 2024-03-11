# Impact (TA0040)

## Impact with <mark style="color:red;">Slowloris</mark>

Slowloris is an HTTP Denial of Service attack that affects threaded servers. This exhausts the server's thread pool and the server can't reply to other people.

Impact tool using DDoS methodology, DDoS – Distributed Denial of Service, and Difficult to differentiate from legit traffic.

### MITRE ATT\&CK Tactics

#### Impact

* T1498: Network Denial of Service
* T1499: Endpoint Denial of Service

### More Information

Slowloris https://github.com/gkbrk/slowloris

Gokberk Yaltirakli https://www.gkbrk.com/



## Impact with <mark style="color:red;">Low Orbit Ion Cannon (LOIC)</mark>

Low Orbit Ion Cannon (LOIC) is an open-source network stress tool. The open-source tool available on GitHub is based on Praetox’s LOIC project and is now managed by multiple contributors. LOIC is a network stress tool.

### MITRE ATT\&CK Tactics

#### Impact

* T1498.001: Service Direct Network Flood
* T1499.002: Service Exhaustion Flood

### More Information

Running on other operating systems https://github.com/NewEraCracker/LOIC /wiki

MITRE ATT\&CK Impact TA0040 https://attack.mitre.org/tactics/TA0040/

