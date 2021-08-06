# Pyhton Web-Scraping from a Dynamic Website

In this notebook, we will learn how to scrape some data from a dynamic website. In dynamic web pages, the Content of pages is different for different visitors. It takes more time to load than the static web page. Dynamic web pages are used where the information is changed frequently, for example, stock prices, weather information, etc

We use requests to load page into our python script. Now, if the page we are trying to load is dynamic in nature and we request this page by requests library, it would send the JS code to be executed locally. Requests package does not execute this JS code and just gives it as the page source. For that we use selenium package.

references: https://www.geeksforgeeks.org/difference-between-static-and-dynamic-web-pages/ https://www.geeksforgeeks.org/scrape-content-from-dynamic-websites/

**Required Libraries:**

requests - this module allows user to send HTTP requests using Python and to get the response text.

Selenium: Selenium (open-source) is a web testing library. It is used to automate browser activities.

bs4 - Beautiful Soup is a Python package for parsing HTML and XML documents. It creates parse trees that is helpful to extract the data easily.

pandas - to store the data in a structured format

Selenium webdriver - need to download selenium webdriver. The webdriver will run in real time and interact with the webpage to get the data.

**URL That We want to scrape**

In this Jupyter Notebook, we will scrape some laptop details from flipkart website 'https://www.flipkart.com/'. The data includes Product Name, Specs_summary, Price, rating.

This is only for educational purpose.

Reference : https://realpython.com/beautiful-soup-web-scraper-python/

**Steps:**

1)  Launch Selenium webdriver

2)  Go the the flipkart website. Let it load. 

3) Once loaded, Enter "Laptop" in the search box. (navigate to searchbox using inspect element). Then press enter.

4) Let the search result load completely.

5) Once loaded, using requests, get html data. 

6) using BeautifulSoup parse the required info like product name, rating, price, specification etc.

7) Go to next page. (By clicking on next button using webdriver)

8) Repeat steps 5, 6 & 7 until required number of products reached.

