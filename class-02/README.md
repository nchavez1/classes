
# Class #2

## ScatterPlot (revisited)

We'll revisit the Plot.ly scatterplot demo from the last class.
Specifically, we'll start with the Python version and convert it to JavaScript.
This will introduce 3 features/techniques...

    * data manipulation (with arrays/lists)
    * customizability
    * Web accessibility

* [Python scatterplot demo](https://plot.ly/python/line-and-scatter/#style-scatter-plots) -- plot.ly

The steps...

1. `Math.random() - .5`
2. Creating an array of random numbers (e.g., "Introduction to code")
    * https://beta.observablehq.com/@mbostock/introduction-to-code (see: randomWalk, near the bottom)
3. Introduction to D3.js
    * https://github.com/d3/d3/blob/master/API.md -- D3 API
    * https://github.com/d3/d3-array -- d3-array
3. Generating a Gaussian random number
    * https://github.com/d3/d3/blob/master/API.md#random-numbers-d3-random  -- d3-random
    * `d3.randomNormal(1, 0)`
4. d3.range(1,1000).map() -- compare this to numpy array manipulation
    * google: array map python
    * https://stackoverflow.com/questions/10973766/understanding-the-map-function
    * compare this with d3.range().map() -- as seen in the SVG example of "Introduction to HTML"
5. set the dimension
6. set two cross hairs that intersect the origin (no ticks or labels on the cross hairs and no axes on the edges)

#### References

* [d3-array](https://github.com/d3/d3-array) -- D3 API docs
    * Array manipulation in JavaScript (standalone library and part of D3.js)
    * [d3.range()](https://github.com/d3/d3-array#range)
* [D3.js API docs](https://github.com/d3/d3/blob/master/API.md)
    * [d3-random.js API docs](https://github.com/d3/d3-random)
* [Plotly.js reference docs](https://plot.ly/javascript/reference/) -- plot.ly
    * [javascript axes examples](https://plot.ly/javascript/axes/)

## From Observable to the Web

It's not hard, but if you haven't done it before, it can be confusing.
It requires some understanding of HTML, CSS, and JavaScript.

1. create the independent web page in a gist (only in JavaScript)
2. view the independent web page and code from bl.ocks.org
    * 863-by-525 (svg dimensions in python plot.ly)

## Web-accessible tools for graphing and data manipulation

Let's step back a second and consider the requirements/weaknesses/strengths of
various options in Python (e.g., matplotlib, Plot.ly) and Observable notebooks...

* Data analytics on the fly (array manipulations, random number generation)
* Web capable -- all three work in browsers (JavaScript and Python APIs are closely related in Plot.ly, matplotlib needs Jupyter server to work in a browser)
* Interactive (matplotlib is evolving, v3 has "events" too ([reference](https://matplotlib.org/users/event_handling.html), but only on the desktop, unless it's in a Jupyter notebook)
* Able to integrate slippy maps (matplotlib requires Jupyter (https://github.com/mapbox/mapboxgl-jupyter))
* Capable of 3D charts and graphs (all 3)
* Customizable (this turns out to be an important differentiator)

Issues (looking under the hood a little deeper)...

* Python version needs a server or desktop application (Jupyter Notebook uses the desktop as a server)
* JavaScript version does not require a server (all computations and rendering are done locally)
* Customization depends on integration with HTML5 (you can see hints of HTML5 in plot.ly)
* Observable notebooks (everything in the browser)
* Observable code needs to be migrated to other websites, or inside an organization's firewall.
    * This is actually pretty easy, as we'll see.
* BTW, R has some nice options, but we won't be using R this semester.

### Chloropleth maps

We've seen scatterplots (dots), now let's look at maps...

* https://plot.ly/python/choropleth-maps/ (Plot.ly)
* http://geopandas.org/ -- geopandas
* https://beta.observablehq.com/@mbostock/d3-choropleth -- D3.js

Looking ahead: slippy maps, and dots on maps.

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
