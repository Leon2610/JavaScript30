# 08- Fun with HTML5 Canvas

This is a JavaScript practice for the [#JavaScript30](https://javascript30.com/) created by [Wes Bos](https://github.com/wesbos), the challenge is to create 30 things in 30 days just with Vanilla JS

## Overview

### About this project

Learn how to use canvas in html5 to make drawings with the mouse

### Screenshot

![](gif.gif)

**Hold down the mouse and move it over the screen to draw.**

### Links

- Live Site URL: [Fun with HTML5 Canvas](https://html5canvasjs30.netlify.app/)

### What I learned

**Working with Canvas in HTML5 and JavaScript**

This project focuses on using Canvas, an HTML5 element, along with JavaScript to create interactive graphics and drawings on a web page.

**What is Canvas?**

Canvas is an HTML element that allows us to draw graphics, animations, and visual elements on a web page. It provides a rectangular surface where pixels can be manipulated individually or through more advanced drawing methods.

- **Canvas**: It is an HTML element used for drawing graphics, animations, and visual elements on a web page. It provides a rectangular surface where pixels can be manipulated individually or through more advanced drawing methods.

- **getContext('2d')**: It is a JavaScript method used to obtain the 2D drawing context of a canvas element. The 2D context provides a set of methods and properties for drawing and manipulating graphics on the canvas.

- **strokeStyle**: It is a property of the 2D context that defines the color or style of the border used when drawing strokes. It can be a solid color, gradient, or pattern.

- **lineJoin**: It is a property of the 2D context that specifies how lines are joined when they have corners. It can have values like "miter" (sharp corners), "round" (rounded corners), or "bevel" (beveled corners).

- **lineCap**: It is a property of the 2D context that determines the appearance of the end of a line when no further extension is drawn beyond it. It can have values like "butt" (square end), "round" (rounded end), or "square" (square end with an extension).

- **beginPath()**: It is a method of the 2D context that initiates a new drawing path. It is used to start defining a set of segments and curves that make up a path.

- **moveTo()**: It is a method of the 2D context that moves the starting point of a drawing path to the specified coordinates without drawing any lines.

- **stroke()**: It is a method of the 2D context that draws the outlines of the current path with the color or style specified by the strokeStyle property. The stroke is drawn using the lineJoin, lineCap properties, and other previously defined settings.