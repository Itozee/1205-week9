# Exploring Population Dynamics: A Python-based Analysis of Fertility and Life Expectancy Trends (1960-2013)

This project is designed to conduct a comprehensive analysis of fertility and life expectancy trends spanning the years 1960 to 2013. The primary goal is to leverage Python for advanced data manipulation, aiming to uncover valuable insights into population dynamics. The analysis will delve into potential economic and health impacts, investigate factors contributing to the aging population, and assess immigration needs.

Taking a more focused approach, the investigation will be specifically tailored to the country associated with my student ID (100871852) as indicated in the metadata. This targeted analysis will offer a nuanced understanding of the region's fertility and life expectancy trends, providing valuable insights into the demographic landscape of the chosen country over the decades.

# Data

The data is stored within a directory, encompassing three Excel sheets: Country_Metadata, Fertility_Rate, and Life Expectancy_At_Birth.

Country_Metadata: This workbook consist of the countries being used for analysis, the country code, student_id (the use will be discussed upon in later stages of this project), the region in which these countries are located, the income group of the countries and special notes regarding the countries. Metadata refers to data that provides information about other data. In other words, it is data about the information provided in the fertility and life expectancy worksheets. 

Fertility_Rate: This workbook incorporates shared variables from country metadata and data spanning from 1960 to 2013, specifically focusing on fertility rates across the various countries.

LifeExpectancy_At_Birth: This workbook integrates shared variables from country metadata alongside life expectancy data for various countries, spanning the years 1960 to 2013.

# Questions the data will answer

I will build appropriate visuals for the problem set which specifically aims to address the following question.

-- How does the country associated with my student ID (100871852) compare to the region it is apart of in terms of average fertility

-- How does Life expectancy in the country associated with my student ID (100871852) change, decade to decade ?

-- Any relationship between Life Expectancy and Fertility in the country associated with my student ID (100871852)?

# Tools

The project utilized Python in Visual Studio Code and Microsoft Excel.

The libraries that will be loaded into python for this analysis are;

-- Pandas: The pandas library in Python is a powerful and widely used open-source data manipulation and analysis library. It provides data structures for efficiently storing and manipulating large datasets, along with tools for cleaning, aggregating, and analyzing data.

-- Openpyxl (Microsoft Excel): This library is used for working with Excel files in Python.

 We also used some modules imported from the openpyxl library, the modules used are;

-- from openpyxl import Workbook

-- from openpyxl.utils.dataframe import dataframe_to_rows

-- from openpyxl.chart import BarChart, Series, Reference

I plan to elaborate on the utilization of these modules when I begin implementing them during the course of the project.


# Steps Followed

# Data Extraction and Transformation (Codes available in the Python code folder)

- Uploaded the raw data(Metadata, Fertility and Life expectancy files) to GitHub.
  
- Linked the datasets to Visual Studio Code and imported data using pandas and openpyxl.
  
- I Set the maximum number of columns to 500 when showing a DataFrame.

# Functions


- Performed actions such as creating headers, resetting index, changing column names, melting columns, converting types, merging, creating new columns, and 
  calculating averages.

- Saved the transformed dataframes in Excel format for local download.

  The resulting dataframes are df_region, df_country, and df_canada.


# Outcome
The analysis reveals a decline in fertility rates and an increase in life expectancy in Canada. Fertility dropped from 3.81 in 1960 to 1.61 in 2013, averaging 1.96 over the period, compared to North America's 2.02. Life expectancy in Canada increased from 71.13 in 1960 to 81.40 in 2013, averaging 76.32, compared to North America's 75.64. This trend contributes to Canada's demographic structure with more aged individuals than young ones and emphasizes the country's high immigration requirements. Future analyses may incorporate additional data, such as medical, education, and economic indicators, using advanced statistical tools to explore correlations, make predictions, and offer recommendations.   

