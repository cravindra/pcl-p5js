# Lesson 4: Putting it all together


## Simple Paint App with P5js
- [pmouseX](https://p5js.org/reference/#/p5/pmouseX)
- [pmouseY](https://p5js.org/reference/#/p5/pmouseY)
- [mouseX](https://p5js.org/reference/#/p5/mouseX)
- [mouseY](https://p5js.org/reference/#/p5/mouseY)
- [line](https://p5js.org/reference/#/p5/line)
- [mouseDragged](https://p5js.org/reference/#/p5/mouseDragged)


### Code Sample
```javascript
function setup() {
  createCanvas(400, 400);
  background(255);
}

function draw() {
}

function mouseDragged(){
  line(pmouseX, pmouseY, mouseX, mouseY);
}
```

## Adding buttons
- [Button](https://p5js.org/reference/#/p5/createButton)
- [Color Picker](https://p5js.org/reference/#/p5/createColorPicker)
- [P5 Element](https://p5js.org/reference/#/p5.Element)

```javascript
let lineColor = "#3C486B";
let button;

function clearBg() {
  background("#F0F0F0");
}
function setup() {
  createCanvas(400, 400);

  // Initialise the background
  clearBg();

  // Create a HTML button
  button = createButton("Clear canvas");
  // Specify it's position on the canvas
  button.position(0, 400);
  // Specify which function to run when the button is pressed
  button.mousePressed(clearBg);
}

function draw() {
  // Reset stroke color to be black for our color buttons
  stroke(0);
  // Reset stroke color to be black for our color buttons
  strokeWeight(1);
  // Draw square for blue color selector button
  fill("#3C486B");
  rect(5, 5, 50);
  // Draw square for red color selector button
  fill("#F45050");
  rect(5, 60, 50);
}

function mouseDragged() {
  // Set the stroke color to be the active color selected
  stroke(lineColor);
  // Set the stroke weight to be thick for our brush
  strokeWeight(4);
  // Draw the line
  line(pmouseX, pmouseY, mouseX, mouseY);
}

function mousePressed() {
  if (mouseX >= 5 && mouseX <= 50 && mouseY >= 5 && mouseY <= 50) {
    // The mouse was pressed inside the blue button
    lineColor = "#3C486B"; // Change line color to blue
  } else if (mouseX >= 5 && mouseX <= 50 && mouseY >= 60 && mouseY <= 110) {
    // The mouse was pressed inside the red button
    lineColor = "#F45050"; // Change line color to red
  }
}
```

### Painting in symmetry

```javascript
function setup() {
  createCanvas(400, 400);
  background(255);
  stroke("#3C486B");
  strokeWeight(4);
}

function draw() {}

function mouseDragged() {
  // Draw the line
  line(pmouseX, pmouseY, mouseX, mouseY);

  // Draw the mirror on the X axis
  line(width - pmouseX, pmouseY, width - mouseX, mouseY);

  // Draw the mirror on the Y Axis
  line(pmouseX, height - pmouseY, mouseX, height - mouseY);

  // Draw the mirron on both axes
  line(width - pmouseX, height - pmouseY, width - mouseX, height - mouseY);
}
```


## Exercise
- [ ] Create a new sketch on P5 Js editor
- [ ] Create a paint application that allows you to draw on the screen
  - [ ] Allow the user to select the color of the brush by clicking buttons
    - [ ] Use an array and a for loop to render and generate many color options
  - [ ] Allow the user to change the size of the brush by clicking buttons
  - [ ] Allow the user to clear the screen by clicking a button
  - [ ] Allow the user to turn on/off symmetry drawing by clicking a button
  - [ ] Allow the user to change the number of axes of symmetry by clicking buttons
  - [ ] Allow the user to select the background color by clicking buttons


## References
- [About P5js](https://p5js.org)
- [P5js editor](https://editor.p5js.org/)
- [Getting started with P5js](https://p5js.org/get-started/)
- [P5js reference](https://p5js.org/reference/)
- [P5js showcase](https://p5js.org/showcase/)
