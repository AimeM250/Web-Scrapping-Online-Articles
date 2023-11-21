# Simple Web Scraping Project 

This repository contains scripts for scrapping data from the web. The extracted data is stored in a JSON format and can be further processed for analysis or fed in any Large Language Model.

## Prerequisites

Before running the scripts, ensure that you have the following dependencies installed:

- Python 3
- `requests` library
- `beautifulsoup4` library
- `pandas` library
- `nltk` library
- `wordnet` corpus (from `nltk`)
- `omw-1.4` corpus (from `nltk`)

You can install the required libraries by running the following command: pip install -r Requirements.txt

## Files

- `myspider.py`: Uses Scrapy framework to scrape the GoV.UK articles and extract the title, content, and URL of each article.
- `web_scrapper.py`: Uses BeautifulSoup and requests to scrape the GoV.UK articles, extract the text and date, and update the JSON data.
- `preprocess.py`: Preprocesses the data stored in `articles.json` for further analysis.
- `URLs.json`: Contains the URLs of the articles to be scraped.
- `articles.json`: Contains the scraped article data including the title, content, and date.


## BeautifulSoup Script: `web_scrapper.py`

The `web_scrapper.py` script uses BeautifulSoup and requests libraries to scrape articles listed in the `URLs.json` file. It extracts the text and date from each article and updates the JSON data in the `articles.json` file.

To run the script, execute the following command: python web_scrapper.py URLs.json


## Preprocessing Script: `preprocess.py`

The `preprocess.py` script preprocesses the scraped JSON data stored in the `articles.json` file. It performs various text processing steps, such as converting to lowercase, removing punctuation, numbers, and stopwords, lemmatizing, stemming, and removing specific words. It also filters the data based on the date and converts the date column to year-month periods.

To run the script, execute the following command: python preprocess.py articles.json

