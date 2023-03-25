# property_valuation

## Summary
Project to build a property valuation tool to accurately predict (listing) prices of London properties. The data has been scraped from the RightMove website (https://www.rightmove.co.uk) from September 2022 onwards. The modelling involves both prediction (supervised ML) and econometrics/causal inference.

## Motivation
As many home-owners will attest, two often debated questions when viewing houses are:
1. whether a property is a good deal or not; and
2. how much of a premium are they paying for extra space, features or a particular location?
This tool hopefully brings objectivity to these questions, which are so often answered by intuitions and gut-feels, by learning and quantifying how various factors influence price. 

## Files & Folders
- **RightMove_Funcs.ipynb:** Contains the functions which scrape RightMove using BeautifulSoup.
- **RightMove_Update_Scrape.ipynb:** Contains the code which calls the scraping functions to perform the scrape, before wrangling/saving the data.
- **Causal inference.ipynb:** Contains the code which builds econometric regressions to quantify the causal relationship of certain features on property values.
- **Predictive models (with floor size).ipynb:** Contains the code which trains and tests multiple ML models to predict property values.
- **data (folder):** Contains all historic datasets from previous scrapes.
- **Old (folder):** Contains all old code files.

## Caveats
Currently the scraper looks at houses between £450k and £800k in certain areas of London (predominantly, North London) - though these parameters can be changed.
Some of the features are London-specific (e.g. centrality - the distance from central London).
