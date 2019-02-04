
# Class #2

### ScatterPlot

Continuing from last class, let's look at Plot.ly again. This time we'll look at the Python version of the scatterplot.

* [Python scatter plot demo](https://plot.ly/python/line-and-scatter/#style-scatter-plots) -- plot.ly

What's going on here, and how does it compare to "matplotlib"? Plot.ly is...

* Manipulating data on the fly (array manipulations, random number generation)
* Web capable (JavaScript and Python APIs are closely related in Plot.ly, matplotlib needs Jupyter server to work in a browser)
* Interactive (matplotlib 3 has "events" too ([reference](https://matplotlib.org/users/event_handling.html), but only on the desktop, unless it's in a Jupyter notebook)
* Able to integrate slippy maps (matplotlib requires Jupyter (https://github.com/mapbox/mapboxgl-jupyter))
* Capable of 3D charts and graphs (matplotlib too)
* Customizable (within limits) (matplotlib too)

Limitations (looking under the hood)...

* Python version needs a server or desktop application (Jupyter Notebook uses the desktop as a server)
* JavaScript version does not require a server (all computations and rendering are done locally)
* Customization depends on integration with HTML5 (you can see hints of HTML5 in plot.ly)

Demo -- Scatterplot (revisited)

Objective: reproduce the Python demo in JavaScript, and highlight the issues/differences

* To set two cross hairs that intersect the origin (no ticks or labels on the cross hairs and no axex on the edges)
* 863-by-525 (svg dimensions in python plot.ly)

## google: array map python

* https://stackoverflow.com/questions/10973766/understanding-the-map-function
* compare this with d3.range().map() -- as seen in the SVG example of "Introduction to HTML"

Show the progression...

1. Math.random() - .5 to 
2. d3.randomNormal(1, 0) to 
3. using d3.range(1,1000).map()
4. set the dimension
5. create the independent web page in a gist (only in JavaScript)
6. view the independent web page and code from bl.ocks.org

JavaScript references...

* [Plotly.js reference docs](https://plot.ly/javascript/reference/) -- plot.ly
    * [javascript axes examples](https://plot.ly/javascript/axes/)
* [D3.js API docs](https://github.com/d3/d3/blob/master/API.md)
    * [d3-random.js API docs](https://github.com/d3/d3-random)

### Chloropleth Map

Python map...

https://plot.ly/python/choropleth-maps/

### Slippy Maps in Python

* [plot.ly python on mapbox](https://plot.ly/python/scattermapbox/)
* [mapbox pricing](https://www.mapbox.com/pricing/)

### Reading

* [Introduction to code](https://beta.observablehq.com/@mbostock/introduction-to-code)
    * We'll keep visiting this is a helpful reference (it was assigned in the first class)
    * Note: There's an example near the bottom that shows how to generate an array of random numbers.
* [Introduction to HTML](https://beta.observablehq.com/@mbostock/introduction-to-code)
    * You don't need all of this, but you should know how to add HTML to an Observable notebook.
    * For example, we added an HTML "div" element `<div id="myDiv"></div>` to the DOM (Document Object Model) in the first class)
    * Introduces Markdown tagging with "md", which is simpler than HTML for formatting text (optional)
    * Introduces Katex, which is a powerful way to format mathematical expressions (optional)

### References 

* [Introduction to notebooks](https://beta.observablehq.com/@mbostock/introduction-to-notebooks) -- Overview of Observable
* [How saving works](https://beta.observablehq.com/@mbostock/how-saving-works) -- Saving, Publishing and Forking Observable notebooks

### Optional reading

* [Introduction to D3](https://bost.ocks.org/mike/d3/workshop/) -- A nice presentation, although a bit old (2012)
