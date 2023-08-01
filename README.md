# What makes a good midfielder?

## About
I started this analysis in order to find out which stats are the most important for a midfielder. It turned out to be less straightforward than expected, since I needed to find an objective way to quantify "good" players, and after I did (ratings and market values), I could not get my hands on data for player ratings so I ended up using market values only. I explored the relationship between market value and age, and used that to create a normalised metric, that is market value corrected for age. Using this metric, I then proceeded to find out which stats are the most important for a midfielder.

## Methods
I used polynomial regression to find the relationship between market value and age, and then used these results to create a normalised metric. I then used multiple linear regression to find the relationship between the stats and the metric. I controlled the FDR, and found the most significant stats. However, because of collinearities, I repeated this one last time with only a handful of stats.

## Data
I used market values from [Transfermarkt](https://www.transfermarkt.com/), acquired from [Kaggle](https://www.kaggle.com/datasets/davidcariboo/player-scores) and player stats from [FBref](https://fbref.com), using a [scraper](https://github.com/NikosKont/FBref-Scraper) I made myself.
The data need not be downloaded, as the scraper is included in the notebook and the data are downloaded automatically, if they don't exist.

## Requirements
This notebook was written in Python 3.9.7. The required packages and versions I used are:
```
numpy==1.23.5
pandas==1.5.3
matplotlib==3.7.0
seaborn==0.12.1
kaggle==1.5.13
statsmodels==0.13.5
scikit-learn==1.2.1
```
(also included in requirements.txt)
