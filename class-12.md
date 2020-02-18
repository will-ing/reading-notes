# Docs for the HTML <canvas> Element & Chart.js

## Creating a Chart

It's easy to get started with Chart.js. All that's required is the script included in your page along with a single \<canvas> node to render the chart.

In this example, we create a bar chart for a single dataset and render that in our page. You can see all the ways to use Chart.js in the usage documentation.

>the \<canvas> element has only two attributes, width and height

>Providing fallback content is very straightforward: just insert the alternate content inside the \<canvas> element.

*Requires closing tag*

>The script includes a function called draw(), which is executed once the page finishes loading;

```html
<html>
 <head>
  <meta charset="utf-8"/>
  <script type="application/javascript">
    function draw() {
      var canvas = document.getElementById('canvas');
      if (canvas.getContext) {
        var ctx = canvas.getContext('2d');

        ctx.fillStyle = 'rgb(200, 0, 0)';
        ctx.fillRect(10, 10, 50, 50);

        ctx.fillStyle = 'rgba(0, 0, 200, 0.5)';
        ctx.fillRect(30, 30, 50, 50);
      }
    }
  </script>
 </head>
 <body onload="draw();">
   <canvas id="canvas" width="150" height="150"></canvas>
 </body>
</html>
```

### here are **three functions** that draw rectangles on the canvas:

1. `fillRect(x, y, width, height)` Draws a filled rectangle.

2. `strokeRect(x, y, width, height)` Draws a rectangular outline.

3. `clearRect(x, y, width, height)` Clears the specified rectangular area, making it fully transparent.

```js
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}
```

## Applying styles and colors

Attribute | Descriptions
---- | ----
`fillStyle = color` | Sets the style used when filling shapes.
`strokeStyle = color` | Sets the style for shapes' outlines.
`globalAlpha = transparencyValue` | Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

>We use the `arc()` method to draw circles instead of squares.

## Drawing text

Property | Descriptions
---- | ----
`fillText(text, x, y [, maxWidth])` | Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
`strokeText(text, x, y [, maxWidth])` | Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

```js
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.fillText('Hello world', 10, 50);
}

```
## Styling Text 

Property | Descriptions
---- | ----
`font = value` | The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
`textAlign = value` | Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
`textBaseline = value` | Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
`direction = value` | Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

```js
ctx.font = '48px serif';
ctx.textBaseline = 'hanging';
ctx.strokeText('Hello world', 0, 100);

```


[Main Page](https://will-ing.github.io/reading-notes)