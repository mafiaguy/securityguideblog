---
title: Google Dorking
date: "2020-07-28"
---
Inorder to acess this room log onto https://tryhackme.com/room/googledorking
Explaining how Search Engines work and leveraging them into finding hidden content!

[Task 1] Ye Ol' Search Engine

simply click complete
 
[Task 2] Let's Learn About Crawlers

1	
Name the key term of what a "Crawler" is used to do
index

2	
What is the name of the technique that "Search Engines" use to retrieve this information about websites?
crawling

3	
What is an example of the type of contents that could be gathered from a website?
keywords

[Task 3] Enter: Search Engine Optimisation
1	
Using the SEO Site Checkup tool on "tryhackme.com", does TryHackMe pass the “Meta Title Test”? (Yea / Nay)
yea

2	
Does "tryhackme.com" pass the “Keywords Usage Test?” (Yea / Nay)
nay

3	
Use https://neilpatel.com/seo-analyzer/ to analyse http://googledorking.cmnatic.co.uk:
What "Page Score" does the Domain receive out of 100?
85/100

4	
With the same tool and domain in Question 3 (previous):
How many pages use “flash”
0

5	
From a "rating score" perspective alone, what website would list first?
tryhackme.com or googledorking.cmnatic.co.uk
Use tryhackme.com's score of 62/100 as of 31/03/2020 for this question.
googledorking.cmnatic.co.uk


[Task 4] Beepboop - Robots.txt
1	
Where would "robots.txt" be located on the domain "ablog.com"
ablog.com/robots.txt

2	
If a website was to have a sitemap, where would that be located?
sitemap.xml

3 How would we only allow "Bingbot" to index the website?
User-Agent: Bingbot

4	
How would we prevent a "Crawler" from indexing the directory "/dont-index-me/"?
Disallow: /dont-index-me/

5	
What is the extension of a Unix/Linux system configuration file that we might want to hide from "Crawlers"?
.conf


[Task 5] Sitemaps
1	
What is the typical file structure of a "Sitemap"?
xml

2	
What real life example can "Sitemaps" be compared to?
map

3	
Name the keyword for the path taken for content on a website
route

[Task 6] What is Google Dorking?
1	
What would be the format used to query the site bbc.co.uk about flood defences
site: bbc.co.uk flood defences

2	
What term would you use to search by file type?
filetype:

3	
What term can we use to look for login pages?
intitle: login
