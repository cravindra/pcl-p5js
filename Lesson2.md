# Lesson 2: Animation in P5 Js

## How does Animation work?
- [Animation in frames](https://www.cs.cornell.edu/courses/cs3152/2021sp/labs/design3/walk.png)
- [Walk Cycle](https://i.gifer.com/5c7V.gif)


## Animations in P5 Js
- [frameRate()](https://p5js.org/reference/#/p5/frameRate)
- [draw()](https://p5js.org/reference/#/p5/draw)
- [frameCount](https://p5js.org/reference/#/p5/frameCount)


### Code sample:

```javascript
let rectX = 0;
let fr = 30; //starting FPS
let clr;

function setup() {
  background(200);
  frameRate(fr); // Attempt to refresh at starting FPS
  clr = color(255, 0, 0);
}

function draw() {
  background(200);
  rectX += 1; // Move Rectangle

  if (rectX >= width) {
    // If you go off screen.
    if (fr === 30) {
      clr = color(0, 0, 255);
      fr = 10;
      frameRate(fr); // make frameRate 10 FPS
    } else {
      clr = color(255, 0, 0);
      fr = 30;
      frameRate(fr); // make frameRate 30 FPS
    }
    rectX = 0;
  }
  fill(clr);
  rect(rectX, 40, 20, 20);
}
```


## Using Randomness
- [random()](https://p5js.org/reference/#/p5/random)



## Exercise
- [ ] Create a new sketch on P5 Js editor
- [ ] Animate a shape to move across the screen from left to right
  - [ ] Play with `frameRate()` to make the animation faster or slower
  - [ ] Once the object goes beyond the right edge of the screen, make it appear on the left edge of the screen
  - [ ] Make the object move faster
- [ ] Animate a shape falling from the top of the screen to the bottom
  - [ ] Once the object goes beyond the bottom edge of the screen, make it appear on the top edge of the screen
  - [ ] Make the object move faster as it falls ti simulate gravity
- [ ] Make a shape move towards a direction when a direction key is pressed
  - [keyCode](https://p5js.org/reference/#/p5/keyCode)
  - [keyPressed()](https://p5js.org/reference/#/p5/keyPressed)
  - [Key codes](https://keycode.info/)
  - Make the shape move towards where the user clicked



## References
- [About P5js](https://p5js.org)
- [P5js editor](https://editor.p5js.org/)
- [Getting started with P5js](https://p5js.org/get-started/)
- [P5js reference](https://p5js.org/reference/)
- [P5js showcase](https://p5js.org/showcase/)
