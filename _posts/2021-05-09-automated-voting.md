---
layout: single
title: "A Lazy K-drama Fan: Automated Voting with Selenium"

permalink: /projects/:title/
date: "2021-05-09"
author_profile: true
categories:
- Python
- Automation
excerpt: |
  Read about how I used Selenium to vote for my favourite Korean drama last year 📺
---

This post is about how I automated the voting process for my favourite Korean drama in this poll on [The Best Korean Drama 2020](https://kingchoice.me/the-best-korean-drama-2020-close-nov-30). At the time, I was looking for a mundane task to try automating after reading Al Sweigart's book, [*Automate the Boring Stuff with Python*](https://automatetheboringstuff.com/).

The plan was to vote for [Hospital Playlist](https://www.netflix.com/ca/title/81239224), a drama about five doctors who are friends from medical school. Perhaps I was particularly biased because they reminded me of myself and my four close friends from university!

![HP Poster](..\..\assets\images\2021-05-09-automated-voting\hospital_playlist_poster.jpg)

If I were to manually cast a vote for the drama, I would have needed to:
1. Go to the website
2. Scroll down to find the drama among 30 choices
3. Click on the green up arrow to cast a vote

![HP Voting](..\..\assets\images\2021-05-09-automated-voting\hospital_playlist_voting.png)

It seemed tedious and repetitive which was exactly why the task should be done by a machine. Luckily, *Automate the Boring Stuff with Python* has a section on [Clicking the Page](https://automatetheboringstuff.com/chapter11/#:~:text=clicking%20the%20page), so I set out to do just that - automate the boring stuff.

The book didn't have exactly what I was looking for but this [Selenium click button](https://pythonspot.com/selenium-click-button/) post did. The steps below are a modified version of the code found in that post.
 
## 1. Define Chrome Options
See list of Chromium command line switches at [this link](https://peter.sh/experiments/chromium-command-line-switches/).
```
# import dependencies
from selenium import webdriver
import time

# define options to pass in to Chrome driver
options = webdriver.ChromeOptions()
options.add_argument('--ignore-certificate-errors')
options.add_argument('--test-type')
options.binary_location = '/usr/bin/chromium'
```

## 2. Set Up Chrome Driver
Download `chromedriver.exe` from [Google here](https://sites.google.com/chromium.org/driver/). Unzip the file and set the `executable_path` as the file's location. In the example below, the driver is located in my Downloads folder.
```
driver = webdriver.Chrome(executable_path = r'C:\Users\Shannon\Downloads\chromedriver.exe')
```

## 3. Get HTML Source Code
Specify the URL.
```
driver.get('<paste URL here>')
```

## 4. Click Vote Button
Find the XPath the button to be clicked. I used Developer Tools to do this (see image below). A [quick Google search](https://www.google.com/search?q=how+to+find+xpath+in+chrome&oq=how+to+find+xpath&aqs=chrome.0.0j69i57j0l4j69i60l2.2344j0j9&sourceid=chrome&ie=UTF-8) will provide details and alternative methods for this.
![Find XPath](..\..\assets\images\2021-05-09-automated-voting\find_xpath.png)

Once the XPath is found, paste it into the `find_elements_by_xpath()` method.
```
vote_button = driver.find_elements_by_xpath('<paste XPath here>')[0]
vote_button.click()
```

After going through these steps, all I needed to do was run the script which would then help me go to the website and cast a vote!