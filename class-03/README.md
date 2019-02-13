
# Class #3

* [demo (my map)](http://localhost/~pbogden/classes/class-03/)
* [demo (earthquake heatmap)](http://localhost/~pbogden/classes/class-03/olheat.html)
* [demo (Leaflet dots on a map)](http://localhost/~pbogden/classes/class-03/leaf.html)
* [demo (OpenLayers dots on a map)](http://localhost/~pbogden/classes/class-03/test.html)

## From Observable to the Web

* We only touched on this last time (gist.github.com & bl.ocks.org)

#### The Web

* [HTML Examples](https://www.w3schools.com/html/html_examples.asp) -- W3Schools
    * [HTML Document](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_document)
    * [HTML `id` attribute](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_id_css)
    * [HTML scripts](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script)
    * [HTML canvas](https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_canvas_tut_path2)
    * [HTML SVG](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_svg_circle)
* [HTML validator](https://validator.w3.org/nu/#textarea)
    * You can omit the <html>, <head> and <body> tags, but beware.
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

## Leaflet Dots

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

Rather than locking up while the file is downloading, browsers download
asynchronously.  This complicates things.  The typical way for JavaScript to handle
asynchronous loads is with callback functions.  For example, early versions of D3.js
(before observablehq.com existed) would load USGS GeoJSON earthquakes with something like this:

        d3 = require("https://d3js.org/d3.v4.min.js");

        var url = 'https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson';

        d3.json(url, processQuakes);

        function processQuakes(err, quakes) {
          if (err) return console.log('Error loading quake data', err);

          console.log('# of quakes in the last hour:', quakes.features.length);
        }

`processQuakes` is a callback function called after the GeoJSON is loaded and parsed into the variable `quakes`.
The variable `err` is Null (so `(err)` evaluates to `false`) if the request is successful.

You can use D3.js to load data into an Observable noteboook as described in
[Introduction to data](https://beta.observablehq.com/@mbostock/introduction-to-data).
It's a little slicker with Observable because the latest version of D3.js
uses JavaScript's `Promise` and `fetch`.
The JavaScript "Promise" API makes it easier to work with asynchronous values.
"Promise"s represent values that are not yet known, but that will be known in the future.

The following line does the same thing, but without D3.js:

    quakes = (await fetch('https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson')).json()

The variable `quakes` starts out as a `Promise` and then resolves to a JavaScript
object representing the GeoJSON FeatureCollection containing all earthquakes in the last hour.
Observable implicitly "awaits" promises across cell boundaries, so you often don’t
need to deal with a promise directly. Cells can return promises, and other cells
can simply refer to the values and they’ll run when the promise resolves.

#### References:

* [Introduction to data](https://beta.observablehq.com/@mbostock/introduction-to-data)
* [Introduction to promises](https://beta.observablehq.com/@mbostock/introduction-to-promises)
* [Observable standard library](https://github.com/observablehq/stdlib/blob/master/README.md)

## Browsers evolve

Observable uses the most modern browser capabilities, such as Generators.  Often, these capabilities
won't work in older browsers. That typically means any version of IE.  But sometimes it
only the most recent version of the Chrome and Firefox.  MDN pages typically provide browser compatibility
at the bottom of the page.  Most of the things we do in this class will work in the lastest
version of IE, so we'll typically stay away from the most cutting edge capabilities.
you may encounter them along the way.  For example...

* `function*` -- declaration defines a "generator function", which returns a "Generator" object
* `Generator` -- an object that conforms to the `iterable` and `iterator` protocols
    * `Generator.prototype.next()` -- returns the value yielded by the "yield" expression
    * `Generator.prototype.return()` -- as `.next()` and also finishes generator
    * `Generator.prototype.throw()` -- throws an error to a generator (and finishes the generator, unless it's caught)
* `yield` -- used to pause/resume a generator function

#### References

* [Introduction to Generators](https://beta.observablehq.com/@mbostock/introduction-to-generators) -- Mike Bostock
* [function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) -- MDN docs
* [Generator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator) -- MDN docs
