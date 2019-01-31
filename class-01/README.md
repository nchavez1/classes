# Class #1

# Observable examples

* [Unemployment rate by county](https://beta.observablehq.com/@mbostock/d3-quantile-choropleth)
* [Obama and Romney](https://archive.nytimes.com/www.nytimes.com/interactive/2012/11/11/sunday-review/counties-moving.html)
* [Chicago killings](https://archive.nytimes.com/www.nytimes.com/interactive/2013/01/02/us/chicago-killings.html)
* [Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- slippy maps with data
    * [OpenStreetMap project](https://www.openstreetmap.org/#map=4/38.01/-95.84) (their website)
    * [OpenStreetMap description](https://www.openstreetmap.org/#map=4/38.01/-95.84) (wikipedia)
* [GeoJSON in Three.js](https://beta.observablehq.com/@mbostock/geojson-in-three-js) -- Dynamic 3-D geospatial demo
* Earthquakes
    * [Interactive time-space filter on a map](https://pbogden.com/shake/)
    * [USGS data on a rotating glove](https://beta.observablehq.com/@jashkenas/quakespotter-0-1) -- observable demo
    * [USGS data source](https://earthquake.usgs.gov/earthquakes/feed/)
    * [USGS GeoJSON feed](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php)
* The sky's the limit (not in this course, but maybe the next one)
    * [Machine learning in a browser](https://beta.observablehq.com/@mbostock/lets-try-t-sne) (image classification)
    * [Tensorflow demo](https://github.com/tensorflow/tfjs-examples/tree/master/tsne-mnist-canvas)
    * [Tensorflow project](https://www.tensorflow.org/)
* [Downloading and embedding notebooks](https://beta.observablehq.com/@jashkenas/downloading-and-embedding-notebooks)

# Github

* [Github](https://github.com/)

# Introduction to code

* Reading: [Introduction to code](https://beta.observablehq.com/@mbostock/introduction-to-code) by Mike Bostock

# Problem-solving in Python, JavaScript, etc.

"top programming languages"...

* top link on google -- JavaScript, Python, Java, C/C++, PHP, Swift, C#, Ruby
* [tiobe index](https://www.tiobe.com/tiobe-index/) -- Java, C, Python, C++, VB/.NET, JavaScript, C#
* "programming language jobs" -- Java, Python, JavaScript, C++, C#, PHP, Perl
* "programming languages data science" -- R, Python, Java, Scala, SQL, Julia

Some geospatial considerations

* Web applications
    * various languages and platform-specific implentations on the back end
    * platform-specific JavaScript on the front end (thanks to HTML5 that's built into modern browsers)
    * increasing number of data and mapping resources are available on the Web with JavaScript APIs
* geospatial applications and libraries (for analysts)
    * QGis and other desktop applications -- often with platform-specific graphics
    * R -- platform-specific scriptable application library with platform-independent (JavaScript) graphics
    * Python -- scriptable language with both platform-specific and platform-independent (JavaScript) graphics
* geospatial software (for developers who have heavy-duty number crunching requirements)
    * GDAL & OGR written in C++ (under the hood for many commercial geospatial applications)
    * Python (language) has many data-oriented libaries with Python bindings to the C++ API
    * [Plot.ly](https://plot.ly/python/) Python library with platform-independent graphics (JavaScript) on the front end

Whether you program in Python, Java, JavaScript or some other language, google is your friend. 
In the old days: you either remembered syntax, looked in a language reference book, or asked a colleague.
Today: it's still good to remember syntax, but the real skill is knowing how to quickly "find" the answer.
And the key to finding the answer is knowing how to phrase the question for google and filter the results.

* If you search for "python array"
    * Top link -- W3Schools
    * First page -- Stackoverflow
* If you search for "JavaScript array"
    * Top link -- W3Schools
    * First page -- MDN (Mozilla Development Network)
* If you search for "remove an element from an list python"
    * Top link -- quote from Quora.com
    * Second link -- a list of stackoverflow links
        * "how to remove a specific element from an array using python"
        * question: 95 votes
        * answer: 134 votes
        * views: 319K
    * You learn that in Python, an array is a "list"
* If you search for "remove an element from a list python"
    * Top link -- quote from stackoverflow.com
    * Second link -- a list of stackoverflow links
        * "how to remove a specific element from an array using python"
        * question: 95 votes
        * answer: 134 votes
        * views: 319K
    * You learn that in Python, an array is a "list"
* If you search for "remove an element from a list python"
    * Top link -- quote from stackoverflow.com
    * Second link -- a list of stackoverflow links

* If you search for "remove an element from an list javascript"



### Observable references

* [How saving works](https://beta.observablehq.com/@mbostock/how-saving-works)

### Other references

* [Mike Bostock](https://bost.ocks.org/mike/) (Creator of D3)
* [Breakout](https://developer.mozilla.org/en-US/docs/Games/Tutorials/2D_Breakout_game_pure_JavaScript) (in JavaScript)
* [Introduction to data](https://beta.observablehq.com/@mbostock/introduction-to-data)


* If you search for "remove an element from an list javascript"



### Observable references

* [How saving works](https://beta.observablehq.com/@mbostock/how-saving-works)

### Other references

* [Mike Bostock](https://bost.ocks.org/mike/) (Creator of D3)
* [Breakout](https://developer.mozilla.org/en-US/docs/Games/Tutorials/2D_Breakout_game_pure_JavaScript) (in JavaScript)
* [Introduction to data](https://beta.observablehq.com/@mbostock/introduction-to-data)

# GIS and the Web

 * Desktop GIS
    * Analysts (Esri, QGIS) -- raster (geotiff), vector (shapefile)
    * Software engineers (C, C++, SQL) -- GDAL, OGR
    * Scientists (Matlab, Fortran) -- matrix, vector
* Web (yesterday)
    * Analysts (MSWord/Google docs, Excel/Tableau) -- images (PNG, GIF), xlsx
    * Graphic artists (Photoshop, Illustrator)  -- images, SVG
    * Web designers (HTML, CSS) -- images (PNG, GIF), SVG
    * Web developers (JavaScript, HTML5) - canvas, XML
    * Scientists (Python/Matplotlib, R) -- images, data
* Web (today)
    * Data journalists (D3, HTML5) -- canvas/WebGL, SVG
    * Data scientists (Python/Plotly, R/Shiny) -- images, data
    * Scientists -- data/metadata, data/metadata

# Common data formats

* Downloads -- shapefiles, xlsx, geotiff
* Mapping apps (google maps, mapbox, leaflet) -- PNG, GIF (raster)
* Data APIs -- CSV, JSON, GeoJSON (vector)

# Visualization & presentation

* Browsers -- taking over the world of data visualization
    * The developer console...
    * Interactive Web apps can do many of the things that use to require desktop applications
    * Thanks to open standards: HTML5, JSON and GPUs
* Code vs Desktop application
    * Python, R, JavaScript, etc.
    * ArcGIS, QGIS, etc.
* Data manipulation, analysis
    * Python -- list, dict
    * R -- vector, list
    * JavaScript -- array, object

# Services

* github -- software repository with version control -- create an account
* bl.ocks.org -- automatically displays the code you put in a github "gist"
* observablehq.com -- a better way to code -- login with your github account

# Problem solving 

* google.com -- ask your question here
* stackoverflow.com -- technical questions answered (and rated)
* developer.mozilla.org -- web docs
* w3schools.com -- basic web docs

# Graphics packages/libraries

* plot.ly -- a Python/R/JavaScript plotting package
* Dash -- a Python framework for building web applications that Plot.ly
* Shiny -- an R framework for creating visualization and interactive Web apps (Node.js, Bootstrap, D3.js)
* D3.js -- the powerful JavaScript library for Web-based graphics that's under the hood of all the others

# Demo

Make this work on observablehq

* https://plot.ly/python/line-and-scatter/
* convert the python to javascript

1. Add plot.ly library

        Plotly = require("https://cdn.plot.ly/plotly-latest.min.js")

2. Copy and paste the JavaScript demo: https://plot.ly/javascript/line-and-scatter/

    * Error #1 -- pointing to `var` in the first line.

            SyntaxError: Unexpected token

3. Solution: Add curly brackets to the entire "block" of code

    * Error #2 -- pointing to `Plotly.newPlot('myDiv', data);`

            Error: No DOM element with id 'myDiv' exists on the page.

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



