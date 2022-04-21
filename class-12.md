## Charts

- Copy chart.min.js into a javascript file
  - connect it to html file using: <script src="Chart.min.js"></script>
  - create a canvas element in our HTML. add <canvas id="id" width="200" height="400></canvas>
  to the body of your page
  - write a script (document.getElementbyID) that will retrieve the context of the canvas. add it to the foot of your body element
  -create your data inside the same script tags- above the line "let buyers= {"
-[specific examples of charts](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

## Basic Usage of Canvas

- canvas created a fixed-size drawing surface that exposes one or more rendering contects, which are used to create and manipulate the content shown.

  <canvas id="id" width="200" height="400></canvas>
  width & height are optional in the element and can be provided using DOM properties
  -during rendering, the image is scaled to fit its layout size and CSS might distort it so you might want to specify width and heigh in the canvas element

  -fall back content - allows for video audio and picture elements to play in older versions of browsers.

- insert the alternate content inside the canvas element. older browsers will ignore the container and render the fallback content inside. Newer browsers vice-versa

  -getContext() - used to get the rendering context and its drawing functions. accept the parameter- the type of context.
  -"2d" for 2D Graphics - CanvasRrenderingContext2D
    -let canvas = document.getElementById('tutorial');
    -let ctx = canvas.getContext('2d');
  - first line retrives the canvas element
  -2nd line acceses the drawing context

  - use - if (canvas.getContext) {let ctx= canvas.getContect('2d);
  } else{
    -canvas unsupported code here
  }
    - this checks to see if canvas is supported on the site

    <!-- \\example copied from Mozilla -->

    <script>
      function draw() {
        var canvas = document.getElementById('tutorial');
        if (canvas.getContext) {
          var ctx = canvas.getContext('2d');
        }
      }
    </script>
    <style>
      canvas { border: 1px solid black; }
    </style>
  </head>
  <body onload="draw();">
    <canvas id="tutorial" width="150" height="150"></canvas>

  - draw() - function that is executed once page loads. listens for the load event on doc.

  <!-- example copied from Mozilla - 2 transparent intersecting rectangles -->
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

#### Drawing Shapes with Canvas

- coordinate space - the canvas grid
- 1 in grid is 1 pixel on canvas
- origin of grid is positioned top left corner at coordinate (0,0).
- images are placed relative to to the origin.
- (x pixels from left, and y pixels from the top)

##### Drawing Rectangles

  -canvas only supports rectangles and paths (list of points connected by lines). other shapes are created using multiple paths.

- all 3 rectangle functions draw immediately to the canvas
    -fillRect(x, y, width, height)
  - draws filled rectange

  - strokeRect(x, y, width, height)
    - rectangular outline

    -clearRect(x, y, width, height)
  - makes rectangle fully transparent

- Path functions do not draw immediately to the canvas
  - create your path
  - [use drawing commands](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D#paths
    )
  - stroke or fill path to render it.

- functions used to do the above steps:
    -beginPath() - create new path
    -[methods to set different paths for objects](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D#paths)
    -closedPath() - adds straight line to path, going to start of the current sub-path(lines, arcs, ....). do not have to be called is the shape has already been closed or if only one point on the list
    -stroke()-draws shape by stroking its outline
  - fill() draws solid shape by filling the path's content area.
  - always use moveTo(x,y) after beginPath()
  - everytime a method is called, the list is reset so you can start drawing new shapes

- Arcs
- arc() and arcTo() methods
    arc(x, y, radius, startAngle, endAngle, counterclockwise) - an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by counterclockwise (defaulting to clockwise).
  -arcTo(x1, y1, x2, y2, radius)
  arc with the given control points and radius, connected to the previous point by a straight line.

- takes 6 parameters:
- x and y- coordinates of center of circle where the arc should be drawn
- radius
- startAngle and endAngle- define start and end points of the aric in radians, along the curve of the circle. measured from x axis. to converts degrees to radians, use : arc with the given control points and radius, connected to the previous point by a straight line.
 -counterclockwise - uses boolean value "true" which draws the arc counterclockwise

## Bezier and Quadratic Curves

  -used to draw complex organic shapes

  quadraticCurveTo(cp1x, cp1y, x, y)
  Draws a quadratic Bézier curve from the current pen   position to the end point specified by x and y, using the control point specified by cp1x and cp1y. has a start point, end point and one control point

  bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
  Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y). has start point, end point, and two control points

    - x & y parameters are the coordinates of the end point
    - cp1x & cp1y - coordinates of the first control point
    -cp2x & cp2y- coordinates of the second control point

## Path2D object

  -lets you cache or record these drawing commands. You are able to play back your paths quickly.

- constructor returns a newly instantiated Path2D object, w/another path as an argument (creates a copy), or w/a string consisting of SVG path data.
  - constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.
- combine paths using the addPath

## SVG Path - let p = new Path2D('M10 10 h 80 v 80 h -80 Z')

    - initialize paths on your canvas. This might allow you to pass around path data and re-use them in both, SVG and canvas.

## Colors

- fillStyle = color
Sets the style used when filling shapes.

- strokeStyle = color
Sets the style for shapes' outlines.

  globalAlpha = transparencyValue
Applies the transparency value to rest of shapes on the doc The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default

## Line styles

- lineWidth = value
  Sets the width of lines drawn in the future.

- lineCap = type
  Sets the appearance of the ends of lines.

- lineJoin = type
Sets the appearance of the "corners" where lines meet.

- miterLimit = value
  Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

- getLineDash()
  Returns the current line dash pattern array containing an even number of non-negative numbers.

- setLineDash(segments)
  Sets the current line dash pattern.

- lineDashOffset = value
  Specifies where to start a dash array on a line.

## Line Cap property

- The lineCap property determines how the end points of every line are drawn. There are three possible values for this property and those are: butt, round and square. By default this property is set to butt:

- butt
  The ends of lines are squared off at the endpoints.

- round
  The ends of lines are rounded.

- square
  The ends of lines are squared off by adding a box with an equal width and half the height of the line's thickness.

## Line Join property

- determines how two connecting segments (of lines, arcs or curves) with non-zero lengths in a shape are joined together (degenerate segments with zero lengths, whose specified endpoints and control points are exactly at the same position, are skipped).

round
Rounds off the corners of a shape by filling an additional sector of disc centered at the common endpoint of connected segments. The radius for these rounded corners is equal to half the line width.

bevel
Fills an additional triangular area between the common endpoint of connected segments, and the separate outside rectangular corners of each segment.

miter
Connected segments are joined by extending their outside edges to connect at a single point, with the effect of filling an additional lozenge-shaped area. effected by miterLimit

- setLineDash method & lineDashOffset property
 specify the dash pattern for lines.

## Gradients

- createLinearGradient(x1, y1, x2, y2)
  Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).

- createRadialGradient(x1, y1, r1, x2, y2, r2)
  Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.

- createConicGradient(angle, x, y)
Creates a conic gradient object with a starting angle of angle in radians, at the position (x, y).

- gradient.addColorStop(position, color) - to assign colors to gradient

## Patterns

createPattern(image, type)
Creates and returns a new canvas pattern object. image is a CanvasImageSource (that is, an HTMLImageElement, another canvas, a <video> element, or the like. type is a string indicating how to use the image.

- type specifies how to use the image in order to create the pattern, and must be one of the following string values:

- repeat
  Tiles the image in both vertical and horizontal directions.

- repeat-x
  Tiles the image horizontally but not vertically.

- repeat-y
  Tiles the image vertically but not horizontally.

- no-repeat
  Doesn't tile the image. It's used only once.

## Shadows

- shadowOffsetX = float
Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

- shadowOffsetY = float
  Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

- shadowBlur = float
  Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.

- shadowColor = color
  A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

## Draw Text

- function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.strokeText('Hello world', 10, 50);'
}

- font = value
  The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.

- textAlign = value
  Text alignment setting. Possible values: start, end, left, right or center. The default value is start.

- textBaseline = value
  Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.

- direction = value
  Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

- measureText()
Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.


## In Class Notes

  Global variable should be on top- declarations that you will use thorughout yoour sheet

  in object contructors, you don't have to add an object to the function parantheses, since DOM will be taking care of it later. set those objects to 0. ex: this.clicks = 0;

  productArray = []
  productArray.push(this);
  add the whole constructor into the array
  in constructors, this. refers to the whole objecct contructor. 

  GO OVER 51 MINUTE MARK IN REVIEW TODAY

example of checking to avoid duplicates
  let indexArray = [];

  function renderProductImg(){
    let randomNumber = getRandomIndex();
    if (!indexArray.includes(randomNumber)){
      indexArray.push(randomNumber);
    }
  }

  let productOneIndex = indexArray.pop();
   let productTwoIndex = indexArray.pop();
    let productThreeIndex = indexArray.pop();

Go over Event Handler function - 1 hour 15 minutes in 


##april 20th notes

# Class 13 Lecture Notes

## Data Persistance

### Local Storage

  - It is an object is accessed throough the browser it is stored on our computer
  - local storage is psecific fto one computer
  - no ecpiration time - cleans when we clear it

  ### Other Storage Types

    - 301 - NoSQL(MongoDB)
    -401 - SQL(postgres)

  ### Why

    - so uses can retain data between page refreshes or accessing different parts of the application

  ### How it is stored
  -JSON - Javascript Object Notation
  - in object key/value pairs
  - Convert to JSON - using a method 'JSON.stingify()'
    - converting our object to a string
  
  ### Methods that we use for Local Storage

  - save something to local storage
    -`setItem('key', value);`
  - get something oout of local storage
    - `getItem('key');`
  - Update an item in local storage
    - `setItem('key',value);`
  -Remove items from local storage
    - `removeItem('key');`
  -Clear all from local storage
    - `clear()`

  `localStorage
  JSON.parse - to unparse the string of code after you remove it from storage