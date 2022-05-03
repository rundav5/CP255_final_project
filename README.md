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

Several online portals, such as [Our World in Data](https://ourworldindata.org/coronavirus), [Coronavirus tracker](https://gorkang.shinyapps.io/2020-corona/), and [Financial Times](https://www.ft.com/content/a2901ce8-5eb7-4633-b89c-cbdf5b386938), developed and published COVID-19 data visualizations and comparisons at a global and country scale. Nevertheless, those analyses do not differenciate between dates related to each case. The COVID-19 curves comparisons have been usually made based on the date of report, which represents a crucial limitation to evaluate the real effect of policy measures, such as mobility restrictions, to contain the spread of the virus.

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

Although similar in their general shape, the daily cases curve looks different when it's analyzed by date of beginning of symptoms or diagnosis, as it is shown in the following figure. There is a "delay" of two (2) to three (3) weeks in the daily cases curve by report date in comparison to the curve by date of beginning of symptoms or diagnosis, which makes a big difference to understand if lockdowns and other restrictions correlate or not to the evolution of infection.

![image](https://user-images.githubusercontent.com/90360629/166570689-5f6358b1-0a0b-4b84-8137-181cd9e9e48a.png)

## Government Stringency and Mobility Reduction

### Oxford Stringency Index (OSI)
[The Oxford Stringency Index (OSI)](https://www.bsg.ox.ac.uk/research/research-projects/covid-19-government-response-tracker) is an indicator of the policy measures adopted by governments in response to COVID-19 pandemic. It takes into account over 20 indicators, such as school closures, travel restrictions, and vaccionation policies.

The following figure shows the OSI for Colombia and Argentina, United States, and United Kingdom for comparison. A higher OSI means stronger restrictions. Compared to the other selected countries, at the beginning of the pandemic the Colombian Government responded with strong restrictions (OSI over 80) that were kept up to five (5) months, until September 2020. Later, there was a period of four (4) months in which restrictions eased a little bit (OSI around 60) to then come back up again close to the first wave stringency. Since then, the OSI for Colombia seems to be gradually decreasing with short periods of time of exception.

![image](https://user-images.githubusercontent.com/90360629/166574546-333217e9-a368-4981-862c-8af99e788d59.png)

### Google Mobility Reports (GMR)
The [COVID-19 Google Mobility Reports](https://www.google.com/covid19/mobility/) offer a relative comparison of the access to different ammenities since the beginning of the pandemic, based on cellphone location data.

The following figure shows the daily "mobility change" in six different ammenities since the beginning COVID-19 in Colombia.

![image](https://user-images.githubusercontent.com/90360629/166596066-21ab6403-e934-4ba6-864f-596e6287aaf0.png)

The daily variation of GMR indicators makes it difficult to visualize the long-term tendency of mobility changes. I smoothed the indicator by applying a 7-day moving average to avoid small variations within a single week, as it is shown in the following figure.

![image](https://user-images.githubusercontent.com/90360629/166590687-98225e41-cc82-4110-991e-2e8cdc621db9.png)

The following figure shows the smoothed mobility changes in each ammenities' actegory after applying the 7-day moving average. With the exception of "Residence", all categorias have a similar evolution from the beginning of COVID-19 until today. Nevertheless, I highlight the "Workspace" because of its relevance and the fact that is stays within the variation of the other categories during almost all the analyzed time-series. 

![image](https://user-images.githubusercontent.com/90360629/166591079-469ba0b2-86ec-4094-a790-5b929307ae31.png)

### Did Restrictions Reduce Mobility?

Recognizing that the GMR data is limited, the following figure shows that in a national scale, when policiy restrictions were more strict, mobility didn't decrease.


## Cases vs Restrictions & Mobility

## Analysis for Main Cities

### Bogotá

![image](https://user-images.githubusercontent.com/90360629/166571962-f75d601f-7bac-439c-81b7-8141747f11d2.png)


## Next steps
1. Finish polishing some figures
3. Figure out a cool way to combine the case curve with the stringency indicators
4. Reproduce analysis for main cities
5. Write discussion and conclusions
6. Review and apply GitHub best practices, so that everything needed to run the project in other computer is available and organized in a repo.

