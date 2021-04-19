# Content: 

### 1- Basic usage of canvas

### 2- Drawing shapes with canvas

### 3- Applying styles and colors

### 4- Drawing text


<br>
<br>



![Canvas!](https://s3-ap-south-1.amazonaws.com/trt-blog-ghost/2020/03/12.jpeg)




### First of all, What do we mean by canvas? 

<br>

>> * The HTML ``<canvas>`` element is used to draw graphics on a web page <mark>[1]</mark>, and it has only two attributes : (width and height) by default their values will be (300px, 150px). 

<br>



![Canvas-shapes!](https://cdn.mos.cms.futurecdn.net/SbV7qwk7jkrfhey8wWZ4Mb.jpg)


<br>


>> * There are some browsers that don't support canvas so the content of the canvas tag will be displayed as a fallback content just like the ``<video>`` , ``<audio>`` , ``<picture>`` elements. 

>> * Canvas has an opening and closing tags, unlike the ``<img>`` element, and If the closing tag was missing the whole content will be considered as a fallback content.

<br>


### How can I render the context of the canvas? 

<br>

>> * First of all, you need to have a script file in order to access the HTML element from there by doing the following:

<br>

```
<html>


<canvas id="testing"> 

</canvas>


<script>
let canvas = document.gitElementById('testing');

let x = canvas.getContext('2d'); //used to obtain the rendering context and its drawing functions
</script>


</html>
```
<br>


### What If the browser doesn't supoort canvas? we have to check for that! HOW? 

<br>

```
var canvas = document.getElementById('tutorial');

if (canvas.getContext) {
  var ctx = canvas.getContext('2d');
  // drawing code here
} else {
  // canvas-unsupported code here
}

```


>> We use ``fillRect`` to draw the shape and by default its color will be black, in order to change it we are going to use ``fillStyle`` and choose the color we want -> As the following : 

```
ctx.fillStyle = 'rgb(200, 0, 0)'; // To change the color of the shape
ctx.fillRect(x, y, width, height); // x : how far from the of the window border - y : from the top - fillRect displays a filled shape
ctx.clearRect(x, y, width, height); // The area of the shape displayed transparent.
ctx.strokeRect(x, y, width, height); // Only the border of the shape

```

![coordinate-space!](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes/canvas_default_grid.png)


<br>


### Drawing Paths

<br>

![Path!](https://cdn.dribbble.com/users/846207/screenshots/4341654/circle-along-with-path.gif)



**What exactly the path is?**

>>A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. <mark>[2]</mark>

**1- ``beginPath()``** -> To start drawing the path.

**2- ``moveTo()``** -> To place the starting point somewhere.

**3- ``lineTo()``** -> For drawing straight lines.

<br>
<br>


### arc of Circles 

```
arc(x, y, radius, startAngle, endAngle, counterclockwise)

arcTo(x1, y1, x2, y2, radius)
```

* ``x`` and ``y`` are the coordinates of the center of the circle on which the arc should be drawn.

* ``radius `` self-explanatory.

* ``startAngle`` and ``endAngle`` parameters define the start and end points of the arc in radians.

* The ``counterclockwise`` parameter is a Boolean value which, when true, draws the arc counterclockwise; otherwise, the arc is drawn clockwise.


<br>
<br>

* ``lineWidth = value``

>>Sets the width of lines drawn in the future.

* ``lineCap = type``

>>Sets the appearance of the ends of lines.

* ``lineJoin = type``

>> Sets the appearance of the "corners" where lines meet.

* ``miterLimit = value``

>> Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

* ``getLineDash()``

>> Returns the current line dash pattern array containing an even number of non-negative numbers.

* ``setLineDash(segments)``

>> Sets the current line dash pattern.

* ``lineDashOffset = value``

>> Specifies where to start a dash array on a line.

<hr>
<br>
<br>


References :

* [<mark>[1]</mark> W3School](https://www.w3schools.com/html/html5_canvas.asp)

* [<mark>[2]</mark> developer.mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

