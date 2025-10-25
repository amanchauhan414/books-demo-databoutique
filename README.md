# Data Mapping Documentation for Books Demo Dataset

## 1. Dataset Description

- **Dataset Type:** Book information
- **Source Website:** [http://books.toscrape.com/](http://books.toscrape.com/)
- **Purpose:** Demo dataset to show field mapping and structure for databoutique.

## 2. Fields Mapping

| Field Name   | Playwright Selector / Source Example                                  | Description / Notes                   |
| ------------ | --------------------------------------------------------------------- | ------------------------------------- |
| Book Title   | `book.query_selector("h3 a").get_attribute("title")`                  | Name of the book                      |
| Price        | `book.query_selector(".price_color").text_content()`                  | Price in GBP                          |
| Availability | `book.query_selector(".instock.availability").text_content().strip()` | Stock status: In stock / Out of stock |

## 3. Example Rows (CSV)

| Book Title                            | Price  | Availability |
| ------------------------------------- | ------ | ------------ |
| A Light in the Attic                  | £51.77 | In stock     |
| Tipping the Velvet                    | £53.74 | In stock     |
| Soumission                            | £50.10 | In stock     |
| Sharp Objects                         | £47.82 | In stock     |
| Sapiens: A Brief History of Humankind | £54.23 | In stock     |

## 4. Notes

- Only scraping first 5 books for demo purposes.
- Data cleaned to remove extra spaces in availability field.
- Playwright selectors correspond to HTML elements on the website.
- Demonstrates how every field in the CSV maps to the source data.
