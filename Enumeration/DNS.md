# DNS enumeration

DNS enumeration is the process of locating all the DNS servers and their corresponding records for an organization. DNS enumeration will yield usernames, computer names, and IP addresses of potential target systems.
The list of DNS record provides an overview of types of resource records (database records) stored in the zone files of the Domain Name System (DNS).

<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/dcc8e616-427e-43d9-b581-3fc4bfba04fc" width="500px" height="250px"><br>DNS</p>

## DNS Zone Transfer

DNS Zone Transfer used to replicate DNS data across a number of DNS servers or to back up DNS files. A user or server will perform a specific zone transfer request from a name server.
If the name server allows zone transfers by an anonymous user to occur, all the DNS names and IP addresses hosted by the name server will be returned in human-readable ASCII text.

## DNS Records Types
DNS records (aka zone files) are instructions that live in authoritative DNS servers and provide information about a domain including what IP address is associated with that domain and how to handle requests for that domain. These records consist of a series of text files written in what is known as DNS syntax. Following table shown most common different dns records types.

| Type | Description |
| --- | --- |
| A | The record that holds the IPv4 address of a domain |
| AAAA | The record that contains the IPv6 address for a domain |
| CNAME | Forwards one domain or subdomain to another domain, does NOT provide an IP address |
| MX | The record that contains directs mail to an email server |
| NS | Stores the name server for a DNS entry |
| TXT | Lets an admin store text notes in the record. These records are often used for email security |
| SOA | Stores admin information about a domain |
| SRV | Specifies a port for specific services |
| PTR | Provides a domain name in reverse-lookups |

## Tools Requirements 
- [Nmap](https://www.nmap.org)
- [Dnsrecon](https://github.com/darkoperator/dnsrecon)
- [dig](https://www.kali.org/tools/bind9/#dig)
- [nslookup](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/nslookup)

## Lab Configuration 
- Windows-10
- kali-linux
- Internet Connection

### Enumeration with dig

We can enumerate different dns records from specific server. Firstly, we will enumerate mail records using dig. Type following commands ``` dig mx [domain] ``` to extract mail records.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/9e6ac570-d804-42f7-b7e8-e8f36cb7fa61" width="400px" height="250px"><br>Figure (1) mail records </p>

To extract name servers from target dns use `ns` option and run following command ``` dig ns [Target_Domain_Name]```. And press enter name records will appear.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/3a150c5e-ba83-4d01-acb9-b1a253e2892e" width="400px" height="250px"><br>Figure (2) name servers records </p>

We will transfer zone using following commands ``` dig @[name_server_address] [domain] axfr ``` to enumerate all dns information.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/25c52cdf-6d97-45fe-a374-5888c8b25815" width="400px" height="250px"><br>Figure (3) transfer zone using dig </p>

## DNSSEC zone checking with dnsrecon
DNS Security Extensions (DNSSEC) is a new security protocol released in order to fix many of these shortcomings. DNSSEC helps to solve these issues by digitally signing responses while also maintaining backwards compatibility with the existing DNS implementation.
DNSSEC signs and protects all response types including IP addresses, TXT records and MX records. Each layer of the DNS lookup process is signed, this includes responses from the root nameserver to TLD nameservers, and TLD name servers to authoritative nameservers.

dnsrecon is python based tool to enumerate dns information. Type ``` python3 dnsrecon.py -d [domain] ``` to enumerate dns information. 
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/14c864a5-e946-4163-98ac-3aac72f12d5d" width="400px" height="250px"><br>Figure (4) DNSSEC zone is not configured</p>

dnsrecon has option `-z` to perform a DNSSEC zone walk with standard enumeration. To do that type ``` python3 dnsrecon.py -d [domain] -z ```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/5941cada-ebf6-48e0-a891-399426d216cc" width="400px" height="250px"><br>Figure (5)DNSSEC zone enumeration</p>

## Enumeration with nmap

This nmap script attempts to enumerate DNS hostnames by brute force guessing of common subdomains. To do that type ``` nmap --script dns-brute [domain] ```.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/95325488-ab47-45ca-bb5b-56551c7a683f" width="400px" height="250px"><br>Figure (6) dns brute force results </p>

This nmap script enumerates various common service (SRV) records for a given domain name. The service records contain the hostname, port and priority of servers for a given service. To do that type following commands ``` nmap --script dns-srv-enum --script-args "dns-srv-enum.domain=' [domain] '" ```.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/582ff52b-a798-4103-973d-5476f9f3ae2b" width="400px" height="250px"><br>Figure (7) results </p>

### Other nmap dns enumeration scripts

1. Retrieves information from a DNS nameserver by requesting its nameserver ID (nsid) and asking for its id.server and version.bind values
``` nmap -sSU -p 53 --script dns-nsid [target] ```


## Nslookup
The nslookup command-line tool is available only if you have installed the TCP/IP protocol. It Displays information that you can use to diagnose Domain Name System (DNS) infrastructure.

To extract soa records from specific server do following steps.
```
server 8.8.8.8 - which is set to dns server
set type=soa - which is set dns records type
[domain] - which is target domain
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7e7ec7f3-5ca1-4460-99d1-d80671e8a408" width="400px" height="250px"><br>Figure (8) SOA records results </p>

To extract all dns records from specific server do following steps.
```
set type=all - which is set dns records type
[domain] - which is target domain
```
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/dc5ebb06-5d33-4715-ad9d-d89f98daac7d" width="400px" height="250px"><br>Figure (9) results appear</p>

## Conclusion 

In this tutorial, DNS Enumeration is performed by using various tools and techniques. Do more Practice and Expert it!. <br>
**3/31/2024** <br>
Contributed By - Jord@n
