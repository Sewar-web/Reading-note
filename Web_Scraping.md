
# How to Web Scrape with Python in 4 Minutes


**Web Scraping**

* Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. In this article, we will go through an easy example of how to automate downloading hundreds of files from the New York MTA. This is a great exercise for web scraping beginners who are looking to understand how to web scrape. Web scraping can be slightly intimidating, so this tutorial will break down the process of how to go about the process.


***Important notes about web scraping:***


1. Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.


2. Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.
Insp


**Inspecting the Website**
The first thing that we need to do is to figure out where we can locate the links to the files we want to download inside the multiple levels of HTML tags. Simply put, there is a lot of code on a website page and we want to find the relevant pieces of code that contains our data. If you are not familiar with HTML tags, refer to W3Schools Tutorials. It is important to understand the basics of HTML in order to successfully web scrape.
On the website, right click and click on “Inspect”. This allows you to see the raw code behind the site.



```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
soup = BeautifulSoup(response.text, “html.parser”)
soup.findAll('a')


```


**************


# Web Scraping


**Web scraping :** web harvesting, or web data extraction is data scraping used for extracting data from websites. The web scraping software may directly access the World Wide Web using the Hypertext Transfer Protocol or a web browser. While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler. It is a form of copying in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis.



* Web scraping a web page involves fetching it and extracting from it. Fetching is the downloading of a page (which a browser does when a user views a page). Therefore, web crawling is a main component of web scraping, to fetch pages for later processing. Once fetched, then extraction can take place. The content of a page may be parsed, searched, reformatted, its data copied into a spreadsheet or loaded into a database. Web scrapers typically take something out of a page, to make use of it for another purpose somewhere else. An example would be to find and copy names and telephone numbers, or companies and their URLs, or e-mail addresses to a list (contact scraping).

* Web scraping is used for contact scraping, and as a component of applications used for web indexing, web mining and data mining, online price change monitoring and price comparison, product review scraping (to watch the competition), gathering real estate listings, weather data monitoring, website change detection, research, tracking online presence and reputation, web mashup and, web data integration.

* Web pages are built using text-based mark-up languages (HT



****************

## How to scrape websites without getting blocked


***Respect Robots.txt***
Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior such as how frequently you can scrape, which pages allow scraping, and which ones you can’t. Some websites allow Google to scrape their websites, by not allowing any other websites to scrape. This goes against the open nature of the Internet and may not seem fair but the owners of the website are within their rights to resort to such behavior. 

You can find the robot.txt file on websites. It is usually the root directory of a website – http://example.com/robots.txt.

If it contains lines like the ones shown below, it means the site doesn’t like and does not want to be scraped.

```
User-agent: *

Disallow:/ 
```

*Here are a few easy giveaways that you are bot/scraper/crawler –*

* scraping too fast and too many pages, faster than a human ever can

* following the same pattern while crawling. For example – go through all pages of search results, and go to each result only after grabbing links to them. No human ever does that.

* too many requests from the same IP address in a very short time

* not identifying as a popular browser. You can do this by specifying a ‘User-Agent’.

* using a user agent string of a very old browser


**Make the crawling slower, do not slam the server, treat websites nicely**

Web scraping bots fetch data very fast, but it is easy for a site to detect your scraper as humans cannot browse that fast. The faster you crawl, the worse it is for everyone. If a website gets too many requests than it can handle it might become unresponsive.

Make your spider look real, by mimicking human actions. Put some random programmatic sleep calls in between requests, add some delays after crawling a small number of pages and choose the lowest number of concurrent requests possible. Ideally put a delay of 10-20 seconds between clicks and not put much load on the website, treating the website nice.



**Do not follow the same crawling pattern**

* Humans generally will not perform repetitive tasks as they browse through a site with random actions. Web scraping bots tend to have the same crawling pattern because they are programmed that way unless specified. Sites that have intelligent anti-crawling mechanisms can easily detect spiders by finding patterns in their actions and can lead to web scraping getting blocked.




**Make requests through Proxies and rotate them as needed**


- When scraping, your IP address can be seen. A site will know what you are doing and if you are collecting data. They could take data such as – user patterns or experience if they are first time users.

Multiple requests coming from the same IP will lead you to get blocked, which is why we need to use multiple addresses. When we send requests from a proxy machine, the target website will not know where the original IP is from, making the detection harder.

Create a pool of IPs that you can use and use random ones for each request. Along with this, you have to spread a handful of requests across multiple IPs.

There are several methods can be used to change your outgoing IP.

TOR
VPNs
Free Proxies
Shared Proxies – the least expensive proxies, shared by many users. Chances to get blocked are high.
Private Proxies – usually used only by you, and lower chances of getting blocked if you keep the frequency low.
Data Center Proxies, if you need a large number of IP Address and faster proxies, larger pools of IPs. They are cheaper than residential proxies and coulde be detected easily.
Residential Proxies, if you are making a huge number of requests to websites that block to actively. These are very expensive (and could be slower, as they are real devices). Try everything else before getting a residential proxy.
In addition, various commercial providers also provide services for automatic IP rotation. A lot of companies now provide residential IPs to make scraping even easier – but most are expensive.




**Rotate User Agents and corresponding HTTP Request Headers between requests**


A user agent is a tool that tells the server which web browser is being used. If the user agent is not set, websites won’t let you view content. Every request made from a web browser contains a user-agent header and using the same user-agent consistently leads to the detection of a bot. You can get your User-Agent by typing ‘what is my user agent’ in Google’s search bar. The only way to make your User-Agent appear more real and bypass detection is to fake the user agent. Most web scrapers do not have a User Agent by default, and you need to add that yourself.


```
curl 'https://scrapeme.live/shop/Ivysaur/' \
-H 'authority: scrapeme.live' \
-H 'dnt: 1' \
-H 'upgrade-insecure-requests: 1' \
-H 'user-agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_4) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.61 Safari/537.36' \
-H 'accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9' \
-H 'sec-fetch-site: none' \
-H 'sec-fetch-mode: navigate' \
-H 'sec-fetch-user: ?1' \
-H 'sec-fetch-dest: document' \
-H 'accept-language: en-GB,en-US;q=0.9,en;q=0.8' \
--compressed
```


**Use a headless browser like Puppeteer, Selenium or Playwright**

If none of the methods above works, the website must be checking if you are a REAL browser.

The simplest check is if the client (web browser) can render a block of JavaScript. If it doesn’t, then it pretty much flags the visitor to be a bot. While it is possible to block running JavaScript in the browser, most of the Internet sites will be unusable in such a scenario and as a result, most browsers will have JavaScript enabled.

Once this happens, a real browser is necessary in most cases to scrape the data. There are libraries to automatically **control browser such as  :**

1. Selenium
2. Puppeteer and Pyppeteer
3. Playwright
4. 