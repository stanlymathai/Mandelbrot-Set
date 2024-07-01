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