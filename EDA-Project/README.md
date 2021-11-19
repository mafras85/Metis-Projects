# Analysing MTA Traffic Data From Summer 2021

### Abstract

In this project we applied exploratory data analysis best practices to analyze publicly available MTA turnstile data in order to help WomenTechWomenYes to recruit attendees for their annual summer gala. We used publicly available data from the MTA website and after cleaning, resampling, aggregating and plotting it by different python packages, we demonstrated inherent seasonality in the data at different levels.


### Design

The project has been designed upon request from WomenTechWomenYes to improve and optimize the allocation of their street team. The ultimate goal was to extract general patterns in station traffic across the NYC subway stations and identify the stations with highest traffic.

### Data

13 weeks of weekly recorded data from 5030 turnstiles across 478 stations in the MTA network had been used. The data covers summer 2021 (from June 5 to September 4). In addition to comprehensive cleaning, resampling and interpolation was also required as the recording intervals are very irregular in the data set.

### Tools

SQL and python packages such as Panda and Numpy were used for exploration, cleaning, and interpolation of the data. Visualization packages including Matplotlib and Seaborn were used to plot the results.

### Results

Stations with top traffic have been uncovered. We found out that Times SQ station is no longer at top of the list of the stations with the most traffic. That most probably is due to profound effects of the pandemic on peoples movement across the country and the globe as Times SQ is a main tourist attraction of NYC. Based on our findings stations have the highest traffic on Mid-week days (Tuesday, Wednesday and Thursday). Although all of the top 10 stations have a high traffic during the morning rush hours, a distinct pattern of traffic can be seen in different stations in later time periods of the day. To name a few, Union Sq has a considerable amount of traffic during the mid-day hours (noon-4:00pm) and weekends. Port Authority and Grand central are busy evening stations while Port Authority has a high weeked traffic as well. Herald Sq. and Penn Station are very busy in late evening hours (8:00pm-midnight). Last but not least, we recommend WomenTechWomenYes focus on Union Sq., Fulton Station, Flushing Main Station and Canal St. Station as they are located outside Manhattan midtown and would help them maximize their reach.

![34 ST-PENN STA-Entries](https://user-images.githubusercontent.com/84594280/142650684-fc64788d-98e7-4f36-8502-50c94926fc78.png)



Additional plots and analysis on specific stations can be made upon request.
