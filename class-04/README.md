
# Class #4

## The purpose of visualization

Mike Bostock "builds tools for for visualizing information", and Observable is his latest creation.
But he cautions that the tool should not be the goal.
Rather, the goal should be visualizing information.
In [A Better Way to Code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0),
he goes one step further and quotes Ben Shneiderman:

> The purpose of visualization is insight, not pictures.

#### Reading:

* [A better way to code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0) -- Mike Bostock

## Class #3 assignments

Observable quakes on leaflet: https://beta.observablehq.com/@pbogden/earthquakes-on-leaflet/

## Active reading

In [A better way to code](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0), Mike Bostock
explains how Observable helps to promote "active reading," which is a concept described by Brett Victor
in [Explorable Explanations](http://worrydream.com/ExplorableExplanations/).

> An active reader asks questions, considers alternatives, questions assumptions,
> and even questions the trustworthiness of the author.
> An active reader tries to generalize specific examples, and devise specific examples
> for generalities. An active reader doesn’t passively sponge up information,
> but uses the author’s argument as a springboard for critical thought and deep understanding.

In the next demo, we'll use interaction elements to create a visualization that promotes active reading.

## Using Observable for visualization

There are quite a few reasons to use Observable for visualization.
One reason is that Observable "minimizes the specialized knowledge you need to be
productive" ([Ref](https://medium.com/@mbostock/a-better-way-to-code-2b1d2876a3a0)).
It is also a "web-first" environment that runs in any browser
and allows your code for data exploration "gracefully transition into code for
explanation." Another reason is because it's interactive.

> Interactive programming improves our ability to scrutinize behavior by poking:
> changing, deleting, reordering code, and seeing what happens.

In other words, Observable is a "reactive" programming environment.

## Reactive programming

We're used to "imperative" programming in scripting languages like Python
and JavaScript (R works that way too).
You may not think you've done reactive programming,
but you've done reactive programming if you've used a spreadsheet.
Imperative programming uses variable assignment, and you have to be careful
about state of a variable because operations are sequential.

    let i = 1;
    let x = 0;  // x = 0, i = 1;
    x = 2 * i;  // x = 2, i = 1; Right now, x = 2, and x == 2 * i
    ++i         // x = 2, i = 2; Right now, x = 2 but x != 2 * i


whereas reactive programming uses variable definition.

Time for a demo.

    i = {
      let i = 0;
      while (true) {
        yield ++i;
      }
    }

    \`The current value of 2 * i is ${2 * i}.\`

The `yield` keyword in JavaScript and Python is used to pause and resume a
generator function. (IE doesn't support `yield`.)

Q: What happens if you replace "yield" with "return"?

Q: What would happen if you tried to do things sequentially
by first creating the values in an Array, and then you returning the Array
so that the array could be processed in another cell?

    result = {
      let i = 0;
      let a = [];
      while (true) {
        a.push(++i);
      }
      return a;
    }

Hint: Think about this. If you try it, you might be sorry.

* Reading:
    * [Five-minute introduction](https://beta.observablehq.com/@mbostock/five-minute-introduction)
* References:
    * [Generator functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators#Generator_functions) -- MDN docs
    * [function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) -- MDN docs

## Generators

    (Repeated from last class): Observable uses the most modern browser capabilities, such as Promises and Generators.  
    Generators enable communication between Observable cells, allowing shared values to be updated dynamically.
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

## Interactive visualization

Observable quakes on leaflet: https://beta.observablehq.com/@pbogden/earthquakes-on-leaflet/

* TODO: Introduce a slider to solve the homework assignment for Class #3
    * Use this to develop some insights about the data
    * Overall pattern -- plate tectonics
    * Space vs magnitude -- western/eastern hemisphere (as per homework assignment)
    * Space vs time -- Oklahoma

## Earthquake Heatmap

* Consider the caveat about heatmaps in [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet)
* TODO: Adapt earthquakes dots on Leaflet to create a heatmap
* Look at the data-processing step in [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet)
* Look at the metro pattern

#### References

* [Observable Leaflet](https://beta.observablehq.com/@tmcw/leaflet) -- Tom MacWright
    * Shows how to do heatmap for DC crime that has been curated by Esri
* [Leaflet.heat](https://github.com/Leaflet/Leaflet.heat) -- Leaflet Heatmap Plugin

* [Introduction to Data](https://beta.observablehq.com/@mbostock/introduction-to-data) -- Mike Bostock
* [Introduction to Promises](https://beta.observablehq.com/@mbostock/introduction-to-promises) -- Mike Bostock
* [Observable standard library](https://github.com/observablehq/stdlib/blob/master/README.md)

#### References

* [Introduction to Generators](https://beta.observablehq.com/@mbostock/introduction-to-generators) -- Mike Bostock
* [function*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*) -- MDN docs
* [Generator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator) -- MDN docs

## Chloropleth maps

* Compare Plotly and D3.js examples
* (Maybe not this class.)

## Project ideas

* Look at Census data
* Explain the patterns in heatmap of crime: https://beta.observablehq.com/@tmcw/leaflet
    * [Metro locations as JSON](https://developer.wmata.com/docs/services/5476364f031f590f38092507/operations/5476364f031f5909e4fe3311)
    * Is there a better way to visualize the data distribution?

## Class #4 Assignment

* Investigate alternative visualizations of the crime data that mitigate stated concerns about heatmaps
