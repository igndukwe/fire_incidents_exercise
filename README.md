# README: Web Scraping and Data Analysis with Scrapy

This guide walks you through setting up a virtual environment, creating a Scrapy project, running the web crawler to collect fire incident reports, and analyzing the data. Follow the steps below to get started.

## Configurations and Installations

### 1. Create a Virtual Environment
Create a virtual environment to manage your project's dependencies.
```
python -m venv venv```

### 2. Activate the Virtual Environment
Activate the virtual environment to use the installed packages.

- On Windows:
```
.\venv\Scripts\activate```

- On Unix or MacOS:
```
source venv/bin/activate```

### 3. Upgrade pip to the latest version.
```python -m pip install --upgrade pip```

### 4. Install Required Libraries
Install the necessary libraries specified in the requirements.txt file.

```
pip install -r requirements.txt```




## Creating a Scrapy Project
Scrapy helps you create a structured web scraping project.

5. Start Scrapy Project
Start a new Scrapy project with the name fire_incidents.
```scrapy startproject fire_incidents```
If you encounter PowerShell permission issues on Windows, use:
```.\venv\Scripts\python.exe -m scrapy startproject fire_incidents```



## Creating the Crawler Class
The crawler retrieves information from the website using XPath expressions.

### 6. Create a Spider
Create a spider to crawl the web page.

```cd fire_incidents
scrapy genspider incident_reports fireandemergency.nz/incidents-and-news/incident-reports```


- Check the robots.txt of the website to ensure you are allowed to crawl it:

https://fireandemergency.nz/robots.txt



## Running the Crawler
The spider class will crawl the web, extract fire incident report data, and save it to a CSV file.

### 7. Crawl the Webpage
Run the spider to extract data and save it into a CSV file in the data folder.

```cd path/to/your/root/directory
python Main_1_ScrapyRunner.py```


## Performing the Analysis
Combine and analyze the collected data to answer specific questions.

8. Perform the Analysis
This script combines all CSV files starting with day_of_week_incident_reports into a DataFrame and performs the analysis to answer the following questions:

- How many incidents has the Stratford Brigade responded to in the last 7 days?
- How many medical incidents have been reported in the Central Region in the last 7 days?
- Where were the medical incidents reported in the last 7 days?
Run the analysis script:

```python Main_2_AnalyzeData.py```


## Conclusion
By following the steps outlined in this README, you will be able to set up your environment, create and run a Scrapy project, and analyze fire incident report data effectively. This guide ensures that new users can easily make use of the provided Scrapy code.






