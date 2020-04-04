---
layout: post
published: true
title: Expedia Wants You!
date: '2019-10-25'
image: /img/expedia-hotel-data/expedia-logo.jpg
bigimg: /img/expedia-hotel-data/expedia-banner.jpg
tags:
  - data science
  - data analysis
  - Lambda School
---
The data we are taking a look at is an excerpt of data from Expedia’s hotel line of business. It contains logs of customer hotel searches, sampled from 2015, either for a hotel only or in a package with air tickets or car rental, but always involving a hotel (and only recording the hotel interactions). These interactions are clicks on hotels in the search, and actual bookings.

The scale of the data is massive, with over 10 million rows! Unfortunately, when using a Google Colab environment, it simply runs out of RAM from this massive amount of data when performing KMeans clustering with one-hot encoded variables and hand-generated features to predict the hotel clusters, and so the data had to be down-sampled to record the logs of 100,000 unique users (almost 1,500,000 rows of data).

Our goal is to explore the journey of a traveler through the Web site and uncover any of the secrets that lie in the data — from patterns in seasonality and day of the week, to finding signals from customers who might prefer a vacation rental property rather than a hotel, and everything in between.

## Exploring the Data

Our foray into the data begins with the engineered feature for **user continent**. From the graph, we can see that North American users offer a staggering 88% of the traffic to Expedia for hotels, and the other bars in the graph are tiny in comparison. If we analyze just the other 5 continents (sorry, Antarctica), then we see that Europe is the next most popular origin for Expedia users. Surprisingly, Oceania has the least number of searches, so maybe their market is taken up by other companies in the hotel realm of business.

<p align="middle">
  <img src="/img/expedia-hotel-data/eda/eda1.png" width="50%" />
  <img src="/img/expedia-hotel-data/eda/eda2.png" width="50%" /> 
</p>

