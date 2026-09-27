# Books Capstone Project

This was my capstone project, where I wanted to go through the entire data process end to end — collecting the data myself, cleaning it, digging into it, trying to build a model, and finally putting it into something visual that a non-technical person could actually use.

## The data

I scraped 1,000 books from books.toscrape.com using Python, pulling the title, price, star rating, and stock status for each one. The site is meant for scraping practice, so it was a good way to work on this without worrying about breaking any rules.

Once I had the raw data, it needed a fair amount of cleaning before it was usable:
- Prices were stored as text with currency symbols, so I had to convert them into actual numbers
- Ratings were written out as words ("One", "Two", "Three", "Four", "Five") instead of numbers, so I mapped those to a 1–5 scale
- There were a handful of duplicate entries I removed

## Exploring the data

With clean data, I looked at a few basic questions using charts: how prices were distributed, how ratings were distributed, and whether there was any relationship between price and rating.

I also tried training a Decision Tree model to see if I could predict whether a book would be highly rated just based on its price. It came out to about 58.5% accuracy, which isn't great, but that itself was an interesting result — it suggests price on its own doesn't tell you much about how good a book is rated. Makes sense, since rating probably has more to do with the book's actual content, genre, or author than its price tag.

## The dashboard

Since the point of the project was to practice presenting data too, not just analyzing it, I built a two-page Power BI dashboard. The first page shows overall KPIs (average price, average rating, number of books, etc.), and the second page lets you filter and drill down into individual books.

## Tools I used

Python (pandas, matplotlib, seaborn, scikit-learn), BeautifulSoup for scraping, and Power BI for the dashboard.

## Files in this repo

- [`01_Web_Scraping_Books.ipynb`](Books_Capstone_Project/01_Web_Scraping_Books.ipynb) – the scraping script
- [`02_Cleaning_EDA_ML.ipynb`](Books_Capstone_Project/02_Cleaning_EDA_ML.ipynb) – cleaning, EDA, and the ML model
- [`Books_Raw_Data.csv`](Books_Capstone_Project/Books_Raw_Data.csv) / [`Books_Cleaned_Data.csv`](Books_Capstone_Project/Books_Cleaned_Data.csv) – the raw and cleaned datasets
- [`Books_Capstone_Report.pdf`](Books_Capstone_Project/Books_Capstone_Report.pdf) – a full write-up of the project with charts and dashboard screenshots

If you want to see the results without running any code, the PDF report is the easiest place to start — it walks through the charts and has screenshots of the dashboard itself.
