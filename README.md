**Simple Method to Calculate Pi using Monte Carlo Simulation**

The method uses a square with an inside circle. The x-Axis and y-Axis go from -1 to 1, and the radius of the inside circle is 1.

In order to apply this method, you can formulate the question: ***What is the probability that any random pair (x, y) will be inside the circle?*** Let's define *P* as this probability:

$$
P = \frac{\text{Possible Cases}}{\text{Total Cases}} = \frac{\text{Circle Area}}{\text{Square Area}}
$$

Let's calculate the area of a square and a circle inside the square. We can assume the circle's radius is **r**, and the side of the square is **2r**.

The area of a square is:

$$
\text{Square Area} = (2r) \cdot (2r) = 4r^2
$$

The area of the circle is:

$$
\text{Circle Area} = \pi r^2
$$

So, the probability can be calculated as:

$$
P = \frac{\pi r^2}{4r^2} = \frac{\pi}{4}
$$

From this, we can calculate:

$$
\pi = 4 \cdot P
$$

**The Monte Carlo Approach**  
To apply this method using Monte Carlo simulation, we need to generate a set of points (x, y) and approximate the probability. This probability *P* is obtained by dividing the number of cases inside the circle by the total number of iterations.  

Remember, our square spans from -1 to 1, and the circle has a radius \( r = 1 \). To determine if a pair (x, y) is inside the circle, we calculate the distance from the point to the center of the square at coordinates (0, 0). If the distance is less than or equal to 1, the point is inside the circle. Using Pythagoras' theorem, the distance *D* is calculated as:

$$
D = \sqrt{x^2 + y^2}
$$

Because the radius is equal to 1, we can use the following condition to check if the point is inside the circle:

$$
x^2 + y^2 \leq 1
$$

Finally, Pi can be calculated as:

$$
\pi = 4 \cdot \frac{\text{Possible Cases}}{\text{Total Cases}}
$$

### Steps:
1. Generate a set (x, y) of uniform random numbers from -1 to 1. This set identifies positions inside the square.
2. Count the number of cases that fall inside the circle.
3. Calculate the probability of any set (x, y) being inside the circle and estimate Pi.
