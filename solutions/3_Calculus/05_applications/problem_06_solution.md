# Problem 6: Average Value of a Function

## 1. Original Problem
Find the average value of $f(x)=x^2$ on $[0,3]$, locate $c$ with $f(c)$ equal to that average, and interpret it geometrically.

## 2. What We Are Trying to Find
The average height is total accumulated area divided by interval length. Then we identify where the curve reaches this height.

## 3. Key Idea or Theorem Needed Before the Calculation
For continuous $f$ on $[a,b]$, average value is $\frac1{b-a}\int_a^b f(x)dx$. Solve $f(c)=f_{avg}$ within the interval.

## 4. Step-by-Step Solution
Compute the integral:
$$\int_0^3x^2dx=\left[\frac{x^3}{3}\right]_0^3=9.$$
Divide by the interval length 3:
$$f_{avg}=9/3=3.$$
Now solve $c^2=3$. Since $c$ must lie in $[0,3]$, $c=\sqrt3$ (the negative root is outside the interval).

## 5. Why Each Step Is Valid
The average-value theorem ensures a continuous function attains its average value somewhere on the interval; here direct solving identifies that point.

## 6. Final Answer in Words
Average value is 3, attained by the function at $c=\sqrt3$.

## 7. Quick Verification
$f(\sqrt3)=(\sqrt3)^2=3$. A rectangle of width 3 and height 3 has area 9, equal to the area under the curve.

## 8. Common Mistakes
- Dividing by 3 twice or forgetting to divide by interval length.
- Choosing $-\sqrt3$, which is not in the interval.

## 9. Short In-Class Explanation
Integrate $x^2$ to get area 9, then divide by interval length 3 to get average height 3. The curve has that height at $x=\sqrt3$.
