---
layout: post
title:  "Web Scraping Project"
author: Christina
# categories: [ Jekyll, tutorial ]
# tags: [red, yellow]
categories: [ Project ]
image: assets/images/news_article.png
description: ""
featured: true
hidden: true
comments: false
---

# Web Scraping Demo

You can view the app version of this project, which I built and is hosted on the Shiny Server. Please access it through this link: 

[Web Scraping Project](https://christina-gao.shinyapps.io/Web_Scraping_Project/)


## Part 1 - Scraping News Articles 

In Part 1, I used 2 packages in Python to scrape news articles relating to Car Wash Chains Industry Trends in the U.S.. The packages I used are Ntlk and Newspaper3k. Within a few lines of codes, I was able to extract and retrieved the title, author(s), date published, the full article in text, a summary, and top keywords. This is a relatively simple Neural Language Processing(NLP) I am using, but the main idea behind NLP is that it is using language models to map words into vector component and that's why it was able to correctly retrieved the information I need. 

<figure align="center">
  <img width="1500" height="700" src="/assets/images/news_article.png">
  <figcaption>Selected News Articles</figcaption>
</figure>

## Part 2 - Scraping A List of Top Car Wash Chains 

In this section, I used rvest package in R to scrape a list of top 50 car wash chains I found on carwash.com. This scraping can also be done using packages like BeautifulSoup in Python. 

<figure align="center">
  <img width="1200" height="600" src="/assets/images/top50_list.png">
  <figcaption>Top 50 Car Wash Chains in the U.S.</figcaption>
</figure>

## References

[Newspaper3k Documentation](https://newspaper.readthedocs.io/en/latest/)

[rvest Documentation](https://cran.r-project.org/web/packages/rvest/rvest.pdf)

[Top 50: Tracking Industry Trends Summary](https://www.carwash.com/top-50-tracking-industry-trends/)

[2022 M&A Predictions](https://www.carwash.com/2022-ma-predictions/)

[Promoting 101: How to Advertise Your Carwash](https://www.carwash.com/promoting-101-advertise-your-carwash/)

[Car Wash Offers a Growing Revenue Stream for Retailers](https://cstoredecisions.com/2022/03/09/car-wash-offers-a-growing-revenue-stream-for-retailers/)

[Top 50 U.S. Conveyor Chain List](https://www.carwash.com/top-50-u-s-conveyor-chain-list/)

<!-- ```html
---
layout: post
title:  "Inception Movie"
author: Christina
# categories: [ Jekyll, tutorial ]
tags: [red, yellow]
image: assets/images/11.jpg
description: "My review of Inception movie. Actors, directing and more."
rating: 4.5
---
``` -->
