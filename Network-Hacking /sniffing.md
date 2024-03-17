# Sniffing
Sniffing is the process of monitoring and capturing all the packets passing through a given network using sniffing tools. Sniffing can be either Active or Passive in nature.
Sniffing allows you to see all sorts of traffic, both protected and unprotected. There're many types of sniffing techniques & attacks.
In this tutorial, ARP Poisoning technique will demostrate.

## Protocols which are vulnerable to sniff the traffic
- HTTP − It is used to send information in the clear text without any encryption and thus a real target.
- SMTP (Simple Mail Transfer Protocol) − SMTP is basically utilized in the transfer of emails. This protocol is efficient, but it does not include any protection against sniffing.
- IMAP (Internet Message Access Protocol) − IMAP is same as SMTP in its functions, but it is highly vulnerable to sniffing.
- POP (Post Office Protocol) − POP is strictly used to receive emails from the servers. This protocol does not include protection against sniffing because it can be trapped.
- FTP (File Transfer Protocol) − FTP is used to send and receive files, but it does not offer any security features. All the data is sent as clear text that can be easily sniffed.
- Telnet − Telnet sends everything (usernames, passwords, keystrokes) over the network as clear text and hence, it can be easily sniffed.

## Prerequstite for this lab ##
- [Windows-7]()
- [Windows-10]()
- [Cain & Abel]()
- A Server with mail service

## Lab Configurations ##
- make sure hosts are in same network
- ping between hosts

### Do following steps to perform ARP Poisoning

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/0a4c6aeb-3e1b-491b-8a1c-c5f37faf9eba" width="450" height="300"/><br>Figure (1): Start Cain & Abel and configure device</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/4f15968f-f5d2-4122-9289-2e11a1823ab5" width="450" height="300"/><br>Figure (2): click shown on figure to enable offloading</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/8747b121-0f8b-4f54-ace3-fae850392364" width="450" height="300"/><br>Figure (3): navigate to sniffer tab and click plus sign and select range to assign network range </p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/aadf6e06-6d40-4c12-bb97-739cd211155a" width="450" height="300"/><br>Figure (4): we found hosts on our network</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/0df85d09-d373-4196-a413-65d3e7d48e39" width="450" height="300"/><br>Figure (5): goes to arp tab & click add to list </p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/07826af9-f8ea-4dd0-a238-650ee1fec679" width="450" height="300"/><br>Figure (6): select one ip and click ok</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/19ec617e-2f34-4eb7-8021-5fe87fcf317f" width="450" height="300"/><br>Figure (7): after that click on arp poision button</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/45e59298-4dab-4b7f-94ab-05e0503510ed" width="450" height="300"/><br>Figure (8): connect with ftp from any host to server</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/6b025c20-366a-4bf1-9370-d27a19943ef3" width="450" height="300"/><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/ed2385f5-cd66-438b-b620-7e00d334baba" width="450" height="300"/><br>Figure (9): goes to passwords tab & ftp usernames and passwords is shown </p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/3be21468-63df-4e39-b55e-7aad3316e412" width="450" height="300"/><br>Figure (10): connect with telent from any host to server</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/40f2ff8f-5a9c-4fda-9cbb-b9855770bae3" width="450" height="300"/><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d926e35e-4508-41ea-ae17-5859b75b3c58" width="450" height="300"/><br>Figure (11): click on telent tab & right click on any session and click view we got it</p>

# Conclusion
In this tutorial, ARP Poisoning attack is demostrated and sniffed credentials from netwrok traffic. Do more Practice and Expert it!. <br>
**3/17/2024** <br>
Contributed By - Jord@n
