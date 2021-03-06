# Did Government Restrictions Contain COVID-19 in Colombia?
**Rafael Unda** \
UC Berkeley | College of Environmental Design | Department of City and Regional Planning \
CYPLAN 255: Urban Informatics and Visualization \
Final Project \
Spring 2022

## Introduction

**My research question** is if mobility restrictions worked to contain COVID-19 infection in Colombia. To answer the question, I will analyze and visualize cases over time and compare it to mobility restriction measures or proxies. The following are the **datasets** used in this project: 
1. [Confirmed COVID-19 cases reported by Colombian National Government](https://www.ins.gov.co/Noticias/Paginas/coronavirus-casos.aspx)
2. [The Oxford Stringency Index (OSI)](https://ourworldindata.org/explorers/coronavirus-data-explorer)
3. [COVID-19 Google Mobility Reports](https://www.google.com/covid19/mobility/)
4. ~~[COVID-19 Apple Mobility Trends Report](https://covid19.apple.com/mobility)~~ (As of April 14, 2022, Apple is no longer providing COVID-19 mobility trend reports)

## Cases in Colombia

Several online portals, such as [Our World in Data](https://ourworldindata.org/coronavirus), [Coronavirus tracker](https://gorkang.shinyapps.io/2020-corona/), and [Financial Times](https://www.ft.com/content/a2901ce8-5eb7-4633-b89c-cbdf5b386938), developed and published COVID-19 data visualizations and comparisons at a global and country scale. Nevertheless, those analyses do not differenciate between dates related to each case. The COVID-19 curves comparisons have been usually made based on the date of report, which represents a crucial limitation to evaluate the real effect of policy measures, such as mobility restrictions, to contain the spread of the virus.

The Colombian government offers a case-by-case dataset of the confirmed COVID-19 infections since the beginning of the pandemic. This means that to-date, that dataset has more than 6 million records (the number of confirmed COVID-19 cases in the country). As a reference, Colombia has approximately 48 million inhabitants.

![image](https://user-images.githubusercontent.com/90360629/164156943-fa086531-b907-4ca6-8b86-58fa92be92fe.png)
*Image from: https://www.eltiempo.com/files/image_950_534/uploads/2020/03/25/5e7b553bac37b.jpeg*

The dataset is updated every 24 hours and can be accessed through and API. Something crucial for this analysis is the difference between the date of reports and other relevant dates related to the infection. The Colombian dataset has the advantage that reports several dates related to each confirmed case, such as: 
- Date of report
- Date of beginning of symptoms
- Date of diagnosis
- Date of recovery
- Date of death (when it applies)

Having access to those dates is what allows to correlate infection (using the date of beginning of symptoms and diagnosis) with the level of mobility. The following figure shows the number of daily cases by the report date and the 7-day moving average to adjust for week-days variance.

![image](https://user-images.githubusercontent.com/90360629/166570370-5ef68e03-c6f5-405e-b37e-cfbfe165cdb5.png)

Although similar in their general shape, the daily cases curve looks different when it's analyzed by date of beginning of symptoms or diagnosis, as it is shown in the following figure. There is a "delay" of two (2) to three (3) weeks in the daily cases curve by report date in comparison to the curve by date of beginning of symptoms or diagnosis, 

![image](https://user-images.githubusercontent.com/90360629/166570689-5f6358b1-0a0b-4b84-8137-181cd9e9e48a.png)

Additionally, symptoms do not appear immediately after infection or "contact" with the virus. [The incubation period, meaning the number of days between the infection and symptoms presenting, is about 5-6 days for COVID-19](https://www.webmd.com/lung/coronavirus-incubation-period#1), although it can vary a lot depending on the variant, the exposure, and the person's previous health conditions. The following figure shows the curve of daily COVID-19 cases in Colombia with an estimated date of infection, which makes a big difference to understand if lockdowns and other restrictions helped or not to reduce infection.

![image](https://user-images.githubusercontent.com/90360629/166814429-c76fd641-e17e-4a5a-b9d0-c05f9cd0e87b.png)

## Government Stringency and Mobility Reduction

### Oxford Stringency Index (OSI)
The [Oxford Stringency Index (OSI)](https://www.bsg.ox.ac.uk/research/research-projects/covid-19-government-response-tracker) is an indicator of the policy measures adopted by governments in response to COVID-19 pandemic. It considers over 20 indicators, such as school closures, travel restrictions, and vaccination policies.

The following figure shows the OSI for Colombia and Argentina, United States, and United Kingdom for comparison. A higher OSI means stronger restrictions. Compared to the other selected countries, at the beginning of the pandemic the Colombian Government responded with strong restrictions (OSI over 80) that were kept up to five (5) months, until September 2020. Later, there was a period of four (4) months in which restrictions eased a little bit (OSI around 60) to then come back up again close to the first wave stringency. Since then, the OSI for Colombia seems to be gradually decreasing with short periods of time of exception.

![image](https://user-images.githubusercontent.com/90360629/166807987-21661292-8a4e-45ad-8176-1d49b40f3707.png)

### Google Mobility Reports (GMR)
The [COVID-19 Google Mobility Reports](https://www.google.com/covid19/mobility/) offer a relative comparison of the access to different amenities since the beginning of the pandemic, based on cellphone location data. The following figure shows the daily "mobility change" in six different amenities since the beginning COVID-19 in Colombia.

![image](https://user-images.githubusercontent.com/90360629/166808036-347a1365-be2a-4a54-b36f-68f245a5c50b.png)

The daily variation of GMR indicators makes it difficult to visualize the long-term tendency of mobility changes. I smoothed the indicator by applying a 7-day moving average to avoid small variations within a single week, as it is shown in the following figure.

![image](https://user-images.githubusercontent.com/90360629/166808068-c04594c2-876e-470e-8690-aa94eeea761e.png)

The following figure shows the smoothed mobility changes in each category after applying the 7-day moving average. Apart from "Residence", all categories have a similar evolution from the beginning of COVID-19 until today. Nevertheless, I highlight the "Workspace" because of its relevance and the fact that is stays within the variation of the other categories during almost all the analyzed time-series. 

![image](https://user-images.githubusercontent.com/90360629/166808101-e01c631d-a9c0-4ec7-bafe-1554561a0774.png)

## Restrictions, Mobility Reduction, and Infection

OSI is an indicator of the level of stringency of the government's policies, but that doesn't necessarily mean that mobility was effectively reduced when the stringency increased. To answer my research question, I first checked if there is a correlation between the OSI and mobility, measured by the GMR data. I acknowledge that the GMR data is limited and biased towards a specific group of people, but there is no better indicator that I know of, and is definitely better than nothing. The following figure shows the evolution of the OSI and the mobility changes in the workplace from GMR since the pandemic started for Colombia.

![image](https://user-images.githubusercontent.com/90360629/166807720-32749a30-b531-4842-b833-3f95e323c55a.png)

The previous graph shows that there is some correlation between the OSI and mobility. Besides the first hit, in which the most stringent policies were in place, mobility decreased when stringency increased (see January 2021 and January 2022 in the graph above). Knowing that, I then graphed the OSI against the curve of daily COVID-19 cases by estimate date of infection. This is not a causal analysis, but if the government's restriction policies worked to contain infection, you would expect that rate growth of the COVID-19 cases curve by infection slows down or that the growing tendency of infection breaks in the next few days after the stringency increases. 

![image](https://user-images.githubusercontent.com/90360629/166828715-5ddcaf94-534b-4070-b269-35a9154d3e15.png)

Besides the initial hit of the pandemic, in which there were very little cases when the most stringent restrictions were imposed, there are three moments in time in which COVID-19 was widely circulating in Colombia and a significant increase of the OSI was observed:
- Beginning of January 2021
- Mid November 2021
- Mid December 2021

For the first two dates, when OSI increased, the COVID-19 daily cases curve by date of infection was already going down. For the third date, the curve peaked more than 9 days after OSI increased. **There is no evidence that suggests correlation between restrictions policies and infection in Colombia**.
