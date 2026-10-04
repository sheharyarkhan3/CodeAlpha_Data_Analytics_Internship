# Task 1: Web Scraping

**CodeAlpha Data Analytics Internship**

## Objective
Collect a custom dataset from a public website using Python, by handling the
site's HTML structure and page navigation.

## Website
[books.toscrape.com](https://books.toscrape.com), a public practice website
made for learning web scraping.

## Tools Used
- Python 3
- requests (to download web pages)
- BeautifulSoup (to parse HTML and extract data)
- pandas (to organize the data and save it as CSV)
- Jupyter Notebook (Anaconda Navigator)
- Chrome DevTools (to inspect the HTML structure)

## What I Did
1. Inspected the HTML of the website to find the tags and classes that hold the data.
2. Wrote a scraper that loops through all 50 pages of the catalogue.
3. Extracted four fields for every book: title, price, star rating, and availability.
4. Converted the star rating from words ("Three") to numbers (3).
5. Stored the results in a pandas DataFrame and saved them as a CSV file.

## Dataset
| Column | Description |
|--------|-------------|
| Title | Name of the book |
| Price | Price in pounds (£), stored as text |
| Rating | Star rating from 1 to 5 |
| Availability | Stock status of the book |

**Size:** 1000 rows and 4 columns

## Files in This Folder
- `Task1_Web_Scraping.ipynb`: the notebook with code and explanations
- `books.csv`: the scraped dataset

## How to Run
1. Install the libraries: `pip install requests beautifulsoup4 pandas`
2. Open the notebook in Jupyter Notebook.
3. Choose **Kernel > Restart & Run All**.
4. The file `books.csv` will be created in the same folder.

## Key Learnings
- How to read the HTML structure of a web page
- How to select data using BeautifulSoup
- How to loop through multiple pages to collect data
- How to turn scraped data into a clean dataset for analysis

## Notes
- This website is built for practice, so scraping it is allowed.
- The Price column still contains the £ symbol. It is cleaned in Task 2.