# SMB over Networkshare port 139 exploit 

## Lab Configuration
- make sure two hosts are in same netwrok
- ping between hosts

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/62573a00-bf13-4f36-bd0d-ee0203f6b71f" width="400px" height="250px"><br>Figure (1) Configuration</p>

## Prerequstite for this lab
- [Metasploitable-2]()
- [Parrot Os]()
- [Metasploit Framework]()
- [Nmap](https://www.nmap.org)

### First
Only thing we need to do is scan. So open mate terminal and type ``` nmap -sS -sC -Pn -p- [Target IP Address] ```.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/a2248acd-0021-431b-9646-9816d1d016f5" width="400px" height="250px"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7507a6c3-4284-4843-90c5-a3007f6a3dd1" width="400px" height="250px"><br>Figure (2) Scanning Results</p>

Now go to Metasploit Console, to do that type ``` msfconsole ``` in mate termoinal. And then search scanner for smb version, type ``` search /scanner/smb ```.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1f9dc0e2-a57a-4ba4-9816-dcbfc82b2ccb" width="400px" height="250px"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/e0683b6b-33d4-453a-956c-6bca981ba9d6" width="400px" height="250px"><br>Figure (3) Modules Results</p>

We will use Module No.12 to start scan to do that type ``` use 12 ``` and type ``` show options ``` to see options.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1813ca5a-d392-4ca9-a943-059af575ee8d" width="400px" height="250px"><br>Figure (4) Show Options</p>

We need to provide Target IP address via RHOST to start scan. ``` set RHOST [Target IP Address] ``` and type ``` exploit ```.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/f99dcffb-f1d8-40b0-97ea-ef9aecdda347" width="400px" height="250px"><br>Figure (5) Start scan</p>

Now we have identified Samba version number. Type ``` sessions -i ``` to see active sessions. We don't have any active sessions yet.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7b1e56ca-9054-4a5b-b91e-9e6ee041533d" width="400px" height="250px"><br>Figure (6) Results</p>

To gain shell access we need to use exploit module to do that type ``` back ``` and type again ``` use exploit/ ```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/bd4ab13d-cc2c-42d8-b35d-9c33e321b09d" width="400px" height="250px"><br>Figure (7)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/472d1862-898b-4df3-9919-b3cd3d0d8a57" width="400px" height="250px"><br>Figure (8)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/f77cfd59-7bb2-4bfb-8b31-4c668fab4626" width="400px" height="250px"><br>Figure (9)</p>

In this tutorial, SMB over Networkshare via port 139 exploit is demostrated. Do more Practice and Expert it!. <br>
**1/29/2024** <br>
Contributed By - Jord@n
