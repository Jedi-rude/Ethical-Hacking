# Loging Form Brute Force with Burpsuite #
## Prereqstite for this lab ##
- [Burpsuite](https://portswigger.net/burp)
- [DVWA](https://github.com/digininja/DVWA)

## Lab Configuration ##
- Make sure DVWA is access on network
- Make sure two hosts are in same network
- Proxy configuration on local machine
- Turn on Burp Suite Interception 
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9ad0336c-9dbc-4cfc-96d8-d5c2440e99e2" width="450px" height="300px"><br>Figure (1) Ping Between Hosts</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/ddc3abe5-e13b-4f78-8440-123ec2fb544e" width="450px" height="300px"><br>Figure (2) Show IP</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/da060a11-6465-4826-b0a0-bca9caaf3fcb" width="450px" height="300px"><br>Figure (3) Configure Proxy</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/0f872e86-f04d-4338-ac84-9fa5dbbfba3d" width="450px" height="300px"><br>Figure (4) Configure IP and Port</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/51a6a89a-1f55-40fb-b0cf-6effef7e8680" width="450px" height="300px"><br>Figure (5) Turn Intercept on</p>

### Step-1 ###
Go to the browser and type DVWA IP in URL bar. Login form will be loaded. 
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/985503c8-a02d-437c-a7d6-e125f7446c87" width="450px" height="300px"><br>Figure (6)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/988f0262-6f78-40df-87a7-56521d3d099d" width="450px" height="300px"><br>Figure (7)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/5b40766b-644e-4308-9b9d-4999cddf774a" width="450px" height="300px"><br>Figure (8)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/f4c705da-de6c-4380-be24-5c60b868a298" width="450px" height="300px"><br>Figure (9)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9348beb7-4b19-4d41-b45b-3f872e5adb94" width="450px" height="300px"><br>Figure (10)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/c245e118-f1a5-456f-9157-e2037a979511" width="450px" height="300px"><br>Figure (11)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/97a6dda6-188e-481b-8806-85c0e593fde1" width="450px" height="300px"><br>Figure (12)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7fd749a6-c20b-4479-acdf-e3681d8f038f" width="450px" height="300px"><br>Figure (13)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/198c7c8b-fe03-48b1-8a4f-374498f91630" width="450px" height="300px"><br>Figure (14)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/6524682a-c21c-4920-8c3a-591b752c0e57" width="450px" height="300px"><br>Figure (15)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/903ed7e6-aea7-4bda-aac7-cc4924c8933c" width="450px" height="300px"><br>Figure (16)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/cfafb810-9d23-4369-b917-157a13ee1c4e" width="450px" height="300px"><br>Figure (17)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/b28df5e9-da01-4e2e-b864-abb4aedf090c" width="450px" height="300px"><br>Figure (18)</p>
