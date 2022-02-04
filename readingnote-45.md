# Reading 17 - Web Scraping

## Web Scrape with Python in 4 minutes

### Web Scraping

**web scraping** - access and extract large amounts of information from a website.
-download data

**IMPORTANT**:
1.most sites forbid the use of their data for commercial purposes
2.do not download data too rapidly because you may be blocked from the site.

#### Inspecting the website

-You want to grab specific doe that contains the desired data.
-find a tag html

### Python Code Import 

```python

  import requests
  import urllib.request
  import time
  from bs4 import BeautifulSoup

  url = 'http://web.mta.info/developers/turnstile.html'
  response = requests.get(url)
```

The output from the response should get a (200) status.

#### Parse

```python

  soup = BeautifulSoup(response.text, “html.parser”)
```

#### Find All Elements

```python

  soup.findAll('a')
```

#### Extract desired link

```python

  one_a_tag = soup.findAll(‘a’)[38]
  link = one_a_tag[‘href’]
```

#### Download Path

  download_url = 'http://web.mta.info/developers/'+ link
  urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])

#### Pause Code to Prevent Request Spam

```python
  time.sleep(1)
```

## What is Web Scraping?

**Fetch** - download a page

**Extraction** - parsed, searched or reformatted data

### Techniques

**Human copy-and-paste** - manually copying data and pasting it into a text file or spreadsheet.

**Text pattern matching** - search pattern found in Python.

**HTTP programming** - post HTTP requests using socket programming

**HTML Parsing** - query languages can "parse" HTML pages and fetch and alter page content.

**DOM Parsing** - parse through DOM manipulation

**Vertical Aggregation** - creates a plethora of "bots" for vertical without having personal interaction with a user/users.

**Semi annotation recognizing** - use semantic markups or annotations that can used to locate specific data.

### Methods to prevent web scraping

1.Block Ip address
2.disable exposed web service API
3.honeypot

## How to Scrap Data w/o getting blocked

No block = use **web crawlers**

*note* **Be Good and Follow Website's Crawling Process**

### Respect Robots.txt

Follow robot.txt file

Robot.text has guidelines to follow which helps crawling behavior.

**Detection**:
1.scrape too fast
2.frequent request in short time
3.user agent string of old browser
4.popular browser mis-identification

### Make Crawl Slower

Utilize auto throttling mechanisms.
-"throttles" crawling speed

### Don't follow same crawling pattern

Implement random clicks on page and random actions

### Request Rotation

Create pools of Ips and use random ones.

### Rotate User Agents

Don't send cookies unless scraper depends on cookies

### Beware of Honey Pot Traps

Links should have proper visibility with not *nofollow* tag.

[<==BACK](README.md)


