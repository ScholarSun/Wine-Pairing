# Wine-Pairing
## Table of Contents
1. [Introduction](#introduction)
2. [Phase 1: Scraping and Parsing](#paragraph1)
3. [Phase 2: Modeling and Predictions](#paragraph2)
4. [Phase 3: Web Application](#p3)

## Introduction <a name="introduction"></a>
Can a machine learn to pair food and wine?
The main idea: we scrape a bunch of recipes with well known wine pairings and see if a machine can detect a patterns or form abstractions between the two. I expect to see group key ingredients that go well with wines together or perhaps certain wines and cooking methods pair well together. 

## Phase 1: Scraping and Parsing <a name="paragraph1"></a>
This mainly concerns the recipescraping folder.
We first scraped the website allrecipe.com with a list of about 420 full recipies with 17 different types of wine pairings using beautifulsoup. I parsed all the information accordingly and broke down the recipe into a JSON as follows:

The base framework scrape was done by @kbrohkahn on github. I adjusted it to my specific requirements. Natural language toolkit library was used to parse each recipe step into sentences. Hardcoded arrays were used to label the ingredients. I traversed the website through beautifulsoup to get the corresponding wine pairings. 

I then manually cleaned up the data to check for mis-labelling and unlabbeled items. I parse this into a csv and then a load it to a pandas dataframe. 

## Phase 2: Modeling and Predictions <a name="paragraph2"></a>


## Phase 3: Web Application <a name="p3"></a>



