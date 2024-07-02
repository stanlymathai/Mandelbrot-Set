# Mandelbrot-Set
The Mandelbrot set is a famous fractal that is defined in the complex plane.

## Overview
1. Define the Complex Plane

    The Mandelbrot set is plotted in a specific region of the complex plane. We'll define this region and the resolution of our image.

2. Check Membership in the Mandelbrot Set

    The core algorithm involves iterating the function 𝑓 ( 𝑧 ) = 𝑧 2 + 𝑐 where 𝑧 and 𝑐 are complex numbers. A point 𝑐 is in the Mandelbrot set if the sequence 𝑧 0 = 0 , 𝑧 𝑛 + 1 = 𝑧 𝑛 2 + 𝑐 does not go to infinity.

    We'll limit the number of iterations and consider a point to be outside the Mandelbrot set if the magnitude of 𝑧 exceeds a certain threshold.

3. Render the Image

    Based on the number of iterations for each point, we'll color the point accordingly.

## Key Details
1. Complex Plane Mapping

    We map the pixel coordinates of our image to the complex plane using linear interpolation.

    `real := xMin + (xMax-xMin)*float64(x)/float64(width)` maps the x-coordinate
    `imaginary := yMin + (yMax-yMin)*float64(y)/float64(height)` maps the y-coordinate

2. Iteration Function

    `mandelbrot` function performs the iterations and returns the number of iterations before the sequence exceeds the threshold.

3. Color Mapping 

    The `colorMapping` function maps the number of iterations to a color. Points that remain within the set are colored black, while others are colored based on the number of iterations.

4. Image Creation

    `createMandelbrotImage` creates an image of the Mandelbrot set by iteration over each pixel, calculating the coresponding point in the complex plane and determining the color based on the iteration count.

5. Output

    The generated image is saved as `mandelbrot.png` in the current directory.

