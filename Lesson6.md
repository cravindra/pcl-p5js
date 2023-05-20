# Lesson 6: Images and Sprites in P5js


## Images and Sound Files Resources

You can use the image and sound files in this location (feel free to use your own!)

[Image and Sound Repository](https://intro.nyuadim.com/wp-content/uploads/2022/02/image_sound_files.zip)

[Detailed cheat sheet](https://gist.github.com/MathuraMG/9fe4a610589b7ff72bcb1e7958f03a6a)

## Images

### Adding images to your sketch

To add an image to your sketch,

### Preloading and Drawing Images

In order to use images in P5js, we need to preload them. This is done in the `preload()` function. The `preload()` function is called before the `setup()` function. This ensures that the image is loaded before the sketch is run.
To display an image, we use the `image()` function. The `image()` function takes two arguments: the image to display and the x and y coordinates of where to display the image.

- [Preload](https://p5js.org/reference/#/p5/preload)
- [loadImage](https://p5js.org/reference/#/p5/loadImage)
- [image](https://p5js.org/reference/#/p5/image)

```javascript
let img;
function preload() {
  img = loadImage("assets/laDefense.jpg");
}

function setup() {
  image(img, 0, 0, width, height);
}
```


### Animating Sprites

```javascript
let img;
let imgHeight;
let imgWidth;
let frameWidth;
let frameHeight;

const spriteCountX = 12;
const spriteCountY = 4;

const FRAME_RATE = 60;
let frames = [];

function preload(){
  img = loadImage('assets/walking.png')
}

function setup() {
  
  imgWidth = img.width;
  imgHeight = img.height;
  
  frameWidth = imgWidth / spriteCountX;
  frameHeight = imgHeight / spriteCountY;
  
  createCanvas(frameWidth, frameHeight);
  
  for(let i = 0 ; i < spriteCountX ; i++) {
    frames.push(img.get(i * frameWidth, 0 , frameWidth, frameHeight))
  }
}

function draw() {
  background(220);
  const currentFrame = Math.floor(frames.length * (frameCount % FRAME_RATE) / FRAME_RATE);
  image(frames[currentFrame], 0 , 0, width, height);
}
```


### Exercise

- [ ] Create a new sketch in the P5js editor
- [ ] Add an image to your sketch
  - [ ] Draw it on to the canvas after preloading it
  - [ ] Inspect the image in the P5js editor by printing it to the console
  - [ ] Get the pixel values of the image
  - [ ] Draw the image to the canvas in black and white (loop over pixel values and normalise them to a grey scale value)
- [ ] Use a spritesheet to create an animation
  - [ ] Walking.png has a character walking in 4 different directions - make the character walk in a direction of your choice
    - [ ] Make the character turn when the user presses the directional keys
    - [ ] Move the character across the canvas when going left or right
- [ ] Add sounds to your sketch

