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



## Steps:

1. Download the repo.

2. Set up the environment with requirements.txt 
```
>> pip install -r requirements.txt 
```

3. Go in the folder  
```
>> cd medium_scrapping
```
and Run the body scraper script with
```
>> python article_text_scraping.py
```

4. To scrap for other tags, please download the URL files from the drive.

5. Place it next to the python file.

6. In the python file, please change the variable ```url_file_name``` to new urls file and run.  

7. You would notice one CSV and one json file written in same folder with the contents.




*Tip*: If you want a trial, you can set 'N' to 5 or 10 to try scrapping for 5-10 articles. By default it will scrap all the urls.
