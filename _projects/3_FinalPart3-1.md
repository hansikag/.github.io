---
name: Pokemon Insights: Unveiling the Mysteries of Pokemon Stats
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a data journal highlighting stats about Pokemon
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# The Interactive Pokemon Stats Chart
# Documented by: Hansika Gaddamanugu
The centerpiece of my exploration is an interactive scatter plot that displays the Attack and Defense stats of each Pokémon, color-coded by their primary type (Type 1). The size of each point corresponds to the total stats of the Pokémon. I’ve represented Legendary Pokémon as squares, while non-legendary ones are circles. This plot allows us to observe patterns and trends in the data, such as the correlation between Attack and Defense, or the distribution of stats among different types. You can interact with the plot to explore more details about each Pokémon.

In the world of Pokémon, each creature has unique characteristics that define its abilities in battles. These characteristics include various stats such as Attack, Defense, and Speed, among others. The ‘Attack’ stat determines how much damage a Pokémon can inflict on its opponents, while the ‘Defense’ stat indicates how much damage it can withstand. These stats are crucial in determining the outcome of battles. In our central visualization, we plot these two stats against each other for each Pokémon, providing a comparative view of their offensive and defensive capabilities.

<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive_chart.json" style="width: 100%"></vegachart>

In addition to the central visualization, I made two contextual visualizations. The first is a bar chart showing the count of Pokémon for each Type 1. This gives us an idea of the distribution of types in the Pokémon universe.

The ‘Type’ of a Pokémon is another important characteristic. Each Pokémon belongs to one or two types, such as Fire, Water, Grass, etc., which determine its strengths and weaknesses in battles. For instance, Water-type Pokémon are strong against Fire types but weak against Electric types. In our visualizations, we use different colors to represent different types, allowing you to see the distribution of types and how they relate to the Pokémon’s stats.


<vegachart schema-url="/assets/json/bar_chart.json" style="width: 100%"></vegachart>

Finally, some Pokémon are designated as ‘Legendary’, indicating that they are extremely rare and possess extraordinary powers. In our dataset, this is represented by a ‘Legendary’ attribute. In our visualizations, we distinguish Legendary Pokémon from others using different shapes, allowing you to easily identify them and observe their stats.

The second contextual visualization is a stacked bar chart showing the count of legendary and non-legendary Pokémon across different generations. This helps us understand how the proportion of legendary Pokémon has evolved over time.

<vegachart schema-url="/assets/json/stacked_chart.json" style="width: 100%"></vegachart>


I made both of these visualizations from the initial dataset:  https://data.world/data-society/pokemon-with-stats

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://data.world/data-society/pokemon-with-stats" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/hansikag/hansikag.github.io/blob/fc51da0d31089b2ed275f9bc192dcc69aa0b9b8a/python_notebooks/Final3.1.ipynb" text="The Analysis" %}
</div>