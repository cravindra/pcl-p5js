# Lesson 2: Objects, Arrays and Loops
- [Lesson 2: Objects, Arrays and Loops](#lesson-2-objects-arrays-and-loops)
  - [Using arrays and loops in JavaScript](#using-arrays-and-loops-in-javascript)
    - [Code Samples](#code-samples)
      - [Objects](#objects)
      - [Arrays](#arrays)
      - [Loops](#loops)
      - [Array methods](#array-methods)
    - [Common pitfalls](#common-pitfalls)
  - [Using loops and arrays in P5js](#using-loops-and-arrays-in-p5js)
    - [Code Samples](#code-samples-1)
      - [Draw a row (or column) of shapes](#draw-a-row-or-column-of-shapes)
      - [Draw a grid of shapes](#draw-a-grid-of-shapes)
  - [Exercise](#exercise)
  - [References](#references)

## Using arrays and loops in JavaScript
- [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)

### Code Samples

#### Objects
```javascript
// Declaring an object
let person = {
  name: "John",
  age: 30,
  isMarried: true,
  children: ["Alice", "Bob"]
};

// Accessing properties of an object
console.log(person.name); // prints "John"
console.log(person["age"]); // prints 30

// Dynamically accessing properties of an object
let propertyName = "age";
console.log(person[propertyName]); // prints 30

// Adding properties to an object
person.height = 180; // adds a new property to the object

// Removing properties from an object
person.height = undefined; // removes the property from the object

// Looping through the properties of an object
for (let key in person) {
  console.log(key); // prints the name of the property
  console.log(person[key]); // prints the value of the property
}

```

#### Arrays
```javascript
// Declaring an array
let colors = ["red", "green", "blue"];
let numbers = [1, 2, 3, 4, 5];
let mixed = ["red", 1, "green", 2, "blue", 3];
let empty = [];

// Getting the length of an array
console.log(colors.length); // prints 3

// Accessing elements in an array
console.log(colors[0]); // prints "red"
console.log(colors[1]); // prints "green"
console.log(colors[2]); // prints "blue"

// Adding elements to an array
colors.push("yellow"); // adds "yellow" to the end of the array
colors.unshift("orange"); // adds "orange" to the beginning of the array

// Removing elements from an array
colors.pop(); // removes the last element from the array
colors.shift(); // removes the first element from the array
```

#### Loops

```javascript
// Traditional Loops

// While loop
let i = 0; // initialise the counter variable
while (i < 10) { // condition to check if the loop should continue
  console.log(i);
  i++; // increment the counter variable
}

// Do while loop
let i = 0; // initialise the counter variable
do {
  console.log(i);
  i++; // increment the counter variable
} while (i < 10); // condition to check if the loop should continue

// For loop
for (
  let i = 0; // initialise the counter variable
  i < 10; // condition to check if the loop should continue
  i++ // increment the counter variable
  ) {
  console.log(i);
}
for (let i = 0; i < colors.length; i++) {
  console.log(colors[i]);
}

// Looping through an array
for (let i = 0; i < colors.length; i++) {
  console.log(colors[i]);
}
```
#### Array methods
```javascript
// Run some code for each element in the array
colors.forEach(function(color, idx, arr) {
  console.log(color);
});

// Create a new array from an existing array
const doubledArray = numbers.map(function(number, idx, arr) {
  return number * 2;
});

// Filter an array to keep only certain elements
const evenNumbers = numbers.filter(function(number, idx, arr) {
  return number % 2 === 0;
});

// Find an element in an array
const three = numbers.find(function(number, idx, arr) {
  return number === 3;
});

// Check if something is an array
Array.isArray(colors); // returns true

```


### Common pitfalls
- Index out of bounds
- Infinite loops
- Forgetting to increment the counter variable in a loop
- Forgetting to use the counter variable in a loop
- Forgetting to use the length of the array in a loop

## Using loops and arrays in P5js

### Code Samples

#### Draw a row (or column) of shapes

```javascript
let rectSize = 50;
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  for (
    let x = 0; // Start at the left edge of the screen
    x < width; // Continue as log as we are still within the canvas
    x = x + rectSize // Shift the x coordinate by the width of the rectangle each iteration
  ) {
    // Make a row by shifting the x cordinate to the right
    // for each iteration
    rect(x, 0, rectSize);
    // Make a column instead by changing the y coordinate
    // rect(0, y, rectSize);
  }
}
```


#### Draw a grid of shapes

```javascript
let rectSize = 50;
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  
  // Outer loop to move across the x axis
  for (
    let x = 0; // Start at the left edge of the canvas
    x < width; // Continue as log as we are still within the canvas
    x = x + rectSize // Shift the x coordinate by the width of the rectangle each iteration
  ) {
    
    // For each outer loop value of `x`, draw rectangles from top to bottom
    for (
      let y = 0; // Start at the top of the canvas
      y < height ; // Continue as long as we are still within the canvas
      y = y + rectSize // Shift the y coordinate by the height of the rectangle each iteration
    ) {
      rect(x, y, rectSize);
    }

  }
}
```





## Exercise
- [ ] Create a new sketch on P5 Js editor
- [ ] Create a row of circles using a for loop
- [ ] Create a grid of circles using a nested for loop
  - [ ] Randomise the shape and color of each circle
  - [ ] Make a chess board pattern
  - [ ] Make a generative QR Code
- [ ] Using the animation techniques from the previous lesson, animate many things at once
  - [ ] Raindrops falling from the sky
  - [ ] Bubbles floating up from the bottom of the screen
  - [ ] Ripples spreading out from a point
  - [ ] Traffic moving along a road
  - [ ] Traffic lights changing color


## References
- [About P5js](https://p5js.org)
- [P5js editor](https://editor.p5js.org/)
- [Getting started with P5js](https://p5js.org/get-started/)
- [P5js reference](https://p5js.org/reference/)
- [P5js showcase](https://p5js.org/showcase/)
