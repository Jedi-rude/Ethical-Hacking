# Anonymous Login through file sharing services
Anonymous login mean files and folders can be accessed not providing valid username and password. This vulnerability is come from server misconfiguration. 

## Prerequistite for this lab
- Ubuntu
- Kali linux
- vsftpd service
- samba service
- Nmap
- smbclient

## Lab Configuration 
we need to install and configure ftp service network file sharing services. First ftp server will be installed. To do that type following in ubuntu terminal.

```
sudo apt install vsftpd

```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/935ee111-0f1d-4b14-97c5-04035b048a8e" width="400px" height="250px"><br>Figure (1)</p>

After installation is done, we need to configure ftp server. now type following in ubuntu terminal.

```
sudo nano /etc/vsftpd.conf

```
Edit ` anonymous_enble=NO ` to ` anonymous_enble=YES `.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1cc21557-50b4-41ac-ad27-a90a84c4e4d2" width="400px" height="250px"><br>Figure (2)</p>
And go to the end of line, add following configurtion.

```
anon_root=/var/ftp/
no_anon_password=YES
hide_ids=YES
pasv_min_port=40000
pasv_max_port=50000
```
`anon_root` is place to access files. `no_anon_password` is configured no password reuire for anonymous login. 
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/425039c5-4686-42da-aa9f-a30f06edf103" width="400px" height="250px"><br>Figure (3)</p>

After ftp server is installed and configured we will install samba file sharing server. To do that type following in ubuntu terminal.
```
sudo apt install samba

```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/85c6171c-7e95-4a06-aeff-f995b87e892c" width="400px" height="250px"><br>Figure (4)</p>
We need to configure smb server, to do that type following in ubuntu terminl.

```
sudo nano /etc/samba/smb.conf

```

and insert following into end of line.

```
security = user
map to guest = bad user

[shares]
path = /var/www/
availble = yes
read only = no
browsable = yes
public = yes
writable = yes
guest ok = yes
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d0d7a0ce-1dc2-4f80-95a2-9122da3047b7" width="400px" height="250px"><br>Figure (5)</p>

## Let's start attack with ftp

we will start scan using `nmap`. Type `nmap -sC -p 21 [Target IP ]` to start scan and the results are appers.
```
nmap - is program to run
-sC - is default script scn
-p 21 - is specific port number
[Target IP ] - is target ip address
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/a2f43327-d060-4793-afc0-ec94d7ff559e" width="400px" height="250px"><br>Figure (6)</p>

Now we will connect to ftp server by uisng `ftp` command. Type `ftp [Target IP]`. 
```
ftp 192.168.161.136
username - Anonymous
ls
cd pub
ls
get welcome.txt
```
We got a successfully login without username and password.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/69516ac6-338c-4375-ae7b-2035b9634d20" width="400px" height="250px"><br>Figure (7)</p>

## Next we will attack Samba server

First start scan using `nmap`. `nmap -sS [Target IP] ` command to scan. Scanned results will appears.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/50f702e1-883d-4d59-baf4-935e4a6426f4" width="400px" height="250px"><br>Figure (8)</p>

We will enumerate sharing by using `smbclient` command. Type following in terminal `smbclient -L //[Target IP]`. We found shares on remote machine.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/25cee50c-2266-4436-b0e9-7a11085a3268" width="400px" height="250px"><br>Figure (9)</p>

Now we will access files under `shares`, using `smbclient //[Target IP]/shares` command. we got access.
```
ls
get [filename]
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/51709024-5146-4d81-8e19-337ab3493392" width="400px" height="250px"><br>Figure (10)</p>

## Conclusion 

In this tutorial, various anonymous login through network file sharing techniques are demostrated. Do more Practice and Expert it!. <br>
**2/14/2024** <br>
Contributed By - Jord@n
