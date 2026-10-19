# Problem 4: Area Between Curves

## 1. Original Problem
Find the area bounded by $y=x$ and $y=x^2$, locating intersections and deciding which curve is above.

## 2. What We Are Trying to Find
Area between graphs is accumulated vertical distance. We first find the interval where the curves meet and determine the order of their heights.

## 3. Key Idea or Theorem Needed Before the Calculation
Solve equality for intersection bounds, then integrate upper curve minus lower curve.

## 4. Step-by-Step Solution
Solve $x=x^2$, obtaining $x=0$ and $x=1$. On $(0,1)$, $x-x^2=x(1-x)>0$, so $y=x$ lies above $y=x^2$. Therefore
$$A=\int_0^1(x-x^2)dx=\left[\frac{x^2}{2}-\frac{x^3}{3}\right]_0^1=\frac12-\frac13=\frac16.$$

## 5. Why Each Step Is Valid
The curves enclose a bounded region only between their intersection points. The integrand is nonnegative throughout that interval, matching geometric area.

## 6. Final Answer in Words
The enclosed area is $1/6$ square units.

## 7. Quick Verification
The line and parabola meet at both endpoints and the line is above between them, so the integral's positive sign is appropriate.

## 8. Common Mistakes
- Reversing upper minus lower, producing a negative value.
- Integrating outside the interval bounded by the intersections.

## 9. Short In-Class Explanation
The curves intersect at zero and one. Between them, $x$ exceeds $x^2$, so integrate $x-x^2$; the area is one sixth.
