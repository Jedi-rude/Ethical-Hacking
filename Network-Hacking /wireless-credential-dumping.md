# Wireless Credential dumping with various techniques
Wireless credentials are entry point for wirelessnetworks, nowadays wireless networks are widey developed and used by organizations. There're Multiple ways to view credentials using command line or GUI or kind of executable file.

## Prerequstite for this lab
- must have wireless adapter
- windows os
- 

### Method one

Wireless credential files are stored on following directory in microsoft windows. ` ProgramData\Microsoft\Wlansvc\Profiles\interfaces `. 
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/3a1b11e1-06dc-4e9b-a6f0-e0b9dbba99d5" width="450px" height="300px"><br>Figure (1)</p>

To dump wireless networks `netsh` can view that wireless adapter is connected on current or past. Command to dump type following in command prompt.
`netsh wlan show profiles`.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/40ab305d-64c2-40c8-ad2f-738ebbd57aaa" width="450px" height="300px"><br>Figure (2) list of profiles</p>

To see passwords for each wireless network use following command syntax. `netsh wlan show profiles name="SSID" key=clear`.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d0b279e1-1755-409d-9bbf-9f2c46cf01eb" width="450px" height="300px"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/5740ebec-d17b-4aad-ae10-6792d2bbe203" width="450px" height="300px"><br>Figure (3)key content is passkey</p>

### Method two

Type following in run box `ncpa.cpl` and then right click on  wireless adapter and then click on status.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/fdec68ea-6413-4d65-ae68-8d1f93d901ff" width="450px" height="300px"><br>Figure (4)</p>

Now click on wireless  properties and go to security tab and then check on show characters.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/528df102-9304-4da4-83b8-baf22e06e9cf" width="450px" height="300px"><br>Figure (5)</p>

## Conclusion 

In this tutorial, wireless credentails dumping with various techniques are shown. Do more Practice and Expert it!. <br>
**2/24/2024** <br>
Contributed By - Jord@n
