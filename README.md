# redfin_scraper
Scrapes listing data and photos from Redfin

### Overview
- Uses Selenium WebDriver and a [proxy](https://github.com/christophergdavis/free-us-proxy) to bypass bot detection
- Loops through the proxy list to find a good one
- Once `<200>` is received, proceeds to load the given listing url
- Uses BeautifulSoup to parse summary data (bed/bath count, etc.), key details (lot size, year built), amenities, and recent price history
- Returns to Selenium to loop through photos because only the lead image shows src in the html
- Joins data into single dictionary
