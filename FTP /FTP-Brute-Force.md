## FTP ###
FTP stands for File Transfer Protocol which is used for transferring files over network to upload and download files. There is a authentication process to sucessfully connect to FTP server. To do that usernames and passwords
are required. In this tutorial we will guess valid username and password by using brute force technique. Lets Start!.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/4b6ed6c9-cc6a-4147-acfa-c8e8cf66c919 width=450 height=300/><br>Figure (1)</p>

## Prerequstite for this Lab ##
- Server with FTP service
- Windows 7 (Optional)
- [Angry IP Scanner](https://github.com/angryip/ipscan)
- [Advanced Port Scanner](https://www.advanced-port-scanner.com/)
- [THC-Hydra Windows](https://github.com/maaaaz/thc-hydra-windows)
- Basic Network, Hacking Tools and FTP knowledge

## Step one ##
Firstly, we need to know our network information to do that goes to the windows command prompt and type ``` ipconfig ``` to see network information as shown in following figure.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d4a4d3b8-63e2-478a-a9bb-e99f0537efaa width=450 height=300/><br>Figure (2): Network Information </p>

## Step two ##
Once we know about our network information we need to find alive hosts in our network. To do that, there a scanning tool called Angry IP Scanner to scan our network.
Now Open Angry IP Scanner and add network range, in this case ``` 192.168.100.1-254  ``` is our target netowrk, and click scan.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/215446db-ed17-4c1a-97ff-5cbf0929f0d1 width=450 height=300/><br>Figure (3): Angry IP Scanner</p>

After Scanning is completed, there is a pop-up windows shows network report.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/60a84774-5e6f-47e3-9f6b-08d9320391f8 width=450 height=300/><br>Figure (4): Angry IP Scanner Report </p>

Scroll down to find the alive host in our network, We found a IP address with open port 80. That is our target IP address.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/8198dd58-d957-49f4-8f14-96432792adb0 width=450 height=300/><br>Figure (5): Angry IP Scanner</p>

## Step Three ##

To confirm this ip address is our target we need to start services and port scanning. To perform this scan we need to lunch Advanced Port Scanner to deep scan.
In Advanced Port Scanner, type our network range to deep scan in this scenario ``` 192.168.100.1-254  ``` is our network range and click scan.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9898bcd6-8238-49e3-8500-f9343cf9dca6 width=450 height=300/><br>Figure (6): Advanced Port Scanner</p>

After Scanning is completed, There is more details scanning results for our target ip address and there is port 21 FTP service is open. Our target is confirmed. 
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/f9eae029-cd23-4f8d-8cba-e076c63272b3 width=450 height=300/><br>Figure (7): Advanced Port Scanner Results </p>

To confirm whether FTP service is active or inactive, click ftp hyperlink in Advance port scanner. There is a authentication process to connect with FTP server.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/57a39a1e-07c8-4989-9fb1-df50c78639ee width=450 height=300/><br>Figure (8): FTP service is active </p>
We don't know username and password for authentication.

## Step Four ##
**Wordlists** <br>
Wordlists are collection of wellknown usernames and passwords to predict valid combination of username and password. Wordlists are most important in brute force attack. Wordlists can be created using various methods automatically or manually. In Hacking Operating Systems wordlists are created as a default feature. In this case we will create manually to do this lab. We need to create wordlists for both usernames and passwords.

<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/443f4f68-5078-4773-bdaa-fac9cbbc139e width=450 height=300/><br>Figure (9): Sample Wordlist </p>

After wordlist creation process is done, we will start brute-force attack. There are genreally two types of brute-frocing is available, online and offline brute forcing attack. Tools and techniques may differ dependings on types of attack. In this scenario, online brute-forcing technique will perform. To perform online brute force attack there's a tool called Hydra which is command line tool and it has ability to attack online brute-forcing.

To access Thc-Hydra, now go to the folder which is located Hydra and type following commmad.
``` hydra -L user.txt -P password.txt 192.168.100.152 ftp ``` and press enter.
- ``` hydra ``` to run hydra program
- ``` -L user.txt ``` option needs to provide wordlist of user file
- ``` -P password.txt ``` option neeeds to provide wordlist of password file
- ``` 192.168.100.152 ``` which is target IP address to attack
- ``` ftp ``` mean the types of service attack

After the brute forcing process is done, hydra is show valid username and password to connect with target. In this case, Username is ``` jordan ``` and Password is ``` asdfghjkl;' ```.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d113e00c-edf8-44a0-a377-0c737002a47b width=450 height=300/><br>Figure (10): THC-Hydra Online Brute Force Tool </p>

Once we got valid username and password, the last thing we need to do is to connect wth FTP server and access it's resources.
<p align="center"><img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/b97c32cf-faaf-4e4b-8963-6db0a4b30c2d width=450 height=300/>
<img src=https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/c876ca81-a174-44e2-b42a-0973ac6b8df8 width=450 height=300/><br>Figure (11): FTP site connect </p>

## Conclusion ##

In this tutorial, basic File Transfer Protocol (FTP) brute forcing lab is performed. Do more Practice and Expert it!. <br>
**12/27/2023**
