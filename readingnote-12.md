# Reading 12 - Chart.js, Canvas

## Chart.js

**Chart.js**- a plugin that renders a chart onto the webpage.
-pie-chart, graph, etc.
-easier way to render charts.

## Canvas

**< canvas>**- an element that allows the rendering of a video or an image onto the page.
-only has a width and height attribute, unlike the *< img>* element.
-fallback information is placed inside the element, whereas the *< img>* has an alt attribute that is contained within the tag itself.

*note* it is essential to have a closing < /canvas> tag, unlike an *img* element.

## Drawing Rectangles

3 Functions that render rectangles on < canvas>:

  1.**fillRect(x, y, width, height)**
    -creates a *filled* rectangle
  2.**strokeRect(x, y, width, height)**
    -a rectangular outline
  3.**clearRect(x, y, width, height)**
    -*clears* the space for the rectangle and makes it *transparent*

## Paths

**Paths**- points that essentially "connect the dots".
-*paths* are lines that create shapes with various *widths* and *colors*.

### STEPS TO CREATE A PATH

1.Establish a path
2.Use *methods* to draw the *path*
3.fill using one of the above functions (fill, or stroke)

#### Examples

**beginPath()**- establishes the new *path*

**closePath()**- line from the start to the current line or *path*

**stroke()**- creates an outline of a shape

**fill()**- *fills* the are to render a shape

## Color Methods

*fillStyle = "color"*
-fill in the desired shape with color

*strokeStyle = "color"*
-adds outline shape with color

## Line Styles

*lineWidth = value*

*lineCap = type*
-appearance of the end of the line

## Drawing Text

**fillText(text, x, y [, maxwidth])**
-*fills* text at the exact coordinates.

**strokeText(text, x, y [, maxwidth])**
-outline text at exact coordinates

## Text Style

Can manipulate the text within JavaScript using the DOM manipulation methods.

Examples:
*font= value*
*textAlign = value*

[<==Back](README.md)