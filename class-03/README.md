
# Class #3

* [demo (my map)](http://localhost/~pbogden/classes/class-03/)
* [demo (earthquake heatmap)](http://localhost/~pbogden/classes/class-03/olheat.html)

## From Observable to the Web

* We only touched on this last time (gist.github.com & bl.ocks.org)

#### The Web

* [HTML Examples](https://www.w3schools.com/html/html_examples.asp) -- W3Schools
    * [HTML Document](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic_document)
    * [HTML `id` attribute](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_id_css)
    * [HTML scripts](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_script)
    * [HTML canvas](https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_canvas_tut_path2)
    * [HTML SVG](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_svg_circle)

Compare the SVG (vector) and canvas (raster) examples. Add the following to the canvas demo...

    ctx.fillStyle='yellow'
    ctx.fill();
    ctx.strokeStyle="green";
    ctx.lineWidth=4;

Serving a web page

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

* [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- Observable notebook by Tom MacWright
    * Nice introduction to Leaflet in Observable
    * Shows how to add a polygon to Leaflet (vector data)
    * Shows how to add a heatmap to Leaflet
* [Using OpenLayers](https://beta.observablehq.com/@tmcw/using-openlayers)
    * [Hello, OpenLayers!](https://beta.observablehq.com/@mbostock/hello-openlayers)
    * [Hello, OpenLayers Select!](https://beta.observablehq.com/@mbostock/hello-openlayers-select)
    * [Hello, OpenLayers Box Selection!](https://beta.observablehq.com/@mbostock/hello-openlayers-box-selection)
* [Leaflet](https://leafletjs.com/)
    * [Leaflet | Mapbox](https://docs.mapbox.com/help/glossary/leaflet/)
* [OpenLayers](https://openlayers.org/)
    * [Download](https://openlayers.org/download/) -- several ways of getting the code
    * [earthquake heatmap](https://openlayers.org/en/v4.6.5/examples/heatmap-earthquakes.html) -- official example
    * [D3 and stamen](https://openlayers.org/en/latest/examples/d3.html) -- official example
    * [ol/layer/Heatmap](https://openlayers.org/en/v5.3.0/apidoc/module-ol_layer_Heatmap.html) -- API docs for v5.3.0
