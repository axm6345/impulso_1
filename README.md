# Medium_Scraper

## Data dictionary (output columns):

1. UUID : Universally unique identifier created for each article URL	
2. url : Article URL	
3. topic : Main topic or key word e.g. Data science / Artificial intelligence / ..	
4. title : Title of the article	
5. subtitle	: If available, subtitle for further emphasis on the article's theme
6. tags	: associated tags which are covered in the article
7. author	: list of writers
8. h1_headers : List of first level headings	
9. h2_headers	: List of second level headings
10. paragraphs : List of paragraphs (each paragraph is a separate entity of 2-5 sentences generally)	
11. blockquotes	: Quotes used by the writers
12. bold_text	: List of important sentances 
13. italic_text : List of codes or special terms as highlighted by writers
14. figures : List of image URLs



## Steps


### 1. Collect URLS from medium
- Folder : Medium_URL_Scraper
- Script to run: scrape_master.py
- Settings in script: You can change the tag and timeline.

### 2. Remove redundent URLs and further cleaning: 
Same URL could be found multiple times, under multiple different tags. 
There are two sub folders for 2009-16 and 2016-20.
- Folder : Medium_scrape_URL_cleaning_EDA
- Scripts to run: Go in the corresponding folder and you will see a jupyter notebook (e.g. data_cleaning_2016-2020.ipynb)
- Raw data : in folder scraped_tags
- Final output: Single CSV for that time period (e.g. Medium_scrape_urls_multi-tag _clean_2016-2020.csv)

### 3. Scrap body and image URLS 
- Folder : Medium_scrape_text_and_image
- Script to run : article_text_img_scraping.py
- Input data: Please place cleaned csv- as generated on 2nd step. (e.g. Medium_scrape_urls_multi-tag _clean_2016-2020.csv)
- Output data: contents_op_*.csv

*Note*: As per request 5 sample articles are scrapped. Please refer - contents_op_Medium_scrape_urls_multi-tag _clean_2016-2020.csv


*P.S.*
*
-requirements.txt is available for the environment setup. Please ensure  correct version of chrome driver in respective folders.


-You can also refer instance setup file - example in Medium_scrape_text_and_image folder.
