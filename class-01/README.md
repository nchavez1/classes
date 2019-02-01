# Class #1

Our goal for the course: visualize and present geospatial and environmental data using the modern, data-rich Web. 

## Examples

Browse these examples to get an idea of what can be done with modern Web technologies.

* Data Journalism -- maps that tell a story
    * [Unemployment rate by county](https://beta.observablehq.com/@mbostock/d3-quantile-choropleth)
    * [Obama and Romney](https://archive.nytimes.com/www.nytimes.com/interactive/2012/11/11/sunday-review/counties-moving.html)
    * [Chicago killings](https://archive.nytimes.com/www.nytimes.com/interactive/2013/01/02/us/chicago-killings.html)
* Slippy maps
    * [Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- slippy maps with data
    * [OpenStreetMap project](https://www.openstreetmap.org/#map=4/38.01/-95.84) (their website)
    * [OpenStreetMap description](https://www.openstreetmap.org/#map=4/38.01/-95.84) (wikipedia)
* 3D dynamic maps
    * [GeoJSON in Three.js](https://beta.observablehq.com/@mbostock/geojson-in-three-js) -- Dynamic 3-D geospatial demo
* Maps that use real-time data
    * [USGS data on a rotating glove](https://beta.observablehq.com/@jashkenas/quakespotter-0-1) -- observable demo
    * [USGS data source](https://earthquake.usgs.gov/earthquakes/feed/)
    * [USGS GeoJSON feed](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php)
* Machine learning with raster data (we won't cover it in this course, but it can be done)
    * [Machine learning in a browser](https://beta.observablehq.com/@mbostock/lets-try-t-sne) (image classification)
    * [Tensorflow demo](https://github.com/tensorflow/tfjs-examples/tree/master/tsne-mnist-canvas)
    * [Tensorflow project](https://www.tensorflow.org/)

## Some history

GIS and the Web have been evolving toward each other...

 * Desktop
    * Desktop applications have a history of geospatial analysis and visualization extending back decades
    * Analysts (Esri, QGIS) -- raster (geotiff), vector (shapefile)
    * Software engineers (C, C++, SQL) -- GDAL, OGR
    * Scientists (Matlab, Fortran) -- matrix, vector
* Early Web
    * Since the 90's, HTML and browsers have linked images and content created by a wide range of specialists using a comparablly wide range of tools and data formats
    * Analysts/Journalists (MSWord/Excel) -- text, images (PNG, GIF), xlsx
    * Graphic artists (Photoshop, Illustrator) -- raw data formats, images (PNG, JPEG), vector (SVG)
    * Web designers (HTML, CSS) -- images (PNG, GIF), SVG
    * Web developers (limited JavaScript) - HTML, CSS, images, XML
    * Scientists and engineers (Python, R, Matlab, Esri, QGIS, etc.) -- images and data of all kinds
* Modern data-rich Web -- In the last decade...
    * HTML5 and Web standards have brought analysis and visualization to the browser.
    * Browsers have become ubiquitous and standarized across desktops and mobile devices.
    * Open source software has become a driver for innovation and business 
    * Two data disciplines have become umbrellas for what used to be a wide range of specialties:
        * Data visualization (journalism and communications) -- (JavaScript, D3) -- canvas, SVG, WebGL
        * Data science (all kind of science and analysis) -- (Python, R) -- raster (PNG, GeoTIFF, GIF), vector and metadata (JSON, GeoJSON)
    * Two programming languages/environments have become dominant: Python & R
    * JavaScript has entered the competition.
        * Python and R run only on the desktop or on servers. They cannot run in browsers (yet?).
        * JavaScript is the language of the browser and the Web, and is migrating to desktops and servers (Node.js)
        * JavaScript connects Python and R to the browser (via extensions and frameworks such as Plot.ly, Shiny)
    * As of 2019, each one has strengths and weaknesses. We'll learn about their weaknesses and exploit their strenghs, and use the best available tools to achieve our goal.

## In this class, we'll code

We'll create dynamic, interactive, Web-based visualizations that work in all modern browsers. 
We'll learn from examples that range from standard charts and grqphs to stunning, data-rich works of art.
And we'll use cutting-edge tools for on-line collaboration and problem solving.
We need to code, because that's the only way to take advantage of the APIs, software libraries 
and tools that power the modern, data-rich Web. 

We'll use JavaScript. That's the only language that runs in a browser. But there's 
no expectation that you already know JavaScript, or any other Web technology such as HTML or CSS.
You will learn some of that along the way, but just enough to achieve our goal.

The expectation is that you know some Python. If you know another scriptable 
language/environment such as R or Matlab, you should be okay. And if you know how to code in a powerful, 
low-level, compiled language such as C or C++, then you'll be fine.  

We'll make an effort to show how JavaScript and Python relate and interact. Each language has its strengths. 
We'll highlight their similarities, and de-emphasize their differences as much as possible. You don't 
have to choose one over the other. It's possible (and advantageous) to have both in your toolbelt.

* Optional reading: [A better way to code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0) by Mike Bostock

## Common data formats

* Download (for desktop applications) -- shapefiles, xlsx, geotiff
* Web mapping (google maps, mapbox, leaflet) -- PNG
* Data APIs -- CSV, JSON, GeoJSON (vector)

## Problem-solving in Python and JavaScript

Whether you program in Python, Java, JavaScript or some other language, google is your friend.
In the old days: if you wanted to do something, you would look in in a book or ask a colleague.
Today: the skill lies in knowing how to "ask a question" in a search engine, and quickly find the best answer.

For JavaScript questions, you shouldn't need to go beyond the 3 top resources...

* w3schools -- https://www.w3schools.com/
* https://stackoverflow.com/
* MDN -- https://developer.mozilla.org/

Know how to use the ranking of the results. For example, all languages have arrays, but they refer to
them differently, which impacts the results of the search.

* If you search for "python array"
    * Top link -- W3Schools
    * Fourth link -- https://docs.python.org (arrays are a python module, not a fundamental data structure)
    * MDN and stackoverflow don't show up on the first page
    * You quickly realize that Python arrays are called "lists"
* If you search for "python list"
    * Top link -- W3Schools
    * Second link -- python documentation (https://docs.python.org)
    * MDN and stackoverflow still don't show up on the first page
* If you search for "javascript array"
    * Top link -- W3Schools
    * Second link -- MDN (Mozilla Development Network)
    * MDN is authoritative documentation for JavaScript

For problem solving, stackoverflow becomes critically important...

* If you search for "remove an element from a python array"
    * Top item -- reworded request from python documentation: "how to remove an element from a list in Python"
    * Second item -- a list of stackoverflow links. Look at the ratings before you look at the answer
        * "how to remove a specific element from an array using python"
        * question: 95 votes
        * answer: 134 votes
        * views: 319K
    * Hmmmm. Then you remember that an array in Python is called a "list", so you try again...
* If you search for "remove an element from a python list"
    * Top item -- quote from a stackoverflow link
    * Second item -- a list of stackoverflow links, each with much higher ratings
        * first stackoverflow link: "Difference between del, remove and pop on lists"
        * question: 551 votes
        * answer: 783 votes
        * views: 913K
    * These are much more likely to provide a good answer to your question
* If you search for "remove an element from a javascript list"
    * Top link -- quote from stackoverflow.com
    * Second link -- a list of stackoverflow links
* If you search for "remove an element from a javascript list"
    * Top link -- stackoverflow.com: "How do I remove a particular element from an array in JavaScript?"
    * question: 6764 votes
    * answer: 9751 votes
    * views: 5+ million
    * With rankings this high, you'll have a nice and concise answer with example(s)

# Tools

* github -- software repository with version control -- create an account
* bl.ocks.org -- automatically displays the visualization and code in a github "gist" (we'll use it later in the course)
* observablehq.com -- a better way to code -- login with your github account

# Graphics packages/libraries

* plot.ly -- a Python/R/JavaScript plotting package
* dash -- a Python framework for building web applications that Plot.ly
* shiny -- an R framework for creating visualization and interactive Web apps (Node.js, Bootstrap, D3.js)
* D3.js -- the powerful JavaScript library for Web-based graphics that's under the hood of all the others

# Reading

* [Introduction to code](https://beta.observablehq.com/@mbostock/introduction-to-code) by Mike Bostock
* [Introduction to data](https://beta.observablehq.com/@mbostock/introduction-to-data)

# Demo #1

Make this following plot.ly plot work on observablehq

* https://plot.ly/javascript/line-and-scatter/
* convert the python to javascript

1. Copy and paste the JavaScript for the demo: https://plot.ly/javascript/line-and-scatter/ into a cell in "observable.com" and "run" the code by pressing the right arrow at the top right of the cell.

    * Error #1 points to `var` in the first line.

            SyntaxError: Unexpected token

    Issue: In observable, blocks of code should be enclosed by curly braces { and }. ([Reference](https://beta.observablehq.com/@mbostock/introduction-to-code))

2. Solution: Add a curly brace { at the beginning, and another } at the end, then run the code.

    * Error: RuntimeError: Plotly is not defined

    Issue: You need to tell observable how to find the plot.ly library.

3. Solution: create a new cell with the following line of code, then run your code again:

        Plotly = require("https://cdn.plot.ly/plotly-latest.min.js")

    * Error: DOM element with id 'myDiv' exists on the page.

    Issue: `Plotly.newPlot('myDiv', data);` is trying to put the chart in an HTML `<div>` element called "mydiv". If you to back to this page (https://plot.ly/javascript/line-and-scatter/) and look in the "HTML" section, you'll see how it should look"

4. Solution: Add one line right before the line in question, and change `'myDiv' to `div`.

             const div = DOM.element('div');
             div.width = width;
             div.height = 450 * width / height;
             Plotly.newPlot(div, data);

    Now run the code.

    * [Plot.ly default width/height (700px/450px)](https://plot.ly/javascript/reference/#layout-width) -- plot.ly docs

5. Solution #2 to Error #2:

    Create a new HTML "block"

            html`<div id='myDiv'></div>`

    And, instead of the previous solution
