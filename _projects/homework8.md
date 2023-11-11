---
name: Homework 8
tools: [Python, HTML, vega-lite]
---


# Example including vega-lite

Example that came with the template:

<vegachart schema-url="{{ site.baseurl }}/assets/json/agency_frequency.json" style="width: 100%"></vegachart>

## From the vega-editor

Simple barplot specification:

<vegachart schema-url="{{ site.baseurl }}/assets/json/constructed.json" style="width: 100%"></vegachart>



<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
