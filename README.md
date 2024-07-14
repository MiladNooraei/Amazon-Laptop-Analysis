#  Amazon Laptop Analysis

## Description
The project involves scraping laptop data from [Amazon](https://www.amazon.com/), cleaning and preprocessing the data, and then using it to train predictive models. The goal is to accurately predict the price of a laptop based on its features using linear regression and random forest algorithms.

## Project Phases

### Phase 1: Data Scraping
In this phase, I used Selenium to automate the collection of laptop links from Amazon. Specifically, I targeted the "Top Rated" page and the "Under $500" page, resulting in a total of 10,446 laptop links. Next, I utilized BeautifulSoup to scrape detailed features for each laptop.

During the scraping process, I encountered numerous instances of response code 500 errors. To handle this, I implemented a retry mechanism where the code attempts to scrape the page up to 3 times with a 1-second wait between attempts. If the error persisted, the code skipped the URL and moved on to the next one. Ultimately, this approach allowed me to successfully scrape data for 3,988 laptops. The data was then saved into a file named `laptops_dataset.csv`.

### Phase 2: Regression Analysis
The second phase involved cleaning and preprocessing the scraped data. I selected relevant features and removed rows with NaN values or corrupted data entries. This cleaning process reduced the dataset to 1,589 valid entries.

With the cleaned dataset, I proceeded to train two predictive models: a Random Forest model and a Linear Regression model. These models were trained to predict laptop prices based on the features scraped from Amazon.

## Conclusion
This project demonstrates the entire process of web scraping, data cleaning, and predictive modeling. The models trained in this project can be used to estimate laptop prices based on various features, providing valuable insights for potential buyers and sellers.
