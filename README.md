# Module-11v1


##Overview

(As captured from Data Bootcamp Module 11) 

Web scraping automates the tedious tasks of extracting online data for analysis. Instead of a person manually visiting each website, copying the data, and then pasting that data into a file, a web-scraping script automatically performs all those actions and, if necessary, organizes the data for analysis.

The web scraping process consists of opening a browser (like Google Chrome), visiting a webpage, and then interacting with that page. The interactions might include logging in to the site or using a search bar to search for text or an item. One of the key ways to making this process efficient is to automate it. With this automation, we don’t need to manually scan dozens of websites and repeat the interactions on each site.

In this module, as assigned Data Analyst, I will automate a web browser to scrape (Web Scrapping), or extract, data then visualize and analyze the data. 


By the end of this module, as assigned Data Analyst, I will:

    •	Describe basic HyperText Markup Language (HTML) elements.

    •	Explain how websites use HTML to structure a webpage.

    •	Explain how Cascading Style Sheets (CSS) uses the class and id attributes to style HTML elements and identify the components of a webpage for scraping.

    •	Use Beautiful Soup and Splinter to both automate a web browser and scrape data.

    •	Visualize and analyze scraped data by using Python tools.

    •	Describe basic HyperText Markup Language (HTML) elements.

    •	Explain how websites use HTML to structure a webpage.

    •	Explain how Cascading Style Sheets (CSS) uses the class and id attributes to style HTML elements and identify the components of a webpage for scraping.

    •	Use Beautiful Soup and Splinter to both automate a web browser and scrape data.

    •	Visualize and analyze scraped data by using Python tools.



##Purpose
(This module is built around a project that mirrors a real-world scenario that would require data analysis and visualization)

SpaceForward is an ambitious aerospace company that’s doing research about resource extraction from nearby planets. Robin, a data analyst at SpaceForward has been tasked with gathering information about the climate of Mars. In addition, Robin has been asked to collect news items about Mars missions.

As a Data Analyst, I am assisting the Client Robin scrape, organize, analyze, and visualize the data.



##Deliverable 1: Scrape Titles and Preview Text from Mars News (40 points)
Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. 

1.	Use automated browsing to visit the Mars NASA news siteLinks to an external site.. Inspect the page to identify which elements to scrape.

2.	Create a Beautiful Soup object and use it to extract text elements from the website.

![image](https://user-images.githubusercontent.com/117233641/229645035-a5d858c6-0644-41ed-ac40-f1813af3b694.png)
 

3.	Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:

    o	Store each title-and-preview pair in a Python dictionary. And, give each dictionary two keys: title and preview. 

    o	Store all the dictionaries in a Python list.

    o	Print the list in your notebook.

![image](https://user-images.githubusercontent.com/117233641/229645056-899a96e5-d75d-43ff-b468-5988156800cc.png)

![image](https://user-images.githubusercontent.com/117233641/229645086-5770e4e8-70ce-4f9f-91ba-28449d96120a.png)
 

##(Optional) Step 4: Export the Data

Optionally, store the scraped data in a file or database (to ease sharing the data with others). To do so, export the scraped data to either a JSON file or a MongoDB database.

![image](https://user-images.githubusercontent.com/117233641/229645128-e0f72e3d-ebcd-47ce-bb0d-a85b560d3153.png)


##Deliverable 2: Scrape and Analyze Mars Weather Data (60 points)

Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.

1.	Use automated browsing to visit the Mars Temperature Data SiteLinks to an external site.. Inspect the page to identify which elements to scrape. Note that the URL is https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html.

2.	Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.

![image](https://user-images.githubusercontent.com/117233641/229645205-74356b85-188b-4f06-8953-98edc53240a6.png)

 

3.	Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:

    o	id: the identification number of a single transmission from the Curiosity rover

    o	terrestrial_date: the date on Earth

    o	sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars

    o	ls: the solar longitude

    o	month: the Martian month

    o	min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)

    o	pressure: The atmospheric pressure at Curiosity's location

 
![image](https://user-images.githubusercontent.com/117233641/229645270-8a544c29-3959-489d-a830-06df6e206631.png)

![image](https://user-images.githubusercontent.com/117233641/229645289-f87c2949-9049-448f-92b6-e8318cba5d87.png)


4.	Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.

 ![image](https://user-images.githubusercontent.com/117233641/229645308-5ea30565-8bc6-4cfd-a8b4-021907fc03fb.png)



5.	Analyze your dataset by using Pandas functions to answer the following questions:
1.	How many months exist on Mars?

![image](https://user-images.githubusercontent.com/117233641/229645333-a59a2edd-dcd2-4840-8aeb-e4eb04c10918.png)
 

2.	How many Martian (and not Earth) days worth of data exist in the scraped dataset?

![image](https://user-images.githubusercontent.com/117233641/229645345-c669c19d-6b2a-4ad8-85c5-331227ae8205.png)
 

3.	What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:

    	Find the average the minimum daily temperature for all of the months.

![image](https://user-images.githubusercontent.com/117233641/229645372-6edfd9ae-551e-424d-808c-549963e09ff9.png)
 
![image](https://user-images.githubusercontent.com/117233641/229645391-2f3baaad-0ade-4b7a-aeac-3bf46aadd2a0.png)

 
    	Plot the results as a bar chart.

![image](https://user-images.githubusercontent.com/117233641/229645419-f65d6cba-fdb5-454f-ba24-5ee08476ea1b.png)


4.	Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:

    	Find the average the daily atmospheric pressure of all the months.

![image](https://user-images.githubusercontent.com/117233641/229645441-7337aba0-e2d7-4ffd-b7e8-98c202b4c179.png)


    	Plot the results as a bar chart.

 ![image](https://user-images.githubusercontent.com/117233641/229645495-6d6ace24-28bc-4a14-90f0-feca633eddd4.png)


5.	About how many terrestrial (Earth) days exist in a Martian year? To answer this question:

    	Consider how many days elapse on Earth in the time that Mars circles the Sun once.

![image](https://user-images.githubusercontent.com/117233641/229645532-87937e41-47b5-4327-bf74-c2680ea4de65.png)

 

    	Visually estimate the result by plotting the daily minimum temperature.

 ![image](https://user-images.githubusercontent.com/117233641/229645573-37832216-2a0e-45a5-8b3a-846ce5d03bd4.png)


2.	Export the DataFrame to a CSV file.

 ![image](https://user-images.githubusercontent.com/117233641/229645589-54624432-5d31-4b0e-b35d-11776a59e2e2.png)

