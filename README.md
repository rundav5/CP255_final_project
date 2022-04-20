# Did Government Restrictions Contained COVID-19 in Colombia?
**Rafael Unda** \
UC Berkeley | College of Environmental Design | Department of City and Regional Planning \
CYPLAN 255: Urban Informatics and Visualization \
Final Project \
Spring 2022


## Introduction

**My research question** is if mobility restrictions worked to contain COVID-19 infection and deaths in Colombia. To answer the question, I will analyze and visualize cases and deaths over time and compare it to mobility restriction measures or proxys. The following are the **datasets** used in this project: 
1. [Confirmed COVID-19 cases reported by Colombian National Government](https://www.ins.gov.co/Noticias/Paginas/coronavirus-casos.aspx)
2. [The Oxford Stringency Index (OSI)](https://www.bsg.ox.ac.uk/research/research-projects/covid-19-government-response-tracker)
3. [COVID-19 Google Mobility Reports](https://www.google.com/covid19/mobility/)
4. ~~[COVID-19 Apple Mobility Trends Report](https://covid19.apple.com/mobility)~~ (As of April 14, 2022, Apple is no longer providing COVID-19 mobility trend reports)

Several online portals, such as [Our World in Data](https://ourworldindata.org/coronavirus), [Coronavirus tracker](https://gorkang.shinyapps.io/2020-corona/), and [Financial Times](https://www.ft.com/content/a2901ce8-5eb7-4633-b89c-cbdf5b386938), developed and published COVID-19 data visualizations and comparisons at a global and country scale. Nevertheless, those analyses do not differenciate between dates related to each case. For example, there is a difference between analyzing the number of daily cases by date of report than by date of diagnosis. The COVID-19 curves comparisons have been usually made based on the date of report, that can have "delay" of two (2) or three (3) weeks from the date of infection. This represents a crucial limitation to evaluate the real effect of policy measures, such as mobility restrictions, to contain the spread of the virus.


## Cases in Colombia

The Colombian government offers a case-by-case dataset of the confirmed COVID-19 infections since the beginning of the pandemic. This means that to-date, that dataset has more than 6 million records (the number of confirmed COVID-19 cases in the country). As a reference, Colombia has approximately 48 million inhabitants.

![image](https://user-images.githubusercontent.com/90360629/164156943-fa086531-b907-4ca6-8b86-58fa92be92fe.png)
*Image from: https://www.eltiempo.com/files/image_950_534/uploads/2020/03/25/5e7b553bac37b.jpeg*

The dataset is updated every 24 hours and can be accessed through and API (as shown in the following chunks of code). Something crucial for this analysis is the differentiation between the report and the infection dates. The Colombian dataset has the advantage that reports several dates related to each confirmed case, such as: 
- Date of report
- Date of beginning of symptoms
- Date of diagnosis
- Date of recovery
- Date of death

Having access to those dates is what allows to correlate infection (using the date of beginning of symptoms and diagnosis as proxys) with the level of mobility.

![image](https://user-images.githubusercontent.com/90360629/164156356-477d0dd1-7af1-42fc-9f4f-45958447ca57.png)

