**Simple Method to Calculate Pi using Montecarlo simulation**

The method used square with a inside circle. The x-Axis and y-Axis goes from -1 to 1 and the radio for the inside circle is 1. 

In order to approach this method you can formulate the questions ***what is the probability of a any random number for a pair (x,y) will be inside the circle?***. Let's define *P* as this probability


<img src="https://render.githubusercontent.com/render/math?math=P = \frac{Possible Cases}{Total Cases}= \frac{Circle Area}{Square Area}">

Lest's calculate the area of a square, and a circle inside the square. We can asume the cicle radio is **r**, and the side of the square is **2r**


The area of a square is $4r^2$.

<img src="https://render.githubusercontent.com/render/math?math=SquareArea = \ (2*r)*(2*r) = 4*r^2">
<img src="https://render.githubusercontent.com/render/math?math=CicleArea = \Pi*r^2">


So, the Probability can be calculated as 

<img src="https://render.githubusercontent.com/render/math?math=P = \frac{4r^2}{\pi*r^2} = \frac{\pi}{4}">


The calculated
<img src="https://render.githubusercontent.com/render/math?math=\pi = 4* P">


**The Montecarlo approach**. In order to apply this method using the Montecarlo simulation, we need to have a set of point (x,y) and we need to calculate the aproximation for the probability. This probabilty P is obtained dividing the *cases inside the circle by the total of iteration*. Remember, our square is -1 to 1, and the circle has a radio r=1. In order to know if a par(x,y) is inside the cicle  We need to calculate the distance to the center of the square, the coordenates (0,0). If the distance is less or equal to 1, the point in inside the circle. Using Pythagoras theorem, we calculate the distance *D* as

<img src="https://render.githubusercontent.com/render/math?math=\Distance = \sqrt{x^2 %2B y^2}">

Because our radio is equal to 1, we can use the next equation to figure out is the point is inside the cirle

<img src="https://render.githubusercontent.com/render/math?math=\x^2 %2B y^2 <=1">

So,

<img src="https://render.githubusercontent.com/render/math?math=\CalcPi = 4* \frac{Possible Cases}{Total Cases}">

Steps:
1. Generate a set(x,y) of uniform random number from -1 to 1. This set will identify a position inside the square.
2. Identify the number of cases that are inside the circle.
3. Calculate the probabilty of the any set (x,y) will be inside the circle and estimate Pi
