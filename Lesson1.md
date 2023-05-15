# Lesson 1: Introduction to Creative Coding with P5 Js

- [Lesson 1: Introduction to Creative Coding with P5 Js](#lesson-1-introduction-to-creative-coding-with-p5-js)
  - [What is Creative Coding?](#what-is-creative-coding)
    - [Applications of Creative Coding](#applications-of-creative-coding)
    - [Examples:](#examples)
  - [Introduction to P5 Js](#introduction-to-p5-js)
    - [Setup](#setup)
    - [Editor breakdown](#editor-breakdown)
    - [What is P5 js?](#what-is-p5-js)
    - [What can I do with P5js?](#what-can-i-do-with-p5js)
  - [Anatomy of a P5 Js sketch](#anatomy-of-a-p5-js-sketch)
    - [Code Sample:](#code-sample)
  - [Drawing in P5 Js](#drawing-in-p5-js)
    - [Code Sample:](#code-sample-1)
  - [Variables](#variables)
  - [Exercise](#exercise)
  - [References](#references)


## What is Creative Coding?

### Applications of Creative Coding
- Art
  - Generative Art
  - Interactive Art
- Data visualization
- Games
- Music
- Education

### Examples:
- [A train ride](https://editor.p5js.org/reajmorais/full/8UxKOWank)
- [Bubble words](https://editor.p5js.org/design.teo.ryu/full/I1PRivFtl)
- [Quilter](https://editor.p5js.org/ilovit/full/M7vOG2aoQ)


## Introduction to P5 Js

### Setup 
- Create an account on P5 Js online editor (allows you to save your sketches)
- [P5 Js online editor](https://editor.p5js.org/)

### Editor breakdown
- Code editor : where you write your code
- Console : where you can see any errors in your code or debug using print statements
- Canvas : where your sketch is displayed
- Saving your sketch (with a name)

### What is P5 js?
p5.js is a JavaScript library for creative coding, with a focus on making coding accessible and inclusive for artists, designers, educators, beginners, and anyone else! p5.js is free and open-source because we believe software, and the tools to learn it, should be accessible to everyone.

Using the metaphor of a sketch, p5.js has a full set of drawing functionality. However, you’re not limited to your drawing canvas. You can think of your whole browser page as your sketch, including HTML5 objects for text, input, video, webcam, and sound.


### What can I do with P5js?
- [P5js examples for various features](https://p5js.org/examples/)
- [P5js reference](https://p5js.org/reference/)


## Anatomy of a P5 Js sketch
A P5 Js sketch has two main functions:
- [draw()](https://p5js.org/reference/#/p5/draw) - This function is called continuously. It is used to draw shapes, images, text, etc. on the canvas.
- [setup()](https://p5js.org/reference/#/p5/setup) - This function is called only once. It is used to set the canvas size, background color, etc.
- [createCanvas()](https://p5js.org/reference/#/p5/createCanvas) - This function is used to create a canvas on which you can draw shapes, images, text, etc.
- [background()](https://p5js.org/reference/#/p5/background) - This function is used to set the background color of the canvas.
- Color Theory
  - How does color work on the web? [RGB](https://www.w3schools.com/colors/colors_rgb.asp) and [Hexadecimal](https://www.w3schools.com/colors/colors_hexadecimal.asp)
  - [Color Picker](https://coolors.co/ffffff)
- Color Palettes:
  - [Color Hunt](https://colorhunt.co/)
  - [Coolors Palettes](https://coolors.co/palettes/trending)
  - [Coolors Palette Generator](https://coolors.co/generate)
- Logging to the console
  - [print()](https://p5js.org/reference/#/p5/print)
  - [console.log()](https://developer.mozilla.org/en-US/docs/Web/API/Console/log)
- Debugging errors

### Code Sample:

```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    background(220);
    // background(220, 0, 0);
    // background(0, 220, 0);
    // background(0, 0, 220);
}
```


## Drawing in P5 Js
- Coordinates in P5 Js
  - [0,0] is the top left corner of the canvas
  - [width, height] is the bottom right corner of the canvas
  - [Image of coordinates](https://drive.google.com/file/d/1_wXIeQAHf2j1jcX0tlaFG2xD1m8pRRzP/view?usp=share_link)
- Adding Shapes
  - [rect()](https://p5js.org/reference/#/p5/rect)
  - [ellipse()](https://p5js.org/reference/#/p5/ellipse)
  - [triangle()](https://p5js.org/reference/#/p5/triangle)
  - [quad()](https://p5js.org/reference/#/p5/quad)
  - [arc()](https://p5js.org/reference/#/p5/arc)
  - [line()](https://p5js.org/reference/#/p5/line)
  - [point()](https://p5js.org/reference/#/p5/point)
- Adding colors to shapes
  - [fill()](https://p5js.org/reference/#/p5/fill)
  - [stroke()](https://p5js.org/reference/#/p5/stroke)
- Composing Shapes
  - Smiley Face
  - [Blueprints](https://drive.google.com/file/d/1E2E_v5FrM-jVk7eTA5GOkro44niKzHpj/view?usp=share_link)


### Code Sample:
```javascript
function setup() {
    createCanvas(400, 400);
}

function draw() {
    background(220);

    // rect(x, y, w, [h])
    // x - x coordinate of the top left corner of the rectangle
    // y - y coordinate of the top left corner of the rectangle
    // w - width of the rectangle
    // h (optional) - height of the rectangle (default is same as width if not specified)
    rect(10, 10, 50, 50);
    rect(10, 70, 160, 90);

    // ellipse(x, y, w, [h])
    // x - x coordinate of the center of the ellipse
    // y - y coordinate of the center of the ellipse
    // w - width of the ellipse
    // h (optional) - height of the ellipse (default is same as width if not specified)
    ellipse(40, 200, 50, 50);
}
```

## Variables
- Custom variables
- Built in variables
  - [width](https://p5js.org/reference/#/p5/width)
  - [height](https://p5js.org/reference/#/p5/height)
  - [mouseX](https://p5js.org/reference/#/p5/mouseX)
  - [mouseY](https://p5js.org/reference/#/p5/mouseY)
- Using mouseX and mouseY to draw shapes
- Creating a rudimentary drawing app

```javascript

let fillColor;
function setup() {
    createCanvas(400, 400);
    fillColor = '#D25380';
}
function draw() {
    background('#FFFAF4');

    // Set the stroke to black to color the line
    stroke(0);
    line(200,0,200,400);

    // Remove the stroke so that the shape does not have an outline
    noStroke();

    // Set the fill color 
    fill(fillColor);
    // Draw the ellipse at the current mouse position
    ellipse(mouseX, mouseY, 50, 50);
}

function mousePressed(){
    // When the mouse is pressed, change the fill color
    // based on the mouse position
    if(mouseX < 200){
        fillColor= '#D25380';
    }else {
        fillColor = '#E08E6D';
    }
}
```

## Exercise
- [ ] Create a new sketch on P5 Js editor
- [ ] Draw a few shapes on the canvas
  - [ ] Draw a rectangle, ellipse, triangle, line
  - [ ] Draw them at different locations on the canvas
  - [ ] Draw them with different colors
- [ ] Compose the shapes to create a face
  - [ ] Draw the example smiley face
  - [ ] Draw your own composition
- [ ] Play with the mouseX and mouseY variables
  - [ ] Draw a circle at the location of the mouse
  - [ ] Draw a circle at the location of the mouse and change its color based on the mouse location
  - [ ] Make a rudimentary painting app using the mouse location
    - [ ] Draw a circle at the location of the mouse when the mouse is pressed
      - [ ] [mousePressed()](https://p5js.org/reference/#/p5/mousePressed)
    - [ ] Change the color of the circle based on the mouse location
  - [ ] Animate your smiley face based on where the mouse is
    - [ ] Open and close the eyes
    - [ ] open and close the mouth



## References
- [About P5js](https://p5js.org)
- [P5js editor](https://editor.p5js.org/)
- [Getting started with P5js](https://p5js.org/get-started/)
- [P5js reference](https://p5js.org/reference/)
- [P5js showcase](https://p5js.org/showcase/)
