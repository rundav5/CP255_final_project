# Did Government Restrictions Contain COVID-19 in Colombia?
**Rafael Unda** \
UC Berkeley | College of Environmental Design | Department of City and Regional Planning \
CYPLAN 255: Urban Informatics and Visualization \
Final Project \
Spring 2022


## Introduction

**My research question** is if mobility restrictions worked to contain COVID-19 infection in Colombia. To answer the question, I will analyze and visualize cases over time and compare it to mobility restriction measures or proxys. The following are the **datasets** used in this project: 
1. [Confirmed COVID-19 cases reported by Colombian National Government](https://www.ins.gov.co/Noticias/Paginas/coronavirus-casos.aspx)
2. [The Oxford Stringency Index (OSI)](https://ourworldindata.org/explorers/coronavirus-data-explorer)
3. [COVID-19 Google Mobility Reports](https://www.google.com/covid19/mobility/)
4. ~~[COVID-19 Apple Mobility Trends Report](https://covid19.apple.com/mobility)~~ (As of April 14, 2022, Apple is no longer providing COVID-19 mobility trend reports)

## Cases in Colombia

Several online portals, such as [Our World in Data](https://ourworldindata.org/coronavirus), [Coronavirus tracker](https://gorkang.shinyapps.io/2020-corona/), and [Financial Times](https://www.ft.com/content/a2901ce8-5eb7-4633-b89c-cbdf5b386938), developed and published COVID-19 data visualizations and comparisons at a global and country scale. Nevertheless, those analyses do not differenciate between dates related to each case. For example, there is a difference between analyzing the number of daily cases by date of report than by date of diagnosis. The COVID-19 curves comparisons have been usually made based on the date of report, that can have "delay" of two (2) or three (3) weeks from the date of infection. This represents a crucial limitation to evaluate the real effect of policy measures, such as mobility restrictions, to contain the spread of the virus.

The Colombian government offers a case-by-case dataset of the confirmed COVID-19 infections since the beginning of the pandemic. This means that to-date, that dataset has more than 6 million records (the number of confirmed COVID-19 cases in the country). As a reference, Colombia has approximately 48 million inhabitants.

![image](https://user-images.githubusercontent.com/90360629/164156943-fa086531-b907-4ca6-8b86-58fa92be92fe.png)
*Image from: https://www.eltiempo.com/files/image_950_534/uploads/2020/03/25/5e7b553bac37b.jpeg*

The dataset is updated every 24 hours and can be accessed through and API (as shown in the following chunks of code). Something crucial for this analysis is the differentiation between the report and the infection dates. The Colombian dataset has the advantage that reports several dates related to each confirmed case, such as: 
- Date of report
- Date of beginning of symptoms
- Date of diagnosis
- Date of recovery
- Date of death

Having access to those dates is what allows to correlate infection (using the date of beginning of symptoms and diagnosis as proxys) with the level of mobility. The following figure shows the number of daily cases by the report date and the 7-day moving average to adjust for week-days variance.

![image](https://user-images.githubusercontent.com/90360629/166570370-5ef68e03-c6f5-405e-b37e-cfbfe165cdb5.png)

Although similar in their general shape, the daily cases curve looks different when it's analyzed by date of beginning of symptoms or diagnosis, as it is shown in the following figure. There is a 2-3 weeks "delay" in the daily cases curve by report date in comparison to the curve by date of beginning of symptoms or diagnosis, which makes a big difference to understand if lockdowns and other restrictions correlate or not to the evolution of infection.

![image](https://user-images.githubusercontent.com/90360629/166570689-5f6358b1-0a0b-4b84-8137-181cd9e9e48a.png)

## Government Stringency and Mobility Reduction

### Oxford Stringency Index (OSI)
[The Oxford Stringency Index (OSI)](https://www.bsg.ox.ac.uk/research/research-projects/covid-19-government-response-tracker) is an indicator of the policy measures adopted by governments in response to COVID-19 pandemic. It takes into account over 20 indicators, such as school closures, travel restrictions, and vaccionation policies.


![image](https://user-images.githubusercontent.com/90360629/164157685-2afa4d4a-7660-44fe-adf8-a39385c58aff.png)

![image](https://user-images.githubusercontent.com/90360629/164157711-66630b83-89be-45bf-85ee-8d57eee5046e.png)

### Google Mobility Reports (GMR)
The source of this dataset is [COVID-19 Google Mobility Reports](https://www.google.com/covid19/mobility/)

![image](https://user-images.githubusercontent.com/90360629/164159192-f2043bd7-7b4b-4faf-ad76-b0d0914bbb6e.png)

![image](https://user-images.githubusercontent.com/90360629/164159216-d7ae7c46-18e8-4cf2-bade-c00316794dca.png)

![image](https://user-images.githubusercontent.com/90360629/164159243-3c3d061e-128b-49d9-aab0-a47bddafd096.png)

## Analysis for Main Cities

### Bogotá

![image](https://user-images.githubusercontent.com/90360629/166571962-f75d601f-7bac-439c-81b7-8141747f11d2.png)


## Next steps
1. Finish polishing some figures
3. Figure out a cool way to combine the case curve with the stringency indicators
4. Reproduce analysis for main cities
5. Write discussion and conclusions
6. Review and apply GitHub best practices, so that everything needed to run the project in other computer is available and organized in a repo.

