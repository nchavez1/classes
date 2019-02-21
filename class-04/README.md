
# Class #4

## The purpose of visualization

Mike Bostock "builds tools for for visualizing information", and Observable is his latest creation.
But he cautions that the tool should not be the goal.
Rather, the goal should be visualizing information.
Moreover, in [A Better Way to Code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0),
he provides the following quote from Ben Shneiderman:

> The purpose of visualization is insight, not pictures.

Now that we've gotten a feel for Observable, we'll focus on visualizations that provide insight.

#### Optional reading:

* [A better way to code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0) -- Mike Bostock

## Class #3 assignments

Observable quakes on leaflet: https://beta.observablehq.com/@pbogden/earthquakes-on-leaflet/

The insights from this assignment emerge when we explain what we observe.

## Observable visualization

There are quite a few reasons to use Observable for visualization.
One reason is that Observable "minimizes the specialized knowledge you need to be
productive" ([Ref](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0)).
And as a "web-first" environment that runs in any browser, your notebook
for data exploration "can gracefully transition into code for
explanation." Equally important, it's interactive.

> Interactive programming improves our ability to scrutinize behavior by poking:
> changing, deleting, reordering code, and seeing what happens.

In other words, Observable is a "reactive" programming environment.

## Reactive programming

We're used to "imperative" programming in scripting languages like Python
and JavaScript (R works that way too).
Imperative programming uses variable "assignment", which introduces the need to be careful
about [state](https://en.wikipedia.org/wiki/State_(computer_science)) because operations are sequential.
For example:

    var x, i;     // x = y = undefined
    x = 0;        // x = 0, i = undefined;
    i = 1;        // x = 0, i = 1;
    x = 2 * i;    // x = 2, i = 1;
    (x == 2 * i)  // true
    ++i           // x = 2, i = 2;
    (x == 2 * i)  // false

Instead of variable assignment, reactive programming uses variable definition.
In observable, this mean that if we define one cell with the line `x = 2 * i`,
(x == 2 * i) is always true, regardless of the value of `i`.
You may not think you've done reactive programming before,
but spreadsheets work this way. Time for a demo so we can explore some of the implications.  

1. Open a new Observable notebook and create a cell with the following line:

        x = 2 * i;

    If you run the cell, you get a runtime error because `i` is not defined.

2. Create another cell with this line:

        i = 1;

    Then "run" the cell and observe the value of `x`. Change the value of `i` and observe what happens with `x`.
    This behavior should be familiar from previous classes, but let's go one step further.

3. Replace the previous cell with the following expression for `i`:

        i = {
              let i = 0;
              while (true) {
                yield ++i;
              }
            }

    This cell is a `generator`, and it "yields" a value for `i` up to 60 times/second.
    Although you may not have seen it before, the `yield` keyword exists in
    JavaScript and Python.  It is used to pause and
    resume a `generator function`, which also exist in both JavaScript and Python.
    (Note: IE does not support `yield`.)

    Q: What happens if you replace "yield" with "return"? Try it.

4. Try replacing `true` with `i < 100` in the previous expression for `i` (the one that uses `yield`)

    Q: What would happen if you tried to do everything sequentially
    by first creating the values all the values of `i` in an Array, and then
    returning the Array so could be processed in another cell?

5. Iterators and generators exist in JavaScript and Python. They're used to iterate over each item in a collection. You've used iterators when you've used a JavaScript `Array` (Python `list`).

        result = {
            let i = 0;
            let a = [];
            while (i < 100) {
                a.push(++i);
            }
            return a;
        }

    This cell creates an `Array` that saves every value of `i` and returns the Array of 100 values as `result`.

   Q: What would happen if you replaced `i < 100` with `true` now?  Think about it first. If you actually try it, you might be sorry.

#### Reading:
* [Five-minute introduction](https://beta.observablehq.com/@mbostock/five-minute-introduction)
At the bottom, you'll see a "brushable" scatterplot created with D3.
This "brush" behavior is built into the scatterplots we've used in Plot.ly

#### References:
* [Iterators and generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators) -- MDN docs
* [Generator functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators#Generator_functions) -- MDN docs
* [function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) -- MDN docs

## Generators

    (Repeated from last class): Observable uses some of the most modern browser capabilities,
    such as Promises and Generators.  Generators enable communication between Observable cells,
    allowing shared values to be updated dynamically.
    The central JavaScript elements, which you'll see from time to time, include:

    * `function*` -- declaration defines a "generator function", which returns a "Generator" object
    * `Generator` -- an object that conforms to the `iterable` and `iterator` protocols
        * `Generator.prototype.next()` -- returns the value yielded by the "yield" expression
        * `Generator.prototype.return()` -- as `.next()` and also finishes generator
        * `Generator.prototype.throw()` -- throws an error to a generator (and finishes the generator, unless the error is caught)
    * `yield` -- used to pause/resume a generator function

    Older browsers (e.g., IE) don't know about Generators, or Promises, or
    many of the other cool things built into Observable.
    If you want your Observable notebooks to run in older browsers, you'll need to do some extra work.
    MDN typically provides browser compatibility at the bottom of each page in the reference docs.

## Active reading

In [A better way to code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0), Mike Bostock
explains how Observable helps to promote "active reading," which is a concept described by Brett Victor
in [Explorable Explanations](http://worrydream.com/ExplorableExplanations/).

> An active reader asks questions, considers alternatives, questions assumptions,
> and even questions the trustworthiness of the author.
> An active reader tries to generalize specific examples, and devise specific examples
> for generalities. An active reader doesn’t passively sponge up information,
> but uses the author’s argument as a springboard for critical thought and deep understanding.

In the next demo, we'll start using interaction controls to create
a visualization that promotes active reading.

## Interactive controls for the reader

Observable quakes on leaflet: https://beta.observablehq.com/@pbogden/earthquakes-on-leaflet/

* TODO: Introduce a slider to solve the homework assignment for Class #3
    * Use this to develop some insights about the data
    * Overall pattern -- plate tectonics
    * Space vs magnitude -- western/eastern hemisphere (as per homework assignment)
    * Space vs time -- Oklahoma

1. `map.eachLayer(function(layer) { });`
    * Show how to access the feature in each layer


#### References

* Leaflet docs
    * https://leafletjs.com/reference-1.4.0.html#map-eachlayer)
* [Loops and iteration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration) -- MDN Docs
* [L.geoJSON](https://leafletjs.com/reference-1.4.0.html#geojson) -- leaflet docs
     * [L.geoJSON style](https://leafletjs.com/reference-1.4.0.html#geojson-style)

## Earthquake Heatmap

* Consider the caveat about heatmaps in [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet)
* TODO: Adapt earthquakes dots on Leaflet to create a heatmap
* Look at the data-processing step in [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet)
* Look at the metro pattern

#### References

* [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- Tom MacWright
    * Shows how to do heatmap for DC crime that has been curated by Esri
* [Leaflet.heat](https://github.com/Leaflet/Leaflet.heat) -- Leaflet Heatmap Plugin
* [D3 + Leaflet](https://bost.ocks.org/mike/leaflet/) -- Mike Bostock (2012)
    * Uses Leaflet v0.7 (vector overlay disappears temporarily on zoom)
* [Interactive Choropleth map](https://leafletjs.com/examples/choropleth/) -- Leaflet docs
    * Uses Leaflet v1.4 (huge improvement, compare with v0.7 D3 + Leaflet)
    * Shows how to interact with features -- nice!
    * Does **not** show how to add/remove layers.
    * Does show how to change feature style interactively using mouseover event
        * Uses layer.setStyle
        * Uses geojson.resetStyle
        * Uses event.target to get the moused feature
    * Figure out how to set fillOpacity 0 for features based on their magnitude
        * This should probably set the style function
* [Leaflet tutorials](https://leafletjs.com/examples.html) -- Leaflet docs
    * [Using GeoJSON with Leaflet](https://leafletjs.com/examples/geojson/)
    * [Leaflet extension methods](https://leafletjs.com/examples/extending/extending-2-layers.html)
    * [Working with map panes](https://leafletjs.com/examples/map-panes/)
    * [Zoom levels](https://leafletjs.com/examples/zoom-levels/)
* [Interact with marker layer](https://stackoverflow.com/questions/13004226/how-to-interact-with-leaflet-marker-layer-from-outside-the-map) -- stackoverflow (2016)
* [Assign id to marker in Leaflet](https://stackoverflow.com/questions/25683871/assign-id-to-marker-in-leaflet) -- stackoverflow (2015)
* [L.stamp recommendation](https://github.com/Leaflet/Leaflet/issues/1805#issuecomment-257128259) -- github (2016)

* [Introduction to Data](https://beta.observablehq.com/@mbostock/introduction-to-data) -- Mike Bostock
* [Introduction to Promises](https://beta.observablehq.com/@mbostock/introduction-to-promises) -- Mike Bostock
* [Observable standard library](https://github.com/observablehq/stdlib/blob/master/README.md)

#### References

* [Introduction to Generators](https://beta.observablehq.com/@mbostock/introduction-to-generators) -- Mike Bostock
* [function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) -- MDN docs
* [Generator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator) -- MDN docs

## Choropleth maps

* [D3 Choropleth](https://beta.observablehq.com/@mbostock/d3-choropleth) -- Mike Bostock
* [Interactive Choropleth demo](https://leafletjs.com/examples/choropleth/) -- Leaflet docs
* [Plot.ly Choropleth demo](https://plot.ly/python/choropleth-maps/)

## Project ideas

* Update [Suzee Parson's project](https://bl.ocks.org/jsparsons2/44ad737738896f8438c6)
    * Augment with Census data
    * This will require work with the HMDA API
* Investigate patterns in heatmap of crime: https://beta.observablehq.com/@tmcw/leaflet
    * Is there a better way to visualize the data distribution?
    * Consider alternate data sources
    * [Metro locations as JSON](https://developer.wmata.com/docs/services/5476364f031f590f38092507/operations/5476364f031f5909e4fe3311)

## Class #4 Assignment

* Investigate alternative visualizations of the crime data that mitigate stated concerns about heatmaps
