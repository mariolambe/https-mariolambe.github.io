---
layout: post
title:  "How to Extract URLs from Webpages"
date:   2021-04-11 17:55:27 +0100
categories: seo

---

If you are wondering **how to extract URLs from any webpage**, for free, really fast you are in the right place!

**1. Extract URLs from webpages with addons:**

I can reccomend a really powerful Chrome addon called [Link Klipper](https://chrome.google.com/webstore/detail/link-klipper-extract-all/fahollcgofmpnehocdgofnhkkchiekoo?hl=en)

![Link-Klipper](https://user-images.githubusercontent.com/61537859/114427036-f9acb600-9bba-11eb-9c39-badb724132b5.jpeg)


This extension allows you to :
- Extract all the links on the webpage
- Store all the extracted links as a CSV file
- Custom drag a selectable area on the webpage from which all the links will be extracted


**2. Extract URLs from webpages with the terminal:**


That´s what you´ll need to do the magic:

- MAC
- termnial
- wget installed




First of all check if you already installed wget by running the following command:
```
$ wget -V
```
If it is not installed yet then install 
[Homebrew](https://brew.sh/) first:
```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Then you need to install wget:
```
$ brew install wget
```

Now you got everything you need to **extract URLs from a webpage** for free with only one single command:
```
$ wget --mirror --delete-after --no-directories https://www.the-page-you-wanna-crawl.com 2>&1 | grep '^--' | awk '{print $3}' | sort >extracted-URLs.txt
```

The command will export all the URLs in a txt file called extracted-URLs.txt (if you want you can also rename it).




This method was shared via Twitter by John Muller:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">wget --mirror --delete-after --no-directories <a href="https://t.co/qZfl6J344M">https://t.co/qZfl6J344M</a> 2&gt;&amp;1 | grep &#39;^--&#39; | awk &#39;{print $3}&#39; | sort &gt;urls.txt</p>&mdash; 🍌 John 🍌 (@JohnMu) <a href="https://twitter.com/JohnMu/status/1381158164243099652?ref_src=twsrc%5Etfw">April 11, 2021</a></blockquote> 




Have fun!
