
# Class #3

* [OpenLayers demo (my map)](http://localhost/~pbogden/classes/class-03/)
    * Reference: https://openlayers.org/en/latest/doc/quickstart.html
* [Earthquake heatmap demo](http://localhost/~pbogden/classes/class-03/olheat.html) -- OpenLayers
* [Observble earthquakes a map with Leaflet)](https://beta.observablehq.com/d/3d0228a3b6eec481) -- PB
    * [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- Tom MacWright

## Quick intro to HTML5

* Last time we only touched on serving a web page from gist.github.com & bl.ocks.org.

#### 

* [HTML Examples](https://www.w3schools.com/html/html_examples.asp) -- W3Schools
    * [HTML Document](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_document)
    * [HTML `id` attribute](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_id_css)
    * [HTML scripts](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script)
    * [HTML canvas](https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_canvas_tut_path2)
    * [HTML SVG](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_svg_circle)
* [HTML validator](https://validator.w3.org/nu/#textarea)
    * You can omit the `<html>`, `<head>` and `<body>` tags, but beware.
* [HTML5 Boilerplate](https://html5boilerplate.com/)
    * An authoritative resource for best practices -- way beyond the scope of this course.

Compare the SVG (vector) and canvas (raster) examples. Add the following to the canvas demo...

    ctx.fillStyle='yellow'
    ctx.fill();
    ctx.strokeStyle="green";
    ctx.lineWidth=4;

#### HTML Bar Chart

* [Let's make a bar chart](https://bost.ocks.org/mike/bar/)
    * [Coding the chart manually](https://bost.ocks.org/mike/bar/#manual)

#### Serving a web page

* Demonstrate how to get homework assignments into a gist and served from bl.ocks.org

#### References:

* [HTML examples](https://www.w3schools.com/html/html_examples.asp) -- W3schools
    * [Basic document](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_document)
* [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started) -- MDN
    * [The head metadata in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
    * [Example page with CSS and JavaScript](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#Active_learning_applying_CSS_and_JavaScript_to_a_page)
* [Downloading and Embedding Notebooks](https://beta.observablehq.com/@jashkenas/downloading-and-embedding-notebooks) -- Observable
    * [Standard Library](https://beta.observablehq.com/@mbostock/standard-library)

#### Advanced references:

* [Observable standard library](https://github.com/observablehq/stdlib)
* [Observable runtime]((https://github.com/observablehq/runtime)

## Chloropleth maps

* Compare Plotly and D3.js examples

## Earthquakes

The data source for OpenLayers earthquake example

    <?xml version="1.0" encoding="UTF-8"?>
    <kml xmlns="http://earth.google.com/kml/2.0" xmlns:atom="http://www.w3.org/2005/Atom">
        <Document>
            <name>2012 Earthquakes, Magnitude 5</name>
            <atom:author>
                <atom:name>U.S. Geological Survey</atom:name>
            </atom:author>
            <atom:link href="http://earthquake.usgs.gov"/>
            <Folder>
                <name>Magnitude 5</name>
                <Placemark id="2012 Jan 15 13:40:16.40 UTC">
                    <name>M 5.9 - 2012 Jan 15, SOUTH SHETLAND ISLANDS</name>
                    <magnitude>5.9</magnitude>
                    <Point>
                        <coordinates>-56.072,-60.975,0</coordinates>
                    </Point>
                </Placemark>
                <Placemark id="2012 Jan 19 06:48:48.75 UTC">
                    <name>M 5.9 - 2012 Jan 19, OFF W. COAST OF S. ISLAND, N.Z.</name>
                    <magnitude>5.9</magnitude>
                    <Point>
                        <coordinates>165.778,-46.686,0</coordinates>
                    </Point>
                </Placemark>
                etc...

#### TODO

* Compare with GeoJSON feed.
* Show how to manipulate the feature vector
* Show how to filter
* Do it dynamically

Reference: [GeoJSON spec](http://geojson.org/)

## Slippy maps

* [Leaflet](https://leafletjs.com/)
    * [Leaflet examples](https://leafletjs.com/examples.html)
    * [Using GeoJSON with Leaflet](https://leafletjs.com/examples/geojson/)
    * [Leaflet API reference](https://leafletjs.com/reference-1.4.0.html)
    * [Leaflet | Mapbox](https://docs.mapbox.com/help/glossary/leaflet/)
* [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- Tom MacWright
    * Nice introduction to Leaflet in Observable
    * Shows how to add a polygon to Leaflet (vector data)
    * Shows how to add a heatmap to Leaflet
* [Using OpenLayers](https://beta.observablehq.com/@tmcw/using-openlayers) -- Tom MacWright
    * [Hello, OpenLayers!](https://beta.observablehq.com/@mbostock/hello-openlayers) -- Mike Bostock
    * [Hello, OpenLayers Select!](https://beta.observablehq.com/@mbostock/hello-openlayers-select) -- Mike Bostock
    * [Hello, OpenLayers Box Selection!](https://beta.observablehq.com/@mbostock/hello-openlayers-box-selection) -- Mike Bostock
* [OpenLayers](https://openlayers.org/)
    * [Download](https://openlayers.org/download/) -- several ways of getting the code
    * [earthquake heatmap](https://openlayers.org/en/v4.6.5/examples/heatmap-earthquakes.html) -- official example
    * [D3 and stamen](https://openlayers.org/en/latest/examples/d3.html) -- official example
    * [ol/layer/Heatmap](https://openlayers.org/en/v5.3.0/apidoc/module-ol_layer_Heatmap.html) -- API docs for v5.3.0
    * [contains](https://openlayers.org/en/latest/apidoc/module-ol_format_filter_Contains-Contains.html)
* [D3.js API]
    * [d3.geoContains()](https://github.com/d3/d3-geo/blob/master/README.md#geoContains)
    * [d3.polygonContains()](https://github.com/d3/d3-geo/blob/master/README.md#geoContains)
* [Using GeoJSON with Leaflet](https://leafletjs.com/examples/geojson/) -- Leaflet docs
    * [map.getBounds()](https://leafletjs.com/reference-1.4.0.html#map-getbounds)

## Leaflet dots

    var map = L.map("map");
    L.tileLayer("http://{s}.tile.osm.org/{z}/{x}/{y}.png").addTo(map);

    map.setView([48.85, 2.35], 8);

    var myRenderer = L.canvas({ padding: 0.5 });

    for (var i = 0; i < 100000; i += 1) { // 100k points
          L.circleMarker(getRandomLatLng(), {
      	  renderer: myRenderer
      }).addTo(map).bindPopup('marker ' + i);
    }

    function getRandomLatLng() {
	return [
  	-90 + 180 * Math.random(),
        -180 + 360 * Math.random()
      ];
    }

## Browsers are asynchronous

Browsers do lots of things asynchronously.
Otherwise, they'd freeze during things like file downloads.
Working asynchronously complicates things, especially when we're loading remote data sources.
The typical (soon to be old-fashioned) way for JavaScript to handle
asynchronous loads is with callback functions.  For example, early versions of D3
(before observablehq.com existed) would load the USGS GeoJSON earthquake feed with something like this:

        var url = 'https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson';

        d3.json(url, processQuakes);

        function processQuakes(err, quakes) {
          if (err) return console.log('Error loading quake data', err);

          console.log('# of quakes in the last hour:', quakes.features.length);
        }

In this example, `processQuakes` is a callback function. It gets called after the GeoJSON is 
loaded and parsed into the `quakes` argument.
If everything worked okay, the variable `err` is Null (so `(err)` evaluates to `false`). 
Otherwise, "err" is an object that indicates the error, in which case `(err)` evaluates to 
true and the function returns early.

You can get this code to work in an Observable notebook, but it's not straightforward if 
you're using lots of cells.
Instead, the slick (modern) way to load data with D3 is described in 
[Introduction to data](https://beta.observablehq.com/@mbostock/introduction-to-data).
It's slick because the latest version of D3.js
uses JavaScript's relatively new `Promise` and `fetch` capabilities.
The JavaScript "Promise" API makes it easier to work with asynchronous values.
"Promise"s represent values that are not yet known, but that will be known in the future.

If you're loading JSON, then you don't even need D3. 
The following line does the same thing with JavaScript's built-in JSON parser.

    quakes = (await fetch('https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson')).json()

The variable `quakes` starts out as a `Promise` and then resolves to a JavaScript
object representing the GeoJSON FeatureCollection containing all earthquakes in the last hour.
Observable implicitly "awaits" promises across cell boundaries, so you often don’t
need to deal with a promise directly. Cells can return promises, and other cells
can simply refer to the values and they’ll run when the promise resolves.

#### References:

* [Introduction to Data](https://beta.observablehq.com/@mbostock/introduction-to-data) -- Mike Bostock
* [Introduction to Promises](https://beta.observablehq.com/@mbostock/introduction-to-promises) -- Mike Bostock
* [Observable standard library](https://github.com/observablehq/stdlib/blob/master/README.md)

## Browsers evolve

Observable uses the most modern browser capabilities, such as Promises and Generators.  
Generators are the things that allow Observable cells to communicate and update their shared values dynamically. 
The key JavaScript elements, which you'll see from time to time, include:

* `function*` -- declaration defines a "generator function", which returns a "Generator" object
* `Generator` -- an object that conforms to the `iterable` and `iterator` protocols
    * `Generator.prototype.next()` -- returns the value yielded by the "yield" expression
    * `Generator.prototype.return()` -- as `.next()` and also finishes generator
    * `Generator.prototype.throw()` -- throws an error to a generator (and finishes the generator, unless it's caught)
* `yield` -- used to pause/resume a generator function

Older browsers (e.g., IE) don't know about Generators, or Promises, or 
many of the other cool things built into Observable.
If you want your Observable notebooks to run in older browsers, you'll need to do some extra work.
MDN pages typically provide browser compatibility at the bottom of the page.

#### References

* [Introduction to Generators](https://beta.observablehq.com/@mbostock/introduction-to-generators) -- Mike Bostock
* [function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) -- MDN docs
* [Generator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator) -- MDN docs
