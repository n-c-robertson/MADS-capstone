#  Predicting Sale Price of a Listing

_Authors: Nathan Robertson, Mijee Kim, Josh Iwanicki_

## Introduction

_This repository represents the capstone project for the authors in the Masters of Applied Data Science (MADS) program at the University of Michigan in the 2024 Fall semester. This is a home price prediction project leveraging machine learning, generative AI, and computer vision._

Pricing a home is difficult. While home marketplaces like Zillow provide estimates of a home’s value, it doesn’t educate buyers and sellers on the factors that influence home price. We hypothesize that enriching listing data with points of interest (POI) data and image data will significantly increase price prediction accuracy. In this report, we outline the existing literature, present the methodology behind our approach, and deliver an evaluation of our results. 

[The full report can be found here](https://docs.google.com/document/d/1bIc3J4sXRWWcBvTOaUCBsZWUrenWeIn1PhI0KEX_0r4/edit)

## Getting Started

Clone the repo.

```
git clone https://github.com/n-c-robertson/MADS-capstone.git
```

Get all of the dependencies needed.

```
pip install -r requirements.txt
```

To run all of the code in this project, you will need API keys to a few different resources.

| API | Documentation to set up API key | Where is it used? |
| ------------- | ------------- | ------------- |
| Microsoft Azure Vision | [Link (Requires Credit Card)](https://learn.microsoft.com/en-us/answers/questions/126140/service-url-and-api-key-of-computer-vision) | `4_Generating Image Training Data.ipynb` |
| OpenAI | [Link (Requires Credit Card)](https://platform.openai.com/docs/quickstart) | `3_Filtering Junk Listings.ipynb`, `4_Generating Image Training Data.ipynb`|
| FBI Crime Data | [Link (Free)](https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi) | `6_POI_+_Additional Datasets.ipynb` | 

## Accessing the Data

The data used for this project can be found in the team's Dropbox [Link](https://www.dropbox.com/home/Nathan%20Robertson/MADS-Fall-2024-Zillow-Predictive-Pricing). If you need access, please request access from natorobertson@gmail.com.

Download all of the data in Dropbox, and put it in the same directory as the notebook you are trying to run. Assuming you have the necessary API keys (documented above), you should be able to run the notebook.

## Where did this data come from?

| **Name**          | **Description**                                                                 | **Source**                     | **License**            |
|------------------|-----------------------------------------------------------------------------------|-------------------------------|------------------------|
| **Crime Data**   | County-level summary statistics on crime.                                      | [Crime Data API, hosted by Justice.gov]([link](https://www.justice.gov/developer)) | Open License / Public Domain |
| **National Risk Index** | County-level data about the natural disaster risks of that area.           | [Fema.gov](https://hazards.fema.gov/nri/data-resources#csvDownload)                | Open License / Public Domain |
| **Population Data** | 2022 county-level population estimates.                                        | [Census.gov](https://www.census.gov/data/tables/time-series/demo/popest/2020s-counties-total.html)             | Open License / Public Domain |
| **US Coast Line** | SHP file to determine whether or not a listing was close to the coast.        | [Data.gov](https://catalog.data.gov/dataset/tiger-line-shapefile-2019-nation-u-s-coastline-national-shapefile)              | Open License / Public Domain |
| **Museum Locations** | Locations of museums, with additional data on each museum’s annual revenue.  | [Institute of Museum and Library Services](https://www.imls.gov/research-evaluation/data-collection/museum-data-files) | Open License / Public Domain |
| **US Mountain Ranges** | SHP file to determine whether or not a listing is in a mountain range.       | [ArcGIS Hub](https://hub.arcgis.com/datasets/fc949de03499477592fc412bb957720e/explore?location=37.431234%2C-82.777653%2C5.15)            | No license provided     |
| **National Parks** | Locations of US parks by latitude / longitude.                               | [Latlong.net](https://www.latlong.net/category/national-parks-236-42.html)           | No license provided     |
| **Post Offices** | Locations of US Post Offices.                                                | [Github](https://github.com/cblevins/us-post-offices/blob/main/us-post-offices.csv)               | MIT License             |
| **Hiking Trails** | Locations of Alltrails trails, including some metadata about each trail.       | [Github](https://github.com/j-ane/trail-data/blob/master/State%20Trail%20Data/.DS_Store)               | No license provided     |
| **Prisons**      | Locations of prisons.                                                          | [Github](https://github.com/joshbegley/data/blob/master/us-prisons.csv)               | No license provided     |
| **Power Plants** | Locations of power plants, with additional metadata on power type and output. | [Github](https://github.com/wri/global-power-plant-database/blob/master/output_database/global_power_plant_database.csv)               | MIT License             |
| **Starbucks**    | Explored, but abandoned due to data gaps.                                      | [Github](https://gist.github.com/dankohn/09e5446feb4a8faea24f)             | Wasn’t used.           |
| **Comps**        | Data on the price of comparable homes (comps) nearby the listing.              | [Bankrate](https://www.bankrate.com/real-estate/how-to-find-real-estate-comps/)             | Not Applicable         |
| **City Tiers**   | Ranally City Rating system for determining the size of the city.               | [Wikipedia](https://en.wikipedia.org/wiki/Ranally_city_rating_system)             | Not Applicable         |
| **Zillow.com**   | Web scraped dataset of 200,000 listings.                                       | [Zillow.com](https://www.zillow.com/)            | I made sure my web scraper respected the robot.txt file for Zillow.com and kept traffic to a human level (it slowly scraped data for 6 weeks). |

