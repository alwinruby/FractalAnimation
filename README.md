# Fractal Animation

A fractal is a mathematically defined, self similar object which has similarity and symmetry on a variety of scales. The Julia Set Fractal is a type of fractal defined by the behaviour of a function that operates on input complex numbers. More explicitly, upon iterative updating of input complex number, the Julia Set Fractal represents the set of inputs whose resulting outputs either tend towards infinity or remain bounded.

Mathematics of the Julia Set Fractal
The Julia Set Fractal is dependent upon complex numbers - numbers which have both a real and 'imaginary' component i, i being defined as the square root of -1. A complex number can formally be expressed as:

      c = r + b * i

Where c is the complex number, r is the real component and b the imaginary component. To create the bounded set, we first create a mathematical function f(z) which accepts a complex number, a simple example is the following equation...

      z = z2 + c

...where c is a constant complex number. The complex number z can be updated iteratively (here defined as F(z)):

Initialisation of the complex number variable z.
Iteratively updating the value of z based upon the function f().
Often, we set a threshold to prevent infinite iteration, which can be one or both of a) we surpass a value of z (in the examples below, iteration stops when absolute value of z exceeds 2) b) and/or b) we surpass a predefined number of iterations. Based upon either method, z can be defined as bounded or unbounded (iteration trends towards infinity).

Visualisation
To visualise the Julia Set Fractal, the initial z value can be defined as the location of a pixel in a 2-dimensional image: the real portion of the initial complex number the x pixel index, and the imaginary value the y pixel index (or vice-versa). For each pixel, we can initialise z based upon its index and plug the values into F() to determine whether the result is bounded or unbounded. Scale, rotation, and translation can be altered by appropriately modifying the input x and y values into the initial complex number z.


![](images/fractal1.png?raw=true)

One can create a binary image based upon the calculated values: black for bounded pixels and white for unbounded pixels. Alternatively, one could colour the image based upon resultant values. For instance, colour the pixel based upon the number of iterations necessary before the pixel is determined to be unbounded (for instance, when its absolute value becomes greater than 2), and/or for bounded values using a normalised value of the resulting end z value. Colours can be normalised to minimum/maximum values, or by using a colour lookup map.

Granularity, detail, and shapes can be modified by changing one or more of the maximum number of iterations, the function f(), and the constant value (should f() contain such a value). Alternatively, as alluded to above, zoom/scale, translation, and rotation can reflected by altering the initial x/y values.
