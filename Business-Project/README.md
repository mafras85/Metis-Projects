## Battling COVID-19 Fatalities in Post-Vaccination United States

### Abstract

COVID-19 has still a high number of fatalities in the United States despite the widespread vaccination campaign. Data science can be utilised in order to help the Center for Disease Control (CDC), federal government and state governments to have COVID-19 in check. Although there is currently a vaccine surplus in the US, the vaccination rate seems to have reached a plateau in summer 2021 with almost 56% of Americans fully vaccinated. This decline in vaccination rate was followed by a surge in the number of new cases and deaths towards the end of the summer. Close to 90% of these casualties were not vaccinated. Due to the fact that any potential "vaccine mandate '' would almost certainly not survive the current lineup of the Supreme Court of the United States (SCOTUS), the need for a new  strategy to control and lower the number of COVID-19 related deaths is strongly felt. Here we propose a strategy based on data science common and best practices to help the federal government to overcome this task.

### Design

__Impact__: If a strategy can be devised to prioritize the focus point for CDC and governments and then to identify the more susceptible areas across the country based on that focus point then these entities can reallocate their resources to most vulnerable regions in a much more efficient manner and that would enables them to lower the number of COVID related deaths.

__Beneficiaries__: As mentioned above, the main beneficiary of this proposal are state governments.

__Data Science Solution__: Publicly available vaccination data (from CDC) and demographic data (from Census Bureau) were and will be used in this project in order to identify the most vulnerable groups and areas to COVID-19.

### Methodology and Tools

In the initial analysis, overall COVID fatality numbers were broken down to two categories of metro areas and non-metro areas. Next, as age has been identified as the single most accurate predictor of COVID-19 fatalities, an arbitrary "Risk Index" were defined for each county in the nation as follow:

__Risk Index = +65 Population (%) / +65 Vaccination Rate (%)__

This index has a direct relationship with the population of over 65 residents and has an inverse relationship with the vaccination rate in this age group. The counties with a larger Risk Index, were deemed as higher risk areas. Using this index, more than 3000 US counties were mapped based on their vulnerability to COVID-19.

### Results

It has been discovered that after the initial stages of the pandemic back in summer 2020, non-metro mortality rate was much higher than that of the metro areas (at times the two were roughly equal). This gap has been widened especially after the peak of the vaccination campaign and in the latest surge of new cases and deaths (more than double in late september). So redirection of resources towards non metro, rural areas, seems to be a viable strategy in keeping the mortality numbers low, especially because the metro areas have already benefited from better infrastructure (more ICU beds, better healthcare system, higher doctor to patient ratio, etc.)

Mapping of counties based on their corresponding risk indices, further revealed the most vulnerable counties in the nation. The results show the two states of West Virginia and Georgia with the highest number of counties in the top 50 must at risk counties. It further consolidates the finding that the rural areas are more susceptible, as none of the top 50 high risk counties are located in a metro area.

For future, risk metrics other than age (income, race, social background, etc.) can be used to further determine the degree of vulnerability of the counties across the country. Also predictive models can be built in order to further investigate the relationship between different presumed risk factors and the actual risks that threatens each county. 

### Communications

A dashboard containing the visuals and charts referenced above can be viewed at this address:

https://public.tableau.com/app/profile/milad.afrasiabi/viz/COVID-19ProjectDashboard/COVID-19Dashboard
