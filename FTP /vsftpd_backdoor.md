# vsftpd version 2.3.4 Backdoor exploit #

Vsftpd is File transfer service which is vulnerable to attack backdoor command execution. In this lab we will exploit this vulnerability.

## Prerequstite for this lab ##
- [DVWA](https://github.com/digininja/DVWA)
- [Parrot Security Os]()
- [Nmap](https://www.nmap.org)
- [Metasploit]()

## Lab Configuration ##
- make sure hosts are in same network
- ping between hosts

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/74c60a7e-4a8f-4bf9-86a7-2fc47fc8039a" width="400px" height="250px"><br>Figure (1) Lab Configuration</p>

Run nmap to know what version of the server, which ports are open and what are vulnerable to attack. To do that, open mate terminal and type ``` nmap -sS -Pn -sV [Target IP Address] ``` and press enter.
```
- nmap is command  to run
- sS option is set to stealth scan
- sV flag is to set version detection scan
- Pn skip ping scan type
- [Target IP ] which is target IP
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/a89adcd7-e139-4154-925a-8a06053c3994" width="400px" height="250px"><br>Figure (2) Nmap scan results</p>

We got vsftpd version is  ``` 2.3.4 ```. Go to Metasploit console by typing msfconsole.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/adc5df6b-36b9-43f6-bc60-9fb1a1fdc874" width="400px" height="250px"><br>Figure (3) Metasploit Framework</p>

And after that search exploit module in metasploit console type ``` search vsftpd ``` and results will appears.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/8bddc371-557e-416f-b0d3-860415216fb2" width="400px" height="250px"><br>Figure (4) Exploit module</p>

To use exploit type ``` use 0 ``` to interact with exploit. After that type ``` show options ``` to see what information need to provide.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d04b85b5-40ad-48c0-a1d6-c77abf517d67" width="400px" height="250px"><br>Figure (5) Show options </p>

To start exploit we need to provide who is our target to do that ``` set RHOST [Target IP] ```. And to start attack type ``` exploit ```.
```
- set RHOST [Target IP] is always victim ip address
- exploit command is to start attack
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/2e42f766-6c24-4ddf-8c06-094267b76bf5" width="400px" height="250px"><br>Figure (6) Options configuration</p>

After that, exploit is running and completed. Type ``` ls ``` to know what we have.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/64a09598-31c0-4dcf-9d48-f528e79fa48c" width="400px" height="250px"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/f4e272fe-5429-47ed-a19b-e6ab950c6ba6" width="400px" height="250px"><br>Figure (7)</p>

## Conclusion ##

In this tutorial, vsftpd version 2.3.4 is exploited by using Metasploit and nmap. Do more Practice and Expert it!. <br>
**1/27/2023** <br>
Contributed By - Jord@n
