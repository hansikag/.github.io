---
name: Final Part 3.1
tools: [Python, HTML, vega-lite]

description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Plot 1: Frequency of Agencies

<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive_chart.json" style="width: 100%"></vegachart>

Write Up for Plot 1:

The first visualization is a bar chart that shows the frequency of buildings owned by each agency. The x-axis represents the ‘Agency Name’ and the y-axis represents the frequency. Each bar in the chart represents an agency, and the height of the bar indicates the number of buildings owned by that agency. The color of the bar is determined by the count, with darker colors indicating higher frequencies. This plot does not involve any data transformations on the analysis side. The interactivity in this plot is limited to the ability to hover over a bar to see the exact count.

Encoding for Plot 1: 

The code I've used is using the Altair library for Python to create a bar chart. In this chart, the encoding types used are nominal (N) and quantitative (Q).

Nominal (N): In my code, ‘Agency Name’ is encoded as nominal. This means that the ‘Agency Name’ column contains categorical data where no particular order is necessary.

Quantitative (Q): In my code, the count function (count()) is encoded as quantitative. This means that the count of each ‘Agency Name’ is a measured quantity.

The color encoding is also using the count() function, which means the color of the bars will represent the frequency of each ‘Agency Name’.

## Plot 2: Construction and Acquired Dates for different Agencies

<vegachart schema-url="{{ site.baseurl }}/assets/json/constructed.json" style="width: 100%"></vegachart>

Write Up for Plot 2:

The second visualization is a scatter plot that represents the relationship between the year a building was constructed and the year it was acquired by different agencies. The x-axis represents the ‘Year Constructed’ and the y-axis represents the ‘Year Acquired’. Each point on the plot represents a building, and the color of the point indicates the agency that owns the building. The color encoding is based on the ‘Agency Name’ field. A dropdown selection is provided for users to select a specific agency, and the points corresponding to that agency are highlighted in the plot. This interactivity allows users to focus on the data for a specific agency, making the visualization more clear and interesting. The data transformations involved in this plot include filtering the data based on the selected ‘Agency Name’.

Encoding for Plot 2: 

Quantitative (Q): In my code, ‘Year Constructed’ and ‘Year Acquired’ are encoded as quantitative. This means that these columns contain numerical data that represent measured quantities.

Nominal (N): In my code, ‘Agency Name’ is encoded as nominal. This means that the ‘Agency Name’ column contains categorical data where no particular order is necessary.

The color encoding is using a conditional statement based on the selection. If a particular ‘Agency Name’ is selected from the dropdown, the points corresponding to that agency will be colored based on the nominal encoding of ‘Agency Name’. If not, they will be colored light gray.

## Transformations:
No transfromations were made to the datasets before processing. 

### Similarity to Homework #7

Both plots are similar to those created in Homework #7, but with modifications to work with Altair. Specifically, the code for creating the plots has been adapted to use Altair’s syntax and functionality. The interactivity in the first plot, which involves a dropdown selection, is a new addition that was not present in Homework #7. The color encoding in the second plot is also a new addition.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/hansikag/online_cv_public/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>