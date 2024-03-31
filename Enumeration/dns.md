# DNS enumeration

DNS enumeration is the process of locating all the DNS servers and their corresponding records for an organization. DNS enumeration will yield usernames, computer names, and IP addresses of potential target systems.
The list of DNS record provides an overview of types of resource records (database records) stored in the zone files of the Domain Name System (DNS).

## DNS Zone Transfer

DNS Zone Transfer used to replicate DNS data across a number of DNS servers or to back up DNS files. A user or server will perform a specific zone transfer request from a ―name server.
If the name server allows zone transfers by an anonymous user to occur, all the DNS names and IP addresses hosted by the name server will be returned in human-readable ASCII text.

## Tools Requirements 
- [Nmap](https://www.nmap.org)
- [Dnsrecon](https://github.com/darkoperator/dnsrecon)
- [dig](https://www.kali.org/tools/bind9/#dig)
- [nslookup](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/nslookup)

## Lab Configuration 
- Windows-10
- kali-linux
- Internet

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/3a150c5e-ba83-4d01-acb9-b1a253e2892e" width="400px" height="250px"><br>Figure (1)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/25c52cdf-6d97-45fe-a374-5888c8b25815" width="400px" height="250px"><br>Figure (2)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9e6ac570-d804-42f7-b7e8-e8f36cb7fa61" width="400px" height="250px"><br>Figure (3)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/a7b4ca2e-8e0d-406e-9334-97763141fc00" width="400px" height="250px"><br>Figure (4)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/8fd6abf0-e3bf-4774-aba9-28c1d19c0de7" width="400px" height="250px"><br>Figure (5)</p>

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/14c864a5-e946-4163-98ac-3aac72f12d5d" width="400px" height="250px"><br>Figure (6)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/5941cada-ebf6-48e0-a891-399426d216cc" width="400px" height="250px"><br>Figure (7)</p>

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/95325488-ab47-45ca-bb5b-56551c7a683f" width="400px" height="250px"><br>Figure (8)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/582ff52b-a798-4103-973d-5476f9f3ae2b" width="400px" height="250px"><br>Figure (9)</p>

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7e7ec7f3-5ca1-4460-99d1-d80671e8a408" width="400px" height="250px"><br>Figure (10)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9847559a-02f7-48f5-a5e7-d30e796dcc82" width="400px" height="250px"><br>Figure (11)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1017f019-8c47-4481-978f-cde344950c10" width="400px" height="250px"><br>Figure (12)</p>
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/dc5ebb06-5d33-4715-ad9d-d89f98daac7d" width="400px" height="250px"><br>Figure (13)</p>

we are using -l option, which is another way to list all DNS records from a domain name.

```
┌──(root@kali)-[~]
└─$ host -t axfr zonetransfer.me nsztm2.digi.ninja.
Trying "zonetransfer.me"
Using domain server:
Name: nsztm2.digi.ninja.
Address: 34.225.33.2#53
Aliases:

;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 6107
;; flags: qr aa; QUERY: 1, ANSWER: 51, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;zonetransfer.me.               IN      AXFR

;; ANSWER SECTION:
zonetransfer.me.        7200    IN      SOA     nsztm1.digi.ninja. robin.digi.ninja.
zonetransfer.me.        300     IN      HINFO   "Casio fx-700G" "Windows XP"
zonetransfer.me.        7200    IN      MX      0 ASPMX.L.GOOGLE.COM.
zonetransfer.me.        7200    IN      MX      10 ALT1.ASPMX.L.GOOGLE.COM.
zonetransfer.me.        7200    IN      SOA     nsztm1.digi.ninja. robin.digi.ninja.
<!--------- snipp --------->
Received 2102 bytes from 34.225.33.2#53 in 269 ms
```

## Conclusion 

In this tutorial, NetBIOS Enumeration is performed by using different tools and techniques. Do more Practice and Expert it!. <br>
**3/31/2024** <br>
Contributed By - Jord@n
