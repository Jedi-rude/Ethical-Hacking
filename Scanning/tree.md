```
Scanning
│
│
│
├────── What is Scanning
│	│
│	├─── [ Second phase for hacking ]
│	├─── [ Types ]
│	│	├─── [ Network Scanning ]
│	│	├─── [ Port Scanning ]
│	│	├─── [ Vulnerability Scanning ]
│	├─── [ Checking live systems & hosts in networks ]
│	├─── [ To discover IP, services, OS, vulnerabilities ]
│
│
│
├────── Tools & Techniques
│	│
│	├─── 1. Host Discovery
│	│
│	│	├─── [ Techniques ]
│	│	├─── [ ARP ping scan ]
│	│	│	├─── [ sending arp request & get response when alive ]
│	│	│	│	├─── [ nmap -sn -PR IP ]
│	│	├─── [ UDP ping scan ]
│	│	│	├─── [ sending udp request & get response when alive ]
│	│	│	│	├─── [ nmap -sn -PU IP ]
│	│	├─── [ ICMP ECHO Ping scan/sweep ]
│	│	│	├─── [ sending icmp request & get response when alive ]
│	│	│	│	├─── [ nmap -sn -PE ]
│	│	├─── [ TCP SYN Ping scan ]
│	│	│	├─── [ when ack response is back host is alive ]
│	│	│	│	├─── [ nmap -sn -PS IP ]
│	│	├─── [ ACK Ping scan ]
│	│	│	├─── [ when RST response is back host is up]
│	│	│	│	├─── [ nmap -sn -PA IP ]
│	│	├─── [ IP Protocol Ping scan ]
│	│	│	├─── [ scan with multiple ip packets & any response is get host is alive ]
│	│	│	│	├─── [ nmap -sn -PO IP ]
│	│	│	│
│	│	├─── hping3
│	│	│	├─── [  ] [  ]
│	│	│	├─── [ hping3 -1 IP (ICMP Ping) ] [ hping3 -A IP -p 80 (ACK scan) ]
│	│	│	├─── [ hping3 -2 IP (UDP scan) ] [ hping3 -8 50-60 -S IP -v (SYN scan) ]
│	│	│	├─── [ hping3 -F -P -U IP -p 80 ] [ hping3 -S IP -a IP -p 22 --flood (SYN) ]
│	│	├─── nmap
│	│	│	├─── nmap commands
│	│	│	│	├─── [ nmap -sn -PR IP ] [ nmap -sn -PE IP ]
│	│	│	│	├─── [ nmap -sn -PU IP ] [ nmap -sn -PP IP ]
│	│	│	│	├─── [ nmap -sn -PM IP ] [ nmap -sn -PS IP ]
│	│	│	│	├─── [ nmap -sn -PA IP ] [ nmap -sn -PO IP ]
│	│	├─── zennmap
│	│	│	├─── [https://nmap.org/zenmap/] 
│	│	├─── Angry IP Scanner
│	│	│	├─── [https://angryip.org/]
│	│	├─── Advanced IP Scanner
│	│	│	├─── [https://www.advanced-ip-scanner.com/download/]
│	│	├─── Visual Ping Tester
│	│	│	├─── [https://www.pingtester.net]
│	│	├─── Colasoft Ping
│	│	│	├─── [https://www.colasoft.com/ping_tool/]
│	│	├─── IP Scanner
│	│	│	├─── [https://www.komodolabs.com/ip-scanner/]
│	│	├─── Netdiscover
│	│	│	├─── [https://www.kali.org/tools/netdiscover/]
│	│	├─── Arp-scan
│	│	│	├─── [https://www.kali.org/tools/arp-scan/] 
│	│	├─── Super scan
│	│	│	├─── [https://www.filecroco.com/download-superscan/download]
│	│
│	├─── 2. Port & Service Discovery
│	│
│	│	├─── [ Techniques ]
│	│	├─── [ TCP connect scan ]
│	│	│	├─── [ a normal TCP connection to determine open or closed ]
│	│	│	│	├─── [ nmap -sT -T3 -v IP ]
│	│	├─── [ Half-Open Scan / Stealth Scan ]
│	│	│	├─── [ scan with uncomplete threewayhandshake signals ]
│	│	│	│	├─── [ nmap -sS -v IP ]
│	│	├─── [ Xmas scan ] [ Inverse TCP flag Scan ]
│	│	│	├─── [ all flags set to headers RFC793 ] [ scan with FIN,URG,PSH,NULL flags ] [ no response when port open ]
│	│	│	│	├─── [ nmap -sX -T4 IP ] [ -sF -sN ]
│	│	├─── [ TCP Maimon scan ]
│	│	│	├─── [ when scan with fin/ack flag no response is back port is open ]
│	│	│	│	├─── [ nmap -sM -v IP ]
│	│	├─── [ ACK scan ]
│	│	│	├─── [ ACK probe packet with random sequence number ]
│	│	│	│	├─── [ nmap -sA -v -T4 IP ]
│	│	├─── [ IDLE scan ]
│	│	│	├─── [ sending spoofed packets to a target. ]
│	│	│	│	├─── [ nmap -Pn -p 80 -sI fIP tIP ]
│	│	├─── [ UDP scan ]
│	│	│	├─── [ sending a generic UDP packet to the target ]
│	│	│	│	├─── [ nmap -sU -A IP ]
│	│	│	│
│	│	├─── nmap
│	│	│	├─── nmap commands
│	│	│	│	├─── [ nmap -sT -v IP ] [ nmap -sS -v IP ]
│	│	│	│	├─── [ nmap -sX -v IP ] [ nmap -sM -v IP ]
│	│	│	│	├─── [ nmap -sU -v IP ] [ nmap -sN -T4 -A -v IP ]
│	│	│	│	├─── [ nmap -sl -v IP ] [ nmap -sY -v IP ]
│	│	│	│	├─── [ nmap -sV -v IP ] [ nmap -A IP ] [ nmap -T4 -p- -A IP ]
│	│	│	│	├─── [ nmap -sZ -v IP ] [ nmap -sC -v IP ]
│	│	├─── Mega Ping
│	│	│	├─── [https://megaping.en.softonic.com/]
│	│	├─── Masscan
│	│	│	├─── [ https://github.com/robertdavidgraham/masscan ]
│	│	├─── NetScanTools pro
│	│	│	├─── [https://www.netscantools.com/download.html]
│	│	├─── advanced-port-scanner
│	│	│	├─── [https://www.advanced-port-scanner.com/]
│	│	├─── Rustscan
│	│	│	├─── [https://github.com/RustScan/RustScan]
│	│	├─── Open Port Scanner
│	│	│	├─── [https://www.solarwinds.com/engineers-toolset/use-cases/open-port-scanner]
│	│	├─── hping3
│	│	│	├─── hping3 commands
│	│	│	│	├─── [https://github.com/HiddenShot/Hping3]
│	│	│	│	├─── [ hping3 -A IP -p 80 -c 5 ] [ hping3 -8 0-100 -S IP -V 80 ]
│	│	│	│	├─── [ hping3 -F -P -U IP -p 80 -c 5 ] [ hping3 --scan 0-100 -S IP ]
│	│	│	│	├─── [ hping3 -1 IP -p 80 -c 5 ] [ hping3 -1 IP --rand-dest -l eth0 ]
│	│	│	│	├─── [ hping3 -2 IP -p 80 -c 5 ]
│	│	├─── sx tool
│	│	│	├─── sx commands
│	│	│	│	├─── [ sx arp IP/Subnet ]
│	│
│	├─── 3. OS Discovery
│	│
│	│	├─── Banner Grabbing
│	│	│	├─── active
│	│	│	│	├─── [ nmap -o IP ] [scan actively ]
│	│	│	├─── passive
│	│	│	│	├─── [ TTL value/TCP windows size ] [ sniffers ] 
│	│	├─── nmap
│	│	│	├─── nmap commands
│	│	│	│	├─── [ nmap -A IP ] [ nmap -O IP ] [ --osscan-guess ] [ nmap -6 -o IP ]
│	│	│	│	├─── [ nmap --script smb-os-discovery.nse IP ]
│	│	├─── wireshark
│	│	│	├─── [https://www.wireshark.org/download.html]
│	│	├─── unicornscan
│	│	│	├─── unicornscan commands
│	│	│	│	├─── [https://www.kali.org/tools/unicornscan/]
│	│	│	│	├─── [ unicornscan IP -lv ]
│	│
│	├─── 4. Evasion Scanning
│	│
│	│	├─── [ Techniques ]
│	│	├─── [ Packet Fragmentation ]
│	│	│	├─── [ splitting of probe packet into smaller packets(fragments) ]
│	│	│	│	├─── [ nmap -sS -T4 -A -f -v IP ]
│	│	├─── [ Source Routing ]
│	│	│	├─── [  IP options field stores source routing information to choose next hop]
│	│	│	│	├─── [  ]
│	│	├─── [ Source port manipulation ]
│	│	│	├─── [ actual port number is manipulate with common port number ]
│	│	│	│	├─── [ nmap -g 80 IP ]
│	│	├─── [ IP Address Decoy scan ]
│	│	│	├─── [ generating decoys ip address to scan ]
│	│	│	│	├─── [ nmap -D RND:10 IP ] [ nmap -D decoy1,decoy2,hIP,decoy3,tIP ]
│	│	├─── [ IP Adress Spoofing ]
│	│	│	├─── [ scan with spoofed IP ]
│	│	│	│	├─── [ hping3 tIP -a sIP ]
│	│	├─── [ Mac Address spoofing ]
│	│	│	├─── [ scan with spoofed mac address ]
│	│	│	│	├─── [ nmap -sT -Pn --spoof-mac 0 IP ]
│	│	├─── [ Custom packets ]
│	│	│	├─── [ scan with custom packets ]
│	│	│	│	├─── [  ]
│	│	├─── [ randomizing host order & sending bad checksums ]
│	│	│	├─── [ packets with bads checksums can evade firewalls ]
│	│	│	│	├─── [ nmap --random-hosts IP ] [ nmap --badsum IP ]
│	│	├─── [ Proxy Servers ] [ Proxy Chaining ] [ Anonymizers ]
│	│	│	├─── [ CCProxy / hotspotshield ]
│	│	├─── nmap 
│	│	│	├─── nmap commands
│	│	│	│   ├─── [ nmap -g 80 IP ] [ nmap -mtu 8 IP ]
│	│	│	│	├─── [ nmap -f IP ] [ nmap -sT -Pn --spoof-mac Dell IP ]
│	│	│	│	├─── [ nmap -D RND:10 IP ] [ nmap -sT -Pn --spoof-mac 00:00:00:00 IP ]
│	│	├─── Colasoft packet builder
│	│	│	├─── [https://www.colasoft.com/download/products/download_packet_builder.php]
│	│	├─── hping3
│	│	│	├─── hping3 commands
│	│	│	│	├─── [https://github.com/antirez/hping]
│	│	│	│	├─── [ hping3 IP --udp --rand-source --data 500 ] [ hping3 -S IP -p 80-c 5 ]
│	│	├─── Proxy switcher
│	│	│	├─── [https://www.proxyswitcher.com/download.html]
│	│	├─── Cyber Ghost
│	│	│	├─── [https://www.cyberghostvpn.com/en_US/download]
│	│	├─── whonix
│	│	│	├─── [ https://www.whonix.org/ ] 
│	│	├─── TunnelBear
│	│	│	├─── [ https://www.tunnelbear.com/ ]
│	│	├─── JonDo
│	│	│	├─── [ https://softfamous.com/jap-jondo/ ]
│	│	├─── Invisible Internet Project
│	│	│	├─── [ https://geti2p.net/en/ ] 
│	│	├─── alkasir
│	│	│	├─── [ https://github.com/alkasir/alkasir ]
│	│	├─── tails
│	│	│	├─── [ https://tails.net/install/ ]
│	│
│	├─── 5. Various Scanning Tools
│	│
│	│	├─── nmap
│	│	│	├─── nmap commands
│	│	│	│	├─── [ nmap -Pn -sS -A -oX Test IP ]
│	│	├─── Metasploit
│	│	│	├─── Modules
│	│	│	│	├─── [ auxiliary/scanner/portscan/syn ]
│	│	│	│	├─── [ auxiliary/scanner/portscan/tcp ]
│	│	│	│	│─── [ auxiliary/scanner/smb_version ]
│	│	│	│	├─── [ auxiliary/scanner/portscan/ack ]
│	│	│	│	├─── [ auxiliary/scanner/portscan/xmas ]
│	│	├─── netcat
│	│	│	├─── [https://eternallybored.org/misc/netcat/] 
│	│	├─── Network miner
│	│	│	├─── [https://www.netresec.com/]
│	│	├─── mylanviewer
│	│	│	├─── [https://www.mylanviewer.com/index.html]
│	│	├─── using netcat
│	│	│	├─── [https://eternallybored.org/misc/netcat/] 
│	│	├─── Network miner
│	│	│	├─── [https://www.netresec.com/]
│	│	├─── mylanviewer
│	│	│	├─── [https://www.mylanviewer.com/index.html]
│	│
│	├─── 6. Mobile Tools
│	│
│	│	├─── IP-Scanner
│	│	│	├─── [ https://10base-t.com/ipscanner/ ]
│	│	├─── Fing 
│	│	│	├─── [https://www.fing.com/fing-app/]
│
│
│
├────── Scanning Countermeasures
│	│
│	├─── 1. Port Scanning
│	│	├─── [ configure firewalls & IDS rules to detect blockprobes ]
│	│	├─── [ Routers, IDS, & Firewalls firmware re up-to-date ]
│	│	├─── [ use custom rules & block unwanted ports ]
│	│	├─── [ Filter all ICMP messages (type 3) ]
│	│	├─── [ anti-scanning & anti-spoofing rules are properly configured ]
│	│	├─── [ check firewalls & routers cannot be bypassed ]
│	├─── 2. Banner Grabbing 
│	│	├─── [ Display false banner ]
│	│	├─── [ Turnoff unnecessary services ]
│	│	├─── [ hide file extension to mask web technologies ]
│	│	├─── [ configure web server to hide banner information ]
│	├─── 3. IP Spoofing
│	│	├─── [ Encrypt all network traffic by using IPsec, TLS, SSH ]
│	│	├─── [ use multiple firewalls to provide multi-layer protection ]
│	│	├─── [ Do not rely on IP authenication ]
│	│	├─── [ use random initial sequence number ]
│	│	├─── [ Ingress / Egress Filtering ]
│	├─── 4. Prevention Tools
│	│	├─── [ ExtraHop ]
│	│	│	├─── [ https://docs.extrahop.com/current/intro-to-eh-system/ ]
│	│	│	├─── [ https://github.com/ExtraHop/threat-intelligence-toolkit ]
│	│	├─── [ Splunk ]
│	│	│	├─── [ https://www.splunk.com/ ]
│	│	├─── [ scanlogd ]
│	│	│	├─── [ https://www.openwall.com/scanlogd/ ]
│	│	├─── [ cynetsystems ]
│	│	│	├─── [ https://www.cynetsystems.com/ ]
│	│	├─── [ QRadar ]
│	│	│	├─── [ https://www.ibm.com/ ]
│
│
│
```
## Conclusion 

Do more Practice and Expert it!. <br>
**3/10/2024** <br>
Contributed By - Jord@n
