#  Nmap
Nmap, short for "Network Mapper," is a powerful open-source tool used for network discovery and security auditing.
It is designed to scan networks, identify hosts, services, and open ports, and create a map of the network topology. 

##  Host Discovery

Scan a specific subnet to discover live hosts:
- `nmap IP/Range`

Scan using hostnames to discover live hosts:
- `nmap scanme.nmap.org`

Use a simple ping scan to discover live hosts without port scanning:
- `nmap -sn IP/Range`

ARP ping scan
- `nmap -sn -PR IP/Range`

UDP ping scan
- `nmap -sn -PU IP/Range`

ICMP ECHO Ping scan/sweep
- `nmap -sn -PE IP/Range`

ACK Ping scan
- `nmap -sn -PA IP`

IP Protocol Ping scan
- `nmap -sn -PO IP`


##  Ports & Services Discovery

Specific port scan
- `nmap -p 21,80 IP` or `nmap -p 0-65535 IP` or `nmap -p- IP`

Version Detection Scan
- `nmap -sV -T4 IP`

Default script scan
- `nmap -sC -T4 IP`

TCP connect scan
- `nmap -sT -T3 -v IP`

Half-Open Scan / Stealth Scan
- `nmap -sS -v IP`

Aggresive scan
- `nmap -A IP`

Xmas scan
- `nmap -sX -T4 IP`


##  Banner Grabbing

OS detection scan
- ` nmap -O IP`

Nmap script os discovery
- `nmap --script smb-os-discovery.nse IP`

Aggresive scan
- `nmap -A IP`

##  Save output into a file

Save Normal Output
- `nmap -oN scan_results.txt target_ip`

Save Grepable Output
- `nmap -oG scan_results.gnmap target_ip`

Save XML Output:
- `nmap -oX scan_results.xml target_ip`

Save All Formats:
- `nmap -oA scan_results target_ip`


## Conclusion 

Do more Practice and Expert it!. <br>
**6/15/2024** <br>
Contributed By - Jord@n
