
# Class #2

* block -- https://bl.ocks.org/pbogden/6840da349acf3311932b8f0f3b252f5b

* code  -- https://github.com/umbcvis/classes/blob/master/class-02/index.html

* demo -- http://umbcvis.github.io/classes/class-02

## What you'll learn

* Array manipulation in JavaScript
* [JSON](http://www.json.org/)
    * [GeoJSON](http://geojson.org/)
    * [TopoJSON](https://github.com/topojson/topojson)
* Reading TopojJSON data into a D3 visualization (d3.json)
* Converting Topojson to GeoJSON
* Plotting GeoJSON point data on a map

## Background

Look at the following tutorials to familiarize yourself with JavaScript objects, functions and arrays.

* <http://www.w3schools.com/js/js_object_definition.asp> -- Objects

* <http://www.w3schools.com/js/js_function_definition.asp> -- Functions

* <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array> -- Arrays

Whenever you're ready, answer the questions below. That said, if you're feeling brave, the best way to complete the assignment is probably to look at the questions first, go as far as you can, then go back and forth between the questions and the background materials.

## Assignment

Answer the questions below. They're related to the Oklahoma earthquake demo that we looked at in class. We'll work through a similar set of questions in the next class.

Click this link to see index.html in your browser...

<http://umbcvis.github.io/classes/class-02>

After you click the link, open up the JavaScript console of your browser.  Type the word ````data```` and hit return. You should see a GeoJSON ````object```` that contains the earthquake data. You can inspect and manipulate (with JavaScript) the contents of the object in the console.  Look back at ````index.html```` to see where it comes from. You may want to refer to the [GeoJSON specification](http://geojson.org) and the [USGS API documentation](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php).

1. How many earthquakes are there in the file ````quakes.json````?  Answer: 4618

2. How many earthquakes of magnitude 2.5 or greater are there in ````quakes.json````?  Look at index.html for a hint.

        // Micro tutorial: Array as the property of an object
        var obj = { a: 3, b: [5, 11, 7, 42] };  // variable "obj" is an object with two properties: "a" and "b"
        var arr = obj.b;                        // variable "arr" is the array: [5, 11, 7, 42]
        console.log( arr );                     // print "arr" on the console

        // Micro tutorial: Filter an array (with an "anonymous" function)
        var fil = arr.filter(function(d) { return (d > 10); });   // create a new array with elements larger than 10
        console.log( fil );     // print the variable "fil", the filtered array, to the console: [11, 42]

3. What's the magnitude of the biggest earthquake in ````quakes.json````?  There are several ways to answer this question. I'll show you how to do it quickly with [D3-array](https://github.com/d3/d3-array).

4. What's the magnitude of the oldest earthquake in ````quakes.json````? Ditto regarding [D3-array](https://github.com/d3/d3-array).

5. When did the oldest earthquake in ````quakes.json```` occur?  Google and stackoverflow are your friends for this one.

6. Make your own copy of index.html. Change the URL for the earthquake data source to the real-time data feed from the USGS.  I already put a URL for the data feed in a variable called ````usgs````. That URL will give you all the earthquakes for the last week.

    1. How many earthquakes were there in the last week?

    2. How many were there in a bounding box that includes California?

    3. How many were there in Oklahoma?

# Fin
