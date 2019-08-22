# Analyzing-data-from-online-book-store-using-Python

### Data Source: http://books.toscrape.com/

### Introduction: 
Books to scrape is a fictional book store's website which has books of 50 different genres types. It is a demo website created for web scraping purposes. The website hosts nearly 1000 books which has random prices (in £) and ratings assigned. Additionally each book has information such as book stock availability, book description, genre type etc..,

### Web Scraping:
Information or data in a website can be collected either by human beings or by automated code. However manually getting all data from a website can be very tedious and time consuming. So we can automate the process by a code which can get all information from the website. This process of extracting information from a website is called web scraping. Depending on the structure of the website that contains the necessary data, code can be developed accordingly to access the data from those structural elements. 
**Drawback:** Major drawback of webscraping is that if the structure of the webpage is altered anytime then the code has to be modified accordingly.

More information: https://en.wikipedia.org/wiki/Web_scraping

### Project description:
Books to scrape website has its information structured in the form of [html](https://www.w3schools.com/html/). In this project I have tried to explore and use a new Python library called [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/). I have scraped important information such as stock availability, ratings, price, description and titles of all books listed in the website. Using the scraped information I am trying to answer the below mentioned research questions by creating visualizations.

#### Research Questions:
1. What are the top 10 genre types ordered by number of unique book titles available for an user to buy when user specifies the budget and also the ratings while purchasing? ***Note:*** Exclude genre types 'Default' and 'Add a comment' that makes no sense in this case 

2. For a given user rating, what is the most common word in book title that influences people to read and give good ratings? 

### Limitations: 
Since most of the data collected from this website is descriptive, only qualitative analysis can be done

### Project Code structure
- Part 1 - Scraping data from website of scope
- Part 2 - Data Analysis: Making vizualizations to answer research questions 

### Part 1: 
- Consists of 3 stand alone functions collect_headerinfo(), get_eachbooklinks(Totalpages,perpagecount), get_eachbookinfo(bookurllist)
- All 3 functions are integrated into 1 main function main_scraping_allbooksinfo() which when run will scrape all data from website and return a dataframe with required information from website of scope

### Part 2:
- Consists of 2 stand alone functions budget_based_books(Books_infotable), rating_based_books(Books_infotable)
- These 2 functions are used together to create 1 main function main_visualization_bookcount(allbooks_dataframe) used for answering research question 1
- Rating function is used along with new library wordcloud to form another main function main_booktitle_wordchoice(allbooks_dataframe)  which can answer research question 2



### Execution Instructions: 
Run all functions in the notebook. However call only main functions such as 
#### main_scraping_allbooksinfo()       
***Important Note:*** Save results of the above function to a variable while calling & pass that variable as an input to below 2 functions
#### main_visualization_bookcount(allbooks_dataframe)
#### main_booktitle_wordchoice(allbooks_dataframe) 

**Warning** Dont try to test by calling other stand alone functions particularly in scraping part as you will spend minutes on stand alone functions which are already included in the main function.

