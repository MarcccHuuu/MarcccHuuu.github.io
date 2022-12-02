---
name: Data Visualization for Week 10
tools: [Python, Altair, vega-lite]
image: assets/pngs/final_vis_state_cases.png
description: This is the final Data Visualization Project "Will Covid_19 Coexist with Human-Beings Forever?", using python, altair and vega-lite for interactive data visualization!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Final Project: Will Covid_19 Coexist with Human-Beings Forever?


### Visualization 1 (No Interactivity)
Description: the relationship of cloud_cover and mean of visibility when bfro happens (result: the more cloud_cover, the visibility goes down)  
Encoding type: X - quantitative, Y - quantitative  
Color scheme: None  
Design: because when two variables pair well, using a scatter plot is a great way to show the relationship, so using a scatter chart to see if it's a positive or negative correlation between cloud_cover and visibility when bfro happens.  
Data Transformations: the transformation for the data is that we aggregates the visibility data based on the cover_over, then calculate its mean to see how the relationship between visibility and cloud_cover is, when bfro happens.

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatterplot.json" style="width: 100%"></vegachart>

### Visualization 2 (Interactive)
Description: the relationship of visibility and humidity when bfro happens and the corresponding bfro times in each state  
Color scheme: the bin cell is aggregated by the count of records, the color bar represents different levels of occurance of bfro, shown in the cell.  
Encoding type: in plot 1, X - quantitative, Y - quantitative; in plot 2, X - nominal, Y - quantitative.  
Interactivity: select an area from the color map, and display the number of bfro in each state, which is not only focusing on one area, it can be selected for a part of areas, it can be one, two or more, so people can see more data and data distribution in the histogram.  
Design: A color map is a great chart to show the number of bfro based on the visibility and humidity, and for the interaction perspective, select an area from the color map, and display the number of bfro in each state, a perfect chart is a histogram, therefore, it comes out the final design, to complete these two plots, because based on the humidity, visibility, state, and bfro data type, the encoding type in color map is quantitive and in the histogram, the x label is encoded as nominal and y label is encoded as quantitative.  
*Quoted vega-lite code from Homework 9:  
"{ "data":{"url":"https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv"}, "mark": "rect", "height": 200, "width": 400, "encoding":{ "x":{"bin":{"maxbins":50},"field":"visibility", "type":"quantitative"}, "y":{"bin":{"maxbins":30}, "field":"humidity", "type":"quantitative"}, "color":{"aggregate":"count","type":"quantitative"} }" "{ "data": {"url": "https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv"}, "mark":{"type": "bar", "color": "red"}, "height": 200, "width": 400, "encoding": { "x": {"field": "state", "type": "nominal"}, "y": {"aggregate": "count", "field": "state", "type": "quantitative"} } }"  
*Modification for interactivity: adjust the plot size (smaller) to make them exists in one line and interact well. And to work with Altair, I delete the comment version of javascript and add "alt.Chart.from_dict" to work in the python environment. Last but not least, Add the interactive code part.  
Data Transformations: Data Transformations: the transformation for the data is that we count the total occurance of bfro based on the cover_over and visbility data, then displays its total occurance in each state in the distogram to see a deeper relationship between the visibility and cloud_cover and bfro.

<vegachart schema-url="{{ site.baseurl }}/assets/pngs/final_vis_state_cases.png" style="width: 100%"></vegachart>


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://data.cdc.gov/api/views/9mfq-cb36/rows.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/MarcccHuuu/MarcccHuuu.github.io/blob/main/python_notebooks/Group3-FinalProject-Part3.ipynb" text="The Analysis" %}
</div>

