---
name: (Final Data Visualization) Will Covid_19 Coexist with Human-Beings Forever?
tools: [Python, Altair, vega-lite]
image: assets/pngs/final_confirmed_cases.png
description: This is the final Data Visualization Project "Will Covid_19 Coexist with Human-Beings Forever?", using python, altair and vega-lite for interactive data visualization!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Will Covid_19 Coexist with Human-Beings Forever?
##### Group 3 
##### Member: Henry Chen (tc30), Yizhan Xue (yizhanx2), Yichuan Hu (yh42), Yuxuan Jiang (yj26)
<br> 
#### Overview

###### Covid-19 is caused by a virus called SARS-CoV-2. It is a member of the coronavirus family, which also includes common viruses that cause more serious but less frequent disorders. Coronaviruses, like many other respiratory viruses, spread swiftly by droplets that are emitted from the mouth or nose when breathing, coughing, sneezing, or speaking. Covid-19 disease was firstly discovered in December, 2019 in Wuhan, China. It's very infectious and has spread rapidly over the world. Nowadays, it's almost been three years since first discovered, the dsease is still spreading in most of the countries in the world. And it may raise the problem,will Covid-19 coexist with human-beings forever?

###### In order to dig into the topic further more, we searched all types of dataset online and decided to use the dataset called "United States COVID-19 Cases and Deaths by State over Time" from DATA.GOV, "time_series_covid19_deaths_global.csv", and "time_series_covid19_recovered_global.csv" from John Hopkins University CSSEGISandData. The CDC publishes daily online total figures of COVID-19 cases and deaths. Based on these most recent figures provided by states, territories, and other jurisdictions, data on the COVID-19 website and the CDC's COVID Data Tracker are used. 

<br> 
#### Global Covid-19 Trending Analysis

###### To take a glance at the virus' spread global trending, we import two datasets recorded by JHU(link: https://github.com/CSSEGISandData/COVID-19), which have included both deaths data and confirmed data. Since the dataset contains almost 200 countries, we pick 22 countries from every corner of the world as targets.

###### As we can see in these particular data visualizations below are the numbers of confirmed cases and death cases of Covid-19 by month from January 2020 to December, 2022. You may get confused by the great drop of number at the point of December, 2022. That is because the time this report was formed, it was just the very beginning of December and the number cannot prove anything.But still in the period between January 2020 and November 2022, we can get an estimate trend of Covid-19. In January 2020, some countries like China started to have cases. Then later, some other countries started to have cases as well. The curves shows very clear that it is gradually flatten. This means the cases and deaths numbers are dropping down gradually. From these two visualizations, we can conclude that the death rate of Covid is dropping very quick, but the Covid-19 seems to be coexisted with human-beings forever.  
<vegachart schema-url="{{ site.baseurl }}/assets/json/countries_confirmed_lines.json" style="width: 100%"></vegachart>
<vegachart schema-url="{{ site.baseurl }}/assets/json/countries_death_lines.json" style="width: 100%"></vegachart>

<br> 
#### US Domestic Trending Analysis

###### AThrough making comparisons among countries, there is a similar trend that the number of people influenced by the virus increases sharply at the front, than remain stable, and decreases gradually in this year. The toxicity of the virus is gradually weakening. What about the United States? Does each state has the same trend?

###### To understand domestic situation better, we find data recorded by CDC (link: https://data.cdc.gov/). As we can see in the bubble plot below, it shows the new cases number of Covid-19 in United States within different states. In the graph, the bigger the bubble is, the bigger the number it represent case number is. Because of the difference in population, some big states like California, Texas and Florida always have the top new cases numbers. This fact is also reflected in the bar chart of sum of new cases below. Even though there are a lot of elements in the graph, we can still get an estimate trend of new cases count. For the data we have here, from March 2020 to October 2022, it some times increase and some times decrease and we don't see any significant decrease or increase trend of it. So after the analysis, we thought the Covid-19 diease is still going to be out there and may coexist with human-beings forever.

<vegachart schema-url="{{ site.baseurl }}/assets/json/final_dashboard.json" style="width: 100%"></vegachart>


###### The most likely long-term result of Covid-19 is that the disease becomes endemic in significant portions of the world, continuously circulating among people but generating fewer occurrences of severe illness. COVID-19 may eventually turn into a minor pediatric sickness, similar to the four endemic human coronaviruses that cause the common cold, years or even decades from now.

<br> 
#### Work Cited
###### 1. Multi-line highlight. Multi-Line Highlight - Altair 4.2.0 documentation. (n.d.). Retrieved December 2, 2022, from https://altair-viz.github.io/gallery/multiline_highlight.html 
###### 2. Main Dataset: https://data.cdc.gov/
###### 3. Contextual Datasets: https://github.com/CSSEGISandData/COVID-19


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://data.cdc.gov/api/views/9mfq-cb36/rows.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/MarcccHuuu/MarcccHuuu.github.io/blob/main/python_notebooks/Group3-FinalProject-Part3.ipynb" text="The Analysis" %}
</div>
