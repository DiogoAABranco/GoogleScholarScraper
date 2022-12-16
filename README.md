# GoogleScholarScraper - A simple WebScraper for Google Scholar.

### This code allows the extraction of Titles and Sources/Date from multiple GS pages.
- This code does not use [Selenium](https://selenium-python.readthedocs.io/) (no need to install drivers) nor [SerpAPI](https://serpapi.com/).
- **Disclosure:** I didn’t put much time into this, more than likely, room for improvement exists.
- Tested using Ubuntu 20.04

## USAGE:

- Change variable **total_of_pages_to_search** to the number of pages you want to scrap

1. Do a manual search at google scholar for example "Brain Computer Interface"
2. The first page will return a link like this https://scholar.google.com/scholar?hl=en&as_sdt=8%2C5&q=Brain+Computer+Interface&btnG=
3. Now press on page 2 and a different link will appear https://scholar.google.com/scholar?start=10&q=Brain+Computer+Interface&hl=en&as_sdt=8,5
4. On this link, replace the 10 with {nrpages} f"https://scholar.google.com/scholar?start={nrpages}&q=Brain+Computer+Interface&hl=en&as_sdt=8,5"
5. Insert the new link the into the variable **URL**.
6. Run!

- The saved csv will be located in a folder with the format _Scrap{Date}. 


## WARNING:

- Multiple requests might lead to temporary ip blockage as google does not like bot like behaviour.

## Requirements
pip:
- beautifulsoup4 
- requests 
- tqdm 
- pandas
 
