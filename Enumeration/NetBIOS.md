# NetBIOS Enumeration by Using Various Techniques 

NetBIOS stands for Network Basic Input/Output System is a network service that enable computers to communicate over a Local Area Network(LAN). We can get information about network resources, share resources and other useful information by enumerating.

## Tools Requirements 
- [Nbtstat](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/nbtstat)
- [Nmap](https://www.nmap.org)
- [NetBIOS Enumerator](https://nbtenum.sourceforge.net)
- [Soft Perfect Network Scanner](https://www.softperfect.com/products/networkscanner/)

## Lab Configuration 
- Windows-7
- Windows Server 2003
- Make sure two hosts are in same network

## NetBIOS Enumeration with Windows Network utility
In windows command line type ``` nbtstat -a [Target IP Address] ``` to start enumerate and press enter.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/647cb4bc-6873-4118-a297-948524e6508e" width="400px" height="250px"><br>Figure (1) Network Share Resources</p>

And then, type ``` nbtstat -c ``` and press enter to display network cache.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/ab458ee9-ef3a-4bec-b4a9-2b1ad5a22f12" width="400px" height="250px"><br>Figure (2) Taget Information </p>

After accessing network resources, type ``` net use ``` to see related history records.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/dd0ae905-50a7-4534-9040-c89f8bd032fe" width="400px" height="250px"><br>Figure (3) Netwrok Shares Records</p>

## NetBIOS Enumeration with nmap scripts 
Go to the folder where nmap locate, Type ``` nmap -sV -v --script nbstat.nse [Target IP Address] ``` and press enter.
```
- nmap is the command to run
- sV option is set to version detection
- v option is to increase verbose level
- script nbtstat.nse is nmap script to enumerate
- [Target IP] which is target ip address
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/0b3f64de-8c15-4284-8927-66f2b4cdd0e7" width="400px" height="250px"><br>Figure (4) nmap enumeration results</p>

Another command to enumerate with specific port number, type ``` nmap -sU -p 137 --script nbstat.nse [Target IP Address] ``` and press enter.
```
- nmap is the command to run
- sU option is set to UDP port enumeration
- p option is set to specific prot number
- script nbtstat.nse is nmap script to enumerate
- [Target IP] which is target ip address
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/c958a50f-11be-4852-aef2-62ecc708d182" width="400px" height="250px"><br>Figure (5) nmap results</p>

## NetBIOS Enumeration with NetBIOS Enumerator 
Open NetBIOS Enumerator. And fill start ip address and end ip address to enumerate. And click scan.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/fd1c0f24-012d-4f33-9c4f-cacc12472b1a" width="400px" height="250px"><br>Figure (6) Provide IP Range</p>

The results will appears, we can see network resources and shares.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/76296a9b-3639-495f-89eb-80cb9c550cc5" width="400px" height="250px"><br>Figure (7) Scan Results</p>

## NetBIOS Enumeration with Soft Perfect Network Scanner 
Open Soft Perfect Network Scanner and provide ip range to scan. After adding ip range click start scan.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/ceb44f20-1131-4322-8bb9-7023e9726dd3" width="400px" height="250px"><br>Figure (8) Provide IP Range</p>
After scanning is complete all network devices shares can be seen.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/34211f10-288f-4997-afe6-4c496bf566bd" width="400px" height="350px"><br>Figure (9) Scan Results</p>

## Conclusion 

In this tutorial, NetBIOS Enumeration is performed by using different tools and techniques. Do more Practice and Expert it!. <br>
**1/27/2024** <br>
Contributed By - Jord@n
