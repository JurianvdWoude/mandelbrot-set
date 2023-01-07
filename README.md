# Mandelbrot Set in p5.js

This project is a simple implementation of the Mandelbrot set using p5.js, 
a JavaScript library for creating graphics and interactive experiences.
You can find more information on the math behind this set on [wikipedia](https://en.wikipedia.org/wiki/Mandelbrot_set).


## Getting Started

To get started with this project, you will need to have a basic understanding of JavaScript and the p5.js library. 
If you are new to p5.js, you may want to check out the [p5.js website](https://p5js.org/) and the [p5.js reference](https://www.p5js.org/reference/) for more information.

To run this project, you will need a web browser that supports the canvas element and JavaScript.

## Running the Program

To run the program, simply open the `index.html` file in your web browser. 
You should see the Mandelbrot set displayed in the canvas. 

## Underlying Math

The Mandelbrot set is a mathematical set of points that is defined using a particular formula. Given a complex number c, the formula for determining whether a point belongs to the Mandelbrot set is:

<pre>
  z<sub>(n+1)</sub> = z<sub>(n)</sub>² + c
</pre>

where z<sub>(0)</sub> = 0 and z<sub>(n)</sub> is the result of the formula at the nth iteration.

Considering that z<sub>(1)</sub> is equal to c, with `c = a + bi`, where `a` is the real component, and `b` is the imaginary component, then:
<pre>
  z<sub>(2)</sub> = (a + bi)(a + bi) + (a + bi) = a² - b² + 2abi + a + bi
</pre>

We can then seperate the real and imaginary components, and plot the real values on the x-axis with `x = a² - b² + a`, and the imaginary values on the y-axis with `y = 2ab + b` on a 2D grid. Afterwards we replace a and b with real component `a = a² - b² + a` and imaginary component `b = 2ab + b` in the code, so that we can calculate the next generation of z.
