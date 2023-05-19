# Lesson 5: Using ChatGPT to code

## Introduction
Large language models like GPT-3 are capable of generating text that is indistinguishable from human-written text. This has led to a lot of excitement about the potential of these models to be used for a variety of tasks. In this lesson, we will explore how to use the ChatGPT model to generate code.

## Strengths of GPT-3
- GPT-3 can be used to generate code
- GPT-3 can be used to generate text that is indistinguishable from human-written text

## Weaknesses of GPT-3
- Limited by the context it is provided
- Limited by the data it is trained on (the cut off date for training data is 2021)
- May make up facts that are not true
- May generate text that is offensive or inappropriate
- GPT-3 may generate code that is syntactically correct but does not work


## Ways of using GPT-3
- [Chat with GPT-3](https://chat.openai.com/)
- [Code with GPT-3](https://copilot.github.com/)
- [Build apps with GPT-3 API](https://platform.openai.com/docs/api-reference)


## Common Applications of GPT-3
- Summarization/Expanding/Explaining
- Translation
- Inferring (sentiment, intent, topics, emotions etc)
- Transforming (spelling and grammar checking, tone adjustment, and format conversion)


## Programming Applications of GPT-3
- Code generation
- Code completion
- Code summarization
- Code translation
- Code debugging
  

## Creating an account on ChatGPT

Sign up for an account on the [Chat GPT website](https://chat.openai.com/auth/login) and Log in


## Guidelines for writing prompts

- Provide clear context that the model needs to know
- Provide specific instructions for the model to follow
- Use delimiters to clearly indicate distinct parts of the prompt
    - Common delimieters: `` ``` ``, `"""`


## Prompt examples

### Code generation

```text
Write a program in p5 JS.
The  canvas dimensions should be 400x400
The background color should be off-white
It should draw a rectangle with dimensions 50x50 whose position can be controlled by the user by pressing directional buttons
```


### Code debugging

```text
Here is a program that is supposed to draw a rectangle and move it with the keyboard. There are some errors shown and the rectangle is not visible. Help me fix the bugs in this code:
"""
let x = 175; // initial x position of the rectangle
let y = 175; // initial y position of the rectangle
const rectSize = 50; // size of the rectangle
const canvasSize = 400; // size of the canvas
let rectColor = '#000000'; // initial color of the rectangle

function setp() {
  createCanvas(canvasSize, canvasSize);
  background(240); // off-white background color

  // Create a color picker
  colorPicker = createColorPicker(rectColor);
  colorPicker.position(10, 10);
  colorPicker.input(updateColor);
}

function draw() {
  background(240);

  // Draw the rectangle at the current position and color
}

function updateColor() {
  rectColor = colorPicker.value();
}

function mouseClicked() {
  // Check if the mouse click is inside the canvas
  if (mousX > 0 && mouseX < canvasSize && mouseY > 0 && mouseY < canvasSize) {
    // Update the position of the rectangle based on the mouse click
    x = mouseX - rectSize / 2;
    y = mouseY - rectSize / 2;
  }
}

function keyPressed() {
  // Move the rectangle based on the arrow key pressed
  if (keyCode === UP_ARROW && y > 0) {
    y -= 10; // move up
  } else if (keyCode === DOWN_ARROW) {
    y += 10; // move down
  } else if (keyCode === LEFT_ARROW && x > 0) {
    x -= 10; // move left
  } else if (keyCode === RIGHT_ARROW) {
    x += 10; // move right
  }
}
"""
```

## Resources:
- [ChatGPT Prompt Engineering for Developers from DeepLearning.AI](https://learn.deeplearning.ai/chatgpt-prompt-eng/)
