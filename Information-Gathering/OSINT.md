#  OSINT
Open-Source Intelligence [OSINT](https://www.sans.org/blog/what-is-open-source-intelligence/) is defined as intelligence produced by collecting, evaluating and analyzing publicly available information with the purpose of answering a specific intelligence question.
Open-source information is content that can be found from various sources such as:

OSINT Sources
- Public Records
- News media
- Libraries
- Social media platforms
- Images, Videos
- Websites
- The Dark web

Who Uses OSINT?
- Government
- Law Enforcement
- Military
- Investigative journalists
- Human rights investigators
- Private Investigators
- Law firms
- Information Security
- Cyber Threat Intelligence
- Pen Testers
- Social Engineers

There are mainly two types of OSINT gathering techniques which are active & passive gathering. Following figure shows main difference between active & passive.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/1c787a66-1556-425b-b178-6e1fe3a4a5cc" width="400px" height="200px"></p>


##  Email Address Hunting
Email hunting refers to the process of finding and gathering email addresses for the purpose of reaching out to potential customers, clients, or contacts.
This can be done for various reasons, including marketing, sales, networking, or recruitment. Following websites are best email hunting tools for OSINT gathering.
- `https://www.findthatemail.io/`
- `https://hunter.io/`
- `https://www.voilanorbert.com/`
- `https://findthatlead.com/en/lead-search/`
- `https://anymailfinder.com/`
- `https://getemail.io/`
- `https://name2email.com/`
- `https://clearbit.com/resources/tools/connect`

##  Google Dorking
Google Dorking, also known as Google Hacking, is a technique that uses advanced search operators in Google Search to find specific information or vulnerabilities on websites.
This method leverages Google's powerful search capabilities to discover hidden data, sensitive information, or security flaws that might not be easily accessible through regular browsing.

Basic Search Operators

- site: Restricts search results to a specific domain.
  - `Example: site:example.com`
- intitle: Searches for pages with a specific word in the title.
  - `Example: intitle:"index of"`
- inurl: Searches for URLs containing a specific word.
  - `Example: inurl:admin`

Combining Operators

- Finding Login Pages
  - `Example: intitle:"login" OR inurl:"login"`
- Searching for Specific File Types
  - `Example: filetype:pdf site:example.com`
- Discovering Index Pages
  - `Example: intitle:"index of" "parent directory"`

Intermediate Techniques

- Finding Sensitive Directorie
  - `Example: intitle:"index of" "backup"`
- Locating Configuration Files
  - `Example: filetype:ini inurl:config`
- Exposing Admin Panels
  - `Example: inurl:admin intitle:login`
- Finding Passwords
  - `Example: intext:"password" filetype:log`
- Finding Email Lists
  - `Example: filetype:xls inurl:"email"`
- Discovering SQL Dumps
  - `Example: filetype:sql "sql dump"`
- Finding Exposed Cameras
  - `Example: intitle:"Live View / - AXIS"`
- Exposing FTP Servers
  - `Example: intitle:"index of" inurl:ftp`
- Searching for Vulnerable Websites
  - `Example: inurl:"php?id="`

##  Shodan
Shodan is a search engine specifically designed to locate and index internet-connected devices.
Unlike traditional search engines that index the web for websites and pages, Shodan indexes information on various types of devices, such as servers, routers, webcams, smart TVs, industrial control systems, and more.
It gathers data on these devices' open ports, services running, software versions, and any banners or responses they send back.

A "Shodan dork" is a search query used in Shodan to find specific types of devices or vulnerabilities. Here are some examples of Shodan dorks:

- Finding Webcams
  - `Example: webcamxp`
- Discovering Unsecured Routers
  - `Example: Netgear R7000`
- Exposing Industrial Control Systems (ICS)
  - `Example: port:502 modbus`
- Locating Databases
  - `Example: port:27017 MongoDB`
- Finding Printers
  - `Example: port:9100 banner:hp`
- Identifying Vulnerable SSH Servers
  - `Example: port:22 "OpenSSH 7.2"`
- Finding Cisco Devices
  - `Example: cisco-ios`
- Discovering Unprotected Redis Databases
  - `Example: port:6379 "redis"`

##  IP Address & Domain names
IP Address and domain information are crucial components of the internet's structure, providing details about the ownership, location, and technical characteristics of websites and online services.
This information is often used for network troubleshooting, cybersecurity assessments, and general informational purposes.

IP information includes details about a specific IP address, such as:
- Geolocation: Physical location associated with the IP address.
- ISP (Internet Service Provider): The service provider managing the IP address.
- ASN (Autonomous System Number): A collection of IP addresses managed by a network operator.
- Blacklist Status: Whether the IP address is listed on spam or abuse databases.

Domain information includes details about a specific domain name, such as:
- WHOIS Data: Registration details, including the owner, registration date, expiration date, and contact information.
- DNS Records: Information about the domain's DNS configuration, including A records, MX records, NS records, and TXT records.
- SSL Certificate Details: Information about the domain's SSL certificate, including issuer, expiration date, and any associated subdomains.

WHOIS Lookup Tools
- `https://www.whois.net/`
- `https://lookup.icann.org/`

IP Geolocation Tools
- `https://ipinfo.io/`
- `https://www.maxmind.com/en/geoip-demo`

DNS Lookup Tools
- `http://www.dnsstuff.com/`
- `https://mxtoolbox.com/`

SSL Certificate Tools
- `https://censys.io/`
- `https://www.ssllabs.com/ssltest/`

Blacklist and Abuse Check Tools
- `https://www.site24x7.com/tools/blacklist-check.html`
- `https://dnschecker.org/ip-blacklist-checker.php`

##  Metadata
Metadata is data that provides information about other data. It helps describe the content, context, and structure of the primary data, making it easier to organize, find, and understand.
Metadata can include details such as the creation date, author, file size, format, and other attributes that describe the characteristics of the data.

- ExifTool
    - Website: [ExifTool](https://exiftool.org/)
- MetaPicz
    - Website: [MetaPicz](http://www.metapicz.com/)
- Get-Metadata
    - Website: [Get-Metadata](https://www.metadata2go.com/)
- Exif.regex.info
    - Website: [Exif.regex.info](http://regex.info/blog/other-writings/online-exif-image-data-viewer)
- Apache Tika
    - Website: [Apache Tika](https://tika.apache.org/)
