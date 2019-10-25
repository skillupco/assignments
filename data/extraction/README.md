# Data extraction assignment

## Summary

Obtain a CSV containing some data extracted from Comundi's training pages: https://www.comundi.fr/

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
- `objectives` Training objectives, full HTML content, if present
- `parsed_duration` Duration of the training
- `parsed_price` Basic price (VAT excluded, discount excluded) of the training, if present

You must store a raw version of above fields (as they appear in page/HTML code). In addition, you should reprocess the following fields:

- `processed_duration` Duration in hours of training, as a number; by convention 1 day = 7 hours
- `processed_price` Price in number format (without currency unit or other text)

## Hints

- You can use the header menu to crawl training categories
- You can use RegEx to process scrapped data formats for duration and price
- Use the CSV in the repository to look into example results (data may be slightly out of date)
- You don't need to execute JavaScript (using Selenium or Chrome Headless) to extract data
- Attempt to keep your code logic and simple, there are no edge cases to solve in this assignment; you may find exception values such as _2 + 2_ or _1 jour + 2 h en classe virtuelle (post formation)_ that you are allowed to discard and ignore

_Do not hesitate to contact us for questions or clarification._
