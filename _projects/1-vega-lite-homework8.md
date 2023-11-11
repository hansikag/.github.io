---
name: Homework 8
tools: [Python, HTML, vega-lite]
---


# Plot 1: 

Example that came with the template:

<vegachart schema-url="{{ site.baseurl }}/assets/json/agency_frequency.json" style="width: 100%"></vegachart>

The first visualization is a bar chart that shows the frequency of buildings owned by each agency. The x-axis represents the ‘Agency Name’ and the y-axis represents the frequency. Each bar in the chart represents an agency, and the height of the bar indicates the number of buildings owned by that agency. The color of the bar is determined by the count, with darker colors indicating higher frequencies. This plot does not involve any data transformations on the analysis side. The interactivity in this plot is limited to the ability to hover over a bar to see the exact count.



## Plot 2:

Simple barplot specification:

<vegachart schema-url="{{ site.baseurl }}/assets/json/constructed.json" style="width: 100%"></vegachart>

The second visualization is a scatter plot that represents the relationship between the year a building was constructed and the year it was acquired by different agencies. The x-axis represents the ‘Year Constructed’ and the y-axis represents the ‘Year Acquired’. Each point on the plot represents a building, and the color of the point indicates the agency that owns the building. The color encoding is based on the ‘Agency Name’ field. A dropdown selection is provided for users to select a specific agency, and the points corresponding to that agency are highlighted in the plot. This interactivity allows users to focus on the data for a specific agency, making the visualization more clear and interesting. The data transformations involved in this plot include filtering the data based on the selected ‘Agency Name’.



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/hansikag/online_cv_public/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
