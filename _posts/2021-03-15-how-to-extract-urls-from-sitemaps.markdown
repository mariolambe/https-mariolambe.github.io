---
layout: post
title:  "How to Extract URLs from Sitemaps"
date:   2021-03-15 16:41:27 +0100
categories: jekyll update
---
[Last update: 12/2020]

If you are wondering how to extract sitemap URLs really fast you are in the right place!

There are different options out there and I selected the best 3 methods:

- Google Sheets
- Screaming Frog
- Terminal
- Let’s jump right into it.



1) Extract URLs From XML Sitemaps Online In Google Sheets

I found a simple sitemap url extractor script that will extract the list of URLs in less than 5 seconds, pretty impressive, isn’t it? Give it a try.

[Here the Google Sheet that act as a sitemap url extractor:]: [https://docs.google.com/spreadsheets/d/1-QiRWQVHqg7nL56Uwy_kqHt8i53oaq4yvG7duGIW3C4/copy]

1. Make a copy of it

2. Add the sitemap URL in the cell B2 (example: https://www.google.com/sheets/sitemaps.xml)

3. The list of URLs will appear automatically in column D

4. Done! You have just converted your sitemap to a URL list.


2) Extract URLs From XML Sitemaps with Screaming Frog
For this second method you need to install the SEO software Screaming Frog to convert any sitemap xml to a url list. This method works pretty well also for sitemap index file that are the ones that contain list of sub-sitemaps.

Here the steps:

1. Open Screaming Frog SEO Spider Tool

2. Mode>Select List

3. Upload>Download Sitemap>Add Sitemap xml URL

4. Done!


3) Extract URLs From XML Sitemaps with command line tools
1. Open your terminal

2. Enter this command (remember to replace the sitemap URL)-> curl -s https://www.google.com/sheets/sitemaps.xml

3. Done!


I hope you find it useful.


