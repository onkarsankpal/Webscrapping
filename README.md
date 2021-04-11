# Webscrapping
Beautiful Soup is a library that makes it easy to scrape information from web pages. It sits atop an HTML or XML parser, providing Pythonic idioms for iterating, searching, and modifying the parse tree.
Beautiful Soup is a Python library designed for quick turnaround projects like screen-scraping. 

## Following features make it powerful:

* Beautiful Soup provides a few simple methods and Pythonic idioms for navigating, searching, and modifying a parse tree: a toolkit for dissecting a document and extracting what you need. It doesn't take much code to write an application
* Beautiful Soup automatically converts incoming documents to Unicode and outgoing documents to UTF-8. You don't have to think about encodings, unless the document doesn't specify an encoding and Beautiful Soup can't detect one. Then you just have to specify the original encoding.
* Beautiful Soup sits on top of popular Python parsers like lxml and html5lib, allowing you to try out different parsing strategies or trade speed for flexibility.

## Steps involved in web scraping:
* Send an HTTP request to the URL of the webpage you want to access. The server responds to the request by returning the HTML content of the webpage. For this task, we will use a third-party HTTP library for python-requests.
* Once we have accessed the HTML content, we are left with the task of parsing the data. Since most of the HTML data is nested, we cannot extract data simply through string processing. One needs a parser which can create a nested/tree structure of the HTML data. There are many HTML parser libraries available but the most advanced one is html5lib.
* Now, all we need to do is navigating and searching the parse tree that we created, i.e. tree traversal. For this task, we will be using another third-party python library, Beautiful Soup. It is a Python library for pulling data out of HTML and XML files.

we need 2 packages:
* requests — for downloading the HTML code from a given URL
* beautiful soup — for extracting data from that HTML string

# Installing the libraries
### python -m pip install requests beautifulsoup4

# Using requests & beautiful soup to extract data
From the requests package we will use the get() function to download a web page from a given URL:
### requests.get(url, params=None, **kwargs)

Where the parameters are:
* url — url of the desired web page
* params — a optional dictionary, list of tuples or bytes to send in the query string
* **kwargs — optional arguments that request takes

## Potential Challenges of Web Scraping
* One of the challenges you would come across while scraping information from websites is the various structures of websites. Meaning, the templates of websites will differ and will be unique; hence, generalizing across websites could be a challenge.
* Another challenge could be longevity. Since the web developers keep updating their websites, you cannot certainly rely on one scraper for too long. Even though the modifications might be minor, but they still might create a hindrance for you while fetching the data.

Hence, to address the above challenges, there could be various possible solutions. One would be to follow continuous integration & development (CI/CD) and constant maintenance as the website modifications would be dynamic.
