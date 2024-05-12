#  Basic Shodan Searching
Shodan is a search engine for Internet-connected devices. Web search engines, such as Google and Bing, are great for finding websites.
But what if you're interested in measuring which countries are becoming more connected? Or if you want to know which version of Microsoft IIS is the most popular?
Or you want to find the control servers for malware? Maybe a new vulnerability came out and you want to see how many hosts it could affect?
Traditional web search engines don't let you answer those questions.
Shodan gathers information about all devices directly connected to the Internet.
If a device is directly hooked up to the Internet then Shodan queries it for various publicly-available information.
The types of devices that are indexed can vary tremendously: ranging from small desktops up to nuclear power plants and everything in between.

##  [Shodan](https://www.shodan.io/)
Access from here and register account.

Simply type `webcams` to find public cameras.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/7c77027b-d1a3-48ab-81af-de8e4ef3083f" width="500px" height="450px"><br> Figure (1)</p>

We can search open ports in public using `port:22` tag.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/d929ea28-f595-4cf8-a3df-24c284729449" width="500px" height="450px"><br> Figure (2)</p>

This is searching for port number `port:3389` tag.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/10f15278-f4e2-4c56-855a-8b93fb21be5e" width="500px" height="450px"><br> Figure (3)</p>

To search specific technology like `netgear` simply type there's results will appear.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/6e0a62b5-9b2c-44b4-9b48-b2a64166bb2f" width="500px" height="450px"><br> Figure (4)</p>

To find os version on the Internet using `os:windows xp` tag.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/99743fcb-1219-48a5-a4f1-18b2d0668dd2" width="500px" height="450px"><br> Figure (5)</p>

To find specific city or place use `city:yangon` tag.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/b23b7d1b-8d09-4bca-8d7a-a1297cec1cc9" width="500px" height="450px"><br> Figure (6)</p>

We can find using multipe search filters like `city:yangon Apache 2.2.3`.
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/54674882-a376-434f-99d2-800c21719a4e" width="500px" height="450px"><br> Figure (7)</p>

To find a specific hostname use `hostname:www.google.com` filters to search
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/26bfaccc-c3eb-4ade-9003-d70adc907763" width="500px" height="450px"><br> Figure (8)</p>

More shodan search filters are [here](https://www.shodan.io/search/filters)
<p align="center"><img src="https://github.com/AungZayMyo/Ethical-Hacking/assets/154745254/26501296-b118-461b-95d9-cdcf25704ebf" width="500px" height="450px"><br> Figure (9)</p>

## Conclusion 

In this tutorial, Shodan IoT search engine passive information gathering techniques are demostrated. Do more Practice and Expert it!. <br>
**5/12/2024** <br>
Contributed By - Jord@n
