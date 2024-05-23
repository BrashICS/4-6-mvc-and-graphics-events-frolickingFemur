# 4.6 - Controlling Graphics Using MVC and p5js

###### ICS4U - Mr. Brash 🐿️

## It's Time!

The time has come to connect everything you have learned in the past two years. Variables, loops, if-statements, abstract data types, Objects, HTML... and now **Graphics**!

  > **Please note: your final project does _not_ need to use graphics, a canvas, or p5js. This is merely an example.**

We are going to use a [graphics library](https://en.wikipedia.org/wiki/Graphics_library) called [p5js](https://p5js.org/) to help make our life a bit easier for drawing shapes and images or writing text on top of graphics.

### Most games incorporate the Cartesian Plane or a 2D Grid

Think of checkers, [chess](https://chess.adamts.me/), battleship, and [minesweeper](https://minesweeper.brash.ca). Even Flappy Bird, [Pacman](https://pacman.brash.ca), or Crossy Road need to utilize a Cartesian Plane (x, y) to know where objects are to be drawn on the screen.

This repository has some code in it already. Here's the breakdown:

- The [index.html](index.html) file sets up the heading, loads the p5js graphics library into memory, and loads our [script.js](script.js) file into memory.
- The [script.js](script.js) file does a bit of heavy lifting. It:
  - Defines some global values to make life easier
  - Defines a very simple Square object that only tracks `colour` (an array of RGB values) and `value` (a number).
  - Utilizes the p5js [`setup()`](https://p5js.org/reference/#/p5/setup) function to create a canvas. Feel free to adjust the size using the global constants.
    - The `setup()` function also initalizes a 2D array of Squares. This is a very _simplistic_ model. In reality the `grid` variable should also be an Object that draws itself, etc.
  - Utilizes the p5js [`draw()`](https://p5js.org/reference/#/p5/draw) function (which gets called 60 times per second) to:
    - erase the scene by painting it grey with the [`background()`](https://p5js.org/reference/#/p5/background) function.
    - draw a grid that is (x, y) in size onto the scene. The `draw_grid(x, y)` function was created for you to demonstrate how easy it is to draw on the canvas using p5js and a little math. Feel free to change the size of the grid - right now it is 8x8 to mimic a chess board.

# Your Task(s)

First of all - you should make sure that you have the p5js [reference page](https://p5js.org/reference/) open and maybe look through some [examples](https://p5js.org/reference/). Also, if you don't understand the code in this repo, you might want to ask Mr. Brash for clarification.

### Task the first:

- Modify the model (grid initialization) so that every second square is coloured a different colour, to mimic a classic [chess or checker board](https://en.wikipedia.org/wiki/Checkerboard). The colours you select are up to you.

### Task the second:

- Learn how to add a [click event listener](https://p5js.org/reference/#/p5/mouseClicked) on the canvas. Write a function that will increment the `.value` of a certain location in the grid when it is clicked.<br>**Hint:** this is going to require some math, some research, and the `mouseX` / `mouseY` [p5js variables](https://p5js.org/reference/#/p5/mouseX).

### Task the third:

- If you've made it this far - congratulations! What we want to do now is highlight the most recently clicked square. So whatever you just clicked on should turn red or yellow or something obvious. The next square you click on should then get this highlight and the previously highlighted square goes back to its normal colour, with regards to the chess board setup.

### Task the fourth:

- Consider yourself a master programmer, do you? Well then, modify the mouse listener so that if a user right-clicks on a square it resets the value to zero. Furthermore, add a keyboard listener so that hitting ESC unhighlights the currently highlighted square (assuming one is highlighed).

---

If you do not understand the code or any of the tasks above, please do not hesitate to ask for assistance!

<br>
🐿️
