```
Footprinting & Reconnaissance
│
│
│
├────── Types
│	│
│	├─── 1. Active Reconnaissance
│	├─── 2. Passive Reconnaissance
│
│
│
├─── Objectives
│	│
│	├─── 1. To get information
│	│		│
│	│		├─── Organiation information
│	│		│		├─── Employees Details
│	│		│		├─── Phone Numbers
│	│		│		├─── Branch & location
│	│		│		├─── Background of the org
│	│		│		├─── Web Technologies
│	│		├─── Network information
│	│		│		├─── Domain & Subdomains
│	│		│		├─── Network blocks
│	│		│		├─── Network Topology  
│	│		│		├─── IP Address
│	│		│		├─── DNS Records
│	│		├─── System information
│	│		│		├─── Web Server OS
│	│		│		├─── location of web server
│	│		│		├─── Email Address
│	│		│		├─── Usernames & passwords
│
│
│
├────── Tools
│	│
│	├─── 1. Search Engines
│	│	│
│	│	├─── Google Search Engine
│	│	│	├─── Google Dorking
│	│	│	│	├─── [allintitle:cyber security essentials]
│	│	│	│	├─── [allinurl:cyber security hacker] [site:microsoft.com -www]
│	│	│	│	├─── [cache:courses.stationx.net][link:stationx.net "kali purple"]
│	│	│	│	├─── [ext:php site:microsoft.com][map:1hackerrd]
│	│	│	│	├─── [filetype:pdf site:apple.com][related:stationx.net security]
│	│	│	│	├─── [info:stationx.net -site:stationx.net]
│	│	│	│
│	│	├─── Geolocation Search 
│	│	│	├─── googlemap
│	│	│	│	├─── [https://www.google.com/maps]
│	│	│	├─── wikimapia
│	│	│	│	├─── [https://wikimapia.org/]
│	│	│	├─── Browserleaks
│	│	│	│	├─── [https://browserleaks.com/ip]
│	│	│	├─── Satellites Pro
│	│	│	│	├─── [https://satellites.pro/]
│	│	│	├─── Geolocation-OSINT
│	│	│	│	├─── [https://github.com/cqcore/Geolocation-OSINT]
│	│	│	├─── License plates
│	│	│	│	├─── [http://worldlicenseplates.com/]
│	│	│	├─── Vehical search
│	│	│	│	├─── [https://carnet.ai/]
│	│	│	│
│	│	├─── Video Search Engines
│	│	│	├─── mattw
│	│	│	│	├─── [https://mattw.io/]
│	│	│	├─── Google videos
│	│	│	│	├─── [https://www.google.com/videohp]
│	│	│	├─── VideoReverser
│	│	│	│	├─── [https://www.videoreverser.com/]
│	│	│	├─── EZGif
│	│	│	│	├─── [https://ezgif.com/]
│	│	│	│
│	│	├─── FTP Search Engines
│	│	│	├─── searchftp
│	│	│	│	├─── [https://www.searchftps.net]
│	│	│	├─── FTP file search
│	│	│	│	├─── [https://www.freewareweb.com/]
│	│	│	│
│	│	├─── IOT Search Engines
│	│	│	├─── Shodan
│	│	│	│	├─── [https://www.shodan.io/]
│	│	│	├─── Censys
│	│	│	│	├─── [https://censys.io/]
│	│	│
│	├─── 2. Web Services
│	│	│
│	│	├─── Domains & Subdomains
│	│	│	├─── Pentest-Tools
│	│	│	│	├─── [https://pentest-tools.com]
│	│	│	├─── Netcraft
│	│	│	│	├─── [https://www.netcraft.com/tools/]
│	│	│	├─── Assetfinder
│	│	│	│	├─── [https://github.com/tomnomnom/assetfinder] 
│	│	│	├─── Sublist3r
│	│	│	│	├─── [https://github.com/aboul3la/Sublist3r]
│	│	├─── People Search Engine
│	│	│	├─── Peekyou 
│	│	│	│	├─── [https://www.peekyou.com/]
│	│	│	├─── pipl
│	│	│	│	├─── [https://pipl.com/]
│	│	│	├─── BeenVerified 
│	│	│	│	├─── [https://www.beenverified.com/]
│	│	│	├─── Intelius 
│	│	│	│	├─── [https://www.intelius.com/]
│	│	│	├─── Spokeo
│	│	│	│	├─── [https://www.spokeo.com/]
│	│	├─── Email hunting 
│	│	│	├─── Linkly
│	│	│	│	├─── [https://linklyhq.com/]
│	│	│	├─── theHarvester
│	│	│	│	├─── [https://github.com/laramies/theHarvester]
│	│	│	├─── Mailtrack
│	│	│	│	├─── [https://mailtrack.io/]
│	│	│	├─── Hunter.io
│	│	│	│	├─── [https://hunter.io/]
│	│	│	├─── Email Checker
│	│	│	│	├─── [https://email-checker.net/]
│	│	│	├─── Verify emailaddress
│	│	│	│	├─── [https://tools.emailhippo.com/] 
│	│	│	├─── Voilanorbert
│	│	│	│	├─── [https://www.voilanorbert.com/] 
│	│	│	├─── PhoneBook
│	│	│	│	├─── [https://phonebook.cz/] 
│	│	│	├─── eMailTrackerPro 
│	│	│	├─── Infoga
│	│	│	│	├─── [https://github.com/GiJ03/Infoga]
│	│	├─── Deep & Dark web
│	│	│	├─── Tor Project
│	│	│	│	├─── [https://www.torproject.org/download/]
│	│	│	├─── ExoneraTor
│	│	│	│	├─── [https://www.metrcis.torproject.org/]
│	│	│	├─── OnionLand search engines
│	│	│	│	├─── [https://onionlandsearchengine.com/]
│	│	│	├─── DeHashed tool
│	│	│	│	├─── [https://www.dehashed.com/]
│	│	│
│	├─── 3. Social Networking sites
│	│	│
│	│	├─── profile information
│	│	│	├─── theHarvester
│	│	│	│	├─── [https://github.com/laramies/theHarvester]
│	│	│	├─── Sherlock
│	│	│	│	├─── [https://github.com/sherlock-project/sherlock]
│	│	│	├─── UserReCon
│	│	│	│	├─── [https://github.com/vijaysahuofficial/UserReCon]
│	│	│	├─── Social Searcher
│	│	│	│	├─── [https://www.socialsearcher.com]
│	│	│	├─── followerwonk 
│	│	│	│	├─── [https://www.followerwonk.com]
│	│	│	├─── Hootsuite
│	│	│	│	├─── [https://www.hootsuite.com]
│	│	│	├─── Meltwater 
│	│	│	│	├─── [https://www.meltwater.com]
│	│	│
│	├─── 4. Website footprinting
│	│	│
│	│	├─── information
│	│	│	├─── ping
│	│	│	│	├─── [ping www.test.com -f -l 1500]
│	│	│	│	├─── [ping www.test.com -i 3]
│	│	│	│	├─── [ping www.test.com -i 2 n 1]
│	│	│	├─── photon 
│	│	│	│	├─── [https://github.com/s0md3v/Photon]
│	│	│	├─── Recon-ng
│	│	│	│	├─── [https://github.com/lanmaster53/recon-ng]
│	│	│	├─── Th3inspector
│	│	│	│	├─── [https://github.com/Moham3dRiahi/Th3inspector]
│	│	│	├─── Recon-dog
│	│	│	│	├─── [https://github.com/s0md3v/ReconDog]
│	│	│	├─── Reccoon
│	│	│	│	├─── [https://github.com/evyatarmeged/Raccoon]
│	│	│	├─── Central ops
│	│	│	│	├─── [https://centralops.net/]
│	│	│	├─── Website Informer
│	│	│	│	├─── [https://website.informer.com/]
│	│	│	├─── BuiltWith 
│	│	│	│	├─── [https://builtwith.com/]
│	│	│	├─── Wappalyzer
│	│	│	│	├─── [https://www.wappalyzer.com/]
│	│	│	├─── Whatweb
│	│	│	│	├─── [https://www.whatweb.net/] [https://www.kali.org/tools/whatweb/]
│	│	├─── Data Extractor
│	│	│	├─── Web Data Extractor
│	│	│	│	├─── [http://www.webextractor.com/wde.htm]
│	│	│	├─── HTTrack Website copier
│	│	│	│	├─── [https://www.httrack.com/]
│	│	│	├─── GRecon 
│	│	│	│	├─── [https://github.com/TebbaaX/GRecon]
│	│	│	├─── CeWL 
│	│	│	│	├─── [https://github.com/digininja/CeWL]
│	│	│	├─── ParseHub
│	│	│	│	├─── [https://www.parsehub.com/]
│	│	│	├─── SpiderFoot
│	│	│	│	├─── [https://github.com/smicallef/spiderfoot]
│	│	│	├─── Cyotek
│	│	│	│	├─── [https://www.cyotek.com/cyotek-webcopy/downloads]
│	│	│
│	├─── 5. Network footprinting
│	│	│
│	│	├─── DNS information
│	│	│	├─── nslookup
│	│	│	│	├─── [http://www.kloth.net/services/]
│	│	│	│	├─── [https://dnsdumpster.com/]
│	│	│	│	├─── [https://network-tools.com/]
│	│	│	├─── whois lookup
│	│	│	│	├─── [https://who.is/]
│	│	│	│	├─── [https://whois.domaintools.com/]
│	│	│	│	├─── [https://tamos.com/]
│	│	│	│	├─── [https://www.sabsoft.com/]
│	│	│	├─── Reverse IP Domain check
│	│	│	│	├─── [https://www.yougetsignal.com/] 
│	│	│	│	├─── [https://github.com/darkoperator/dnsrecon]
│	│	│	├─── DNS Records
│	│	│	│	├─── [https://centralops.net/]
│	│	│	│	├─── [https://securitytrails.com/]
│	│	│	│	├─── [https://dnschecker.org/]
│	│	│	├─── Certificate search
│	│	│	│	├─── [https://crt.sh/]
│	│	├─── Network Range
│	│	│	├─── traceroute / tracert
│	│	│	├─── Path Analyer Pro
│	│	│	│	├─── [https://path-analyzer-pro.software.informer.com/]
│	│	│	├─── VisualRoute
│	│	│	│	├─── [https://www.visualroute.com/]
│	│	│	├─── Traceroute NG
│	│	│	│	├─── [https://www.solarwinds.com/]
│	│	│	├─── ARIN
│	│	│	│	├─── [https://www.arin.net/]
│	│	│
│	├─── 6. OSINT Techniques
│	│	│
│	│	├─── Maltego Tool
│	│	│	├─── [https://www.maltego.com/downloads/]
│	│	├─── OSRFramework
│	│	│	├─── [https://github.com/i3visio/osrframework]
│	│	├─── FOCA Tool suite
│	│	│	├─── [https://github.com/ElevenPaths/FOCA]
│	│	├─── BillCipher Tool
│	│	│	├─── [https://github.com/bahatiphill/BillCipher]
│	│	├─── OSINT framework
│	│	│	├─── [https://osintframework.com/] 
│	│	├─── exif/exiftool
│	│	│	├─── [https://exiftool.org/] [https://exif.tools/]
│	│	├─── metagoofil
│	│	│	├─── [https://github.com/laramies/metagoofil]
│
│
│
├────── Threats
│	│
│	├─── Social Engineering
│	├─── System & Network Attacks
│	├─── Information Leakage
│	├─── Privacy Loss
│	├─── Corporate Espionage
│	├─── Business Loss
│
│
│
├─── Countermeasures
│	│
│	├─── Employees Access
│	│	├─── Restrict to access social networking sites from organization's network
│	│	├─── Educate employees to use pseudonyms on blogs, groups, and forums
│	│	├─── Educate employees about various social engineering tricks and risks
│	├─── Technical Control
│	│	├─── Configure web servers to avoid information leakage
│	│	├─── Encrypt and password protect sensitive information
│	│	├─── Disable directory listings in the web servers
│	│	├─── Use footprinting techniques to counter
│	├─── Administrative Control
│	│	├─── Configure web servers to avoid information leakage
│	│	├─── Limit the amount of information that you are publishing on the website/Internet
│	│	├─── Do not reveal critical information in press releases, etc.
│
│
│
```

## Conclusion 

Do more Practice and Expert it!. <br>
**2/28/2024** <br>
Contributed By - Jord@n
