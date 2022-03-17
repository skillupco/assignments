# Data extraction assignment

## Summary

Obtain a CSV containing some training data extracted from a French training organization: https://www.gereso.com/

In this repository, we provide a CSV file containing an example of the expected output (which may not be up to date). This CSV is using coma as a delimiter and is encoded in UTF-8. If you open this file using Excel you may have to use data import. Your CSV is not expected to 100% match the provided file (data evolves on a regular basis).

**Expected output from this assignment: scraper code and the CSV file.**

## Requirements

- Language: Python 3
- Library: you are free to use any data extraction & processing library

Internally, we use [Scrapy](https://scrapy.org/).

## Expected columns

- `url` Training page URL
- `name` Training title
- `sku` Unique reference of the training
- `program` Training program, full HTML content, if present
- `parsed_duration` Duration of the training
- `parsed_price` Basic price (VAT excluded, discount excluded) of the training, if present

You must store a raw version of above fields (as they appear in page/HTML code). In addition, you should reprocess the following fields:

- `processed_duration` Duration in hours of training, as a number; by convention 1 day = 7 hours
- `processed_price` Price in number format (without currency unit or other text)

## Hints

- You can use the category list from home page to crawl training categories and find links to training pages, for example: https://www.gereso.com/formations/pratiques-rh/formation-l-essentiel-de-la-gestion-administrative-des-rh
- You can use RegEx to process scrapped data formats for duration and price
- Use the CSV in the repository to look into example results (data may be slightly out of date)
- You don't need to execute JavaScript (using Selenium or Chrome Headless) to extract data
- Attempt to keep your code logic and simple, there are no edge cases to solve in this assignment; you may find multiple price values, just take the first one into account

_Do not hesitate to contact us for questions or clarification._
