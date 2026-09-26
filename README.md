Books Capstone Project

This was my capstone project - I wanted to practice the full data process, 
from collecting data myself to presenting it in a dashboard.

I scraped 1,000 books off books.toscrape.com using Python (title, price, 
rating, stock status), then cleaned it up - fixed the price formatting, 
converted word ratings ("Three", "Four") into numbers, and removed 
duplicates.

After that I explored the data with some basic charts (price distribution, 
rating distribution, price vs rating), and tried building a Decision Tree 
model to predict if a book would be highly rated based on price. It only 
got 58.5% accuracy, which showed price alone isn't a strong enough signal - 
makes sense, since rating probably depends more on the actual book itself.

I also built a two-page Power BI dashboard - one page with overall KPIs, 
and a second page to filter and look at individual books.

**Tools:** Python (pandas, matplotlib, seaborn, scikit-learn), 
BeautifulSoup, Power BI

**Files:**
- `01_Web_Scraping_Books.ipynb` - scraping script
- `02_Cleaning_EDA_ML.ipynb` - cleaning, EDA, and ML model
- `Books_Raw_Data.csv` / `Books_Cleaned_Data.csv` - the data
- `Books_Capstone_Report.pdf` - full write-up with charts and dashboard screenshots
