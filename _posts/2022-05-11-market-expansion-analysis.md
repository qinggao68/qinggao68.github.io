---
layout: post
title:  "Market Expansion Analysis"
author: Christina
categories: [ Project ]
image: assets/images/strategy.jpg
featured: true
hidden: true
comments: false
---

# Brookdale Senior Living - Market Expansion Analysis

You can view the app version of this analysis, which I built and is uploaded to the Shiny Server. Please access it through this link: 

[Market Expansion Analysis of Brookdale Senior Living](https://christina-gao.shinyapps.io/Brookdale-Senior-Living-Market-Expansion-App/)

---

The purpose of this project is to perform location analysis using US Census Bureau datasets to locate white-space opportunities. This project may serve more purpose for (service-based) companies, whose strategic rationales for M&A initiatives centered around factors like #s of population, #s of elderly population, median income, projected growth rate of population(elderly), % of insured, proximity to existing locations/sites, and etc, when looking for the best market to expand. In my project, I used the longitude & latitude provided in the dataset I found on Homeland Infrastructure Foundation-Level and packages in R to map out the locations.

This dataset contained information about Brookdale Senior Living's existing locations. Here is a screenshot of the dataset.  

<figure align="center">
  <img width="1000" height="151" src="/assets/images/brookdale_dataset.PNG">
  <figcaption>Top 8 Observations of Brookdale Dataset</figcaption>
</figure>

In this dataset, there is a total of **776 observations(facilities)**. 

## Step 1: Map Out the Closed Facilities

I used the longitude & latitude to map out the closed facilities and display them on a map layout created using the leaflet package in R.

<figure align="center">
  <img width="700" height="500" src="/assets/images/closed_facilities.PNG">
  <figcaption>Closed Facilities Only</figcaption>
</figure>

From here, we can see there are: 
- 6 closed facilities near Washington D.C.
- 6 closed facilities in Panhandle Texas
- 11 closed facilities in Washington State
- 2 closed facilities in California

A total of **25 facilities** have been closed. 

Since I didn't want to include the closed facilities in determining the next market for Brookdale to expand into, I removed all data points of the closed facilities.  

## Step 2: Map Out the Open Facilities

Similar to mapping out the closed facilities, I used the longtitude & latitude that are provided in the dataset to map out only the open facilities. 

<figure align="center">
  <img width="700" height="500" src="/assets/images/open_facilities.png">
  <figcaption>Open Facilities Only</figcaption>
</figure>

There are still **751 open facilities**. According to this dataset, Brookdale has a market presence in 36 states, with the most market presence in the following: 

<figure align="center">
  <img width="400" height="400" src="/assets/images/top10_presence.png">
  <figcaption>Top 10 States with Most Market Presence</figcaption>
</figure>


## Step 3: Identify Potential White-Space Opportunities 

After identifying the states where Brookdale has a market presence, I then proceeded to find states where Brookdale has yet any market presence. I found that there are 14 states and they are: Arkansas, Hawaii, Iowa, Maine, Mississippi, Nevada, New Hampshire, New Mexico, North Dakota, Oregon, Pennsylvania, South Dakota, and Vermont. 

Then, I conducted some market research about the elderly population and senior facilities. I found that OR is one of the states that meet both of these criteria in terms of having a higher projection of growth in a rise of elderly population and usage of senior living facilities.  

References: 

[States Where Seniors Use Assisted Living the Most](https://seniorhousingnews.com/2016/09/25/states-seniors-use-assisted-living/)

[Which U.S. States Have the Oldest Populations?](https://www.prb.org/resources/which-us-states-are-the-oldest/)

## Step 4: API US Census Bureau Dataset

Then, I API the 5-year ACS for 2015-2019 dataset from the US Census Bureau to map out the projected elderly population in OR. I chose this dataset, because it has the smallest margins of error as compared to the 1-year. 

This is what the dataset looks like:

<figure align="center">
  <img width="1000" height="500" src="/assets/images/census_data.png">
  <figcaption>Top 10 Observations of US Census Bureau's Projection of Elderly Population</figcaption>
</figure>

Next, I used the leaflet package to map out the estimated elderly population of OR. We can see that Multnomah County and Washington County have the highest projected elderly population. 

<figure align="center">
  <img width="700" height="500" src="/assets/images/est_OR.png">
  <figcaption>US Census Bureau Estimation of Elderly Population in OR Only</figcaption>
</figure>


## Step 5: Proposed Potential Locations 

After identifying the two potential markets, I created a dataset that includes the longitude & latitude of Multnomah County and Washington County and loaded the dataset into RStudio. Then, I combined this dataset with the other dataset that includes Brookdale's open facilities and mapped only the surrounding states of OR. I also drew a circle radius surrounding the proposed counties, in which Brookdale could look further into these two areas.

<figure align="center">
  <img width="700" height="500" src="/assets/images/final_rec.png">
  <figcaption>Proposed Two Locations</figcaption>
</figure>

I believe this project can serve multiple purposes, whether a company is exploring potential markets or interesting in de-novo development. 

## References
[Homeland Infrastructure Foundation-Level Data (HIFLD) database - Nursing Homes](https://hifld-geoplatform.opendata.arcgis.com/datasets/geoplatform::nursing-homes/about)

[Leaflet for R Documentation](https://rstudio.github.io/leaflet/choropleths.html)

[Tidycensus Documentation](https://walker-data.com/tidycensus/articles/basic-usage.html)


<!-- ## Final Thoughts -->

<!-- I believed this project can serve multiple purposes, whether a company is exploring potential markets or interesting in de-novo development. We can use the internal data about the company's locations, map out using leaflet package, and then use US Census Bureau datasets to locate potential sites that are proximity to existing locations.  -->


<!-- The mind-warping film opened with a hospital patient Simon Cable (Ryan Phillippe) awakening in a <span class="spoiler"> hospital with little knowledge (amnesia perhaps?) of what had happened, and why he was there, etc. He was told by attending Dr. Jeremy Newman (Stephen Rea) that it was July 29, 2002 (Simon thought it was the year 2000 - he was confused - he heard a doctor say 20:00 hours!) and that he had died for two minutes from cardiac arrest following the near-fatal accident -- but he had been revived ("You're as good as new").</span> Dr. Newman: "Simon, this is the 29th of July. The year is 2002. And your wife, whose name is Anna, is waiting outside."  -->


<!-- ```html
<span class="spoiler">My hidden paragraph here.</span>
``` -->
