# Plotly maps with Florida counties

Activate a virtual environment (can be one you already had) and install Plotly with pip:

```
pip install plotly==5.7.0
```

For more information, see:
https://pypi.org/project/plotly/

Plotly is free to use:
https://plotly.com/python/is-plotly-free/#is-plotly-for-python-free

You will also need to install pandas in the same virtual environment.

```
pip install pandas
```

To test and perfect your code, work with Plotly in a Jupyter Notebook at first. Later you can put the code into a Flask app. This will also save you time in future projects, because your notebook will show you everything you did to get your map to work.

This install is recommended for use with Jupyter Notebooks:

```
pip install "notebook>=5.3" "ipywidgets>=7.5"
```

Import Plotly into your project:

```
import plotly.express as px
```

`as px` allows us to use `px` as a shorthand before each Plotly function we call in our code.

You can test that Plotly is working with these two lines, which will display a simple three-column chart (not a map) in Jupyter:

```
fig = px.bar(x=["a", "b", "c"], y=[1, 3, 2])
fig.show()
```

## Plotly for creating maps

Plotly does more than just maps, but here we will focus on maps: 
https://plotly.com/python/maps/

We will follow these instructions to create a choropleth map:
https://plotly.com/python/choropleth-maps/

One change to those instructions: Instead of `urlopen`, we will use `requests`.  Make sure you have the Requests library installed in your virtual environment.

Find FIPS codes for U.S. states, countries, Congressional districts, etc., here:
https://www.census.gov/library/reference/code-lists/ansi.html

Find up-to-date shapefiles for U.S. states, countries, Congressional districts, etc., here:
https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html

## Changing the Plotly map layout, etc.

Changing the map layout attributes:

* https://plotly.com/python/reference/layout/geo/

See also:

* https://plotly.com/python/reference/layout/
* https://plotly.com/python/reference/choropleth/

Changing the color scale:

* https://plotly.com/python/builtin-colorscales/
