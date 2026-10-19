# Problem 9: Definite Integral and Geometric Area

## 1. Original Problem
Compute $\int_{-1}^2x dx$, calculate the areas below and above the axis separately, and explain their difference.

## 2. What We Are Trying to Find
We distinguish signed accumulation from total geometric area by locating where the line crosses the horizontal axis.

## 3. Key Idea or Theorem Needed Before the Calculation
A definite integral counts area above the axis positively and below the axis negatively. Geometric area counts both positively, so split at zeros and use absolute area.

## 4. Step-by-Step Solution
An antiderivative is $x^2/2$, so
$$\int_{-1}^2x dx=\left[\frac{x^2}{2}\right]_{-1}^2=2-\frac12=\frac32.$$
The line crosses at 0. On $[-1,0]$ the triangle has base 1 and height 1, area $1/2$ below the axis. On $[0,2]$ it has base and height 2, area 2 above the axis. Total geometric area is $1/2+2=5/2$, while signed integral is $2-1/2=3/2$.

## 5. Why Each Step Is Valid
The sign of $x$ determines the sign of the contribution to the definite integral. Splitting at zero separates positive and negative parts.

## 6. Final Answer in Words
The definite integral is $3/2$; the total geometric area is $5/2$.

## 7. Quick Verification
The signed calculation equals positive area minus negative area: $2-1/2=3/2$.

## 8. Common Mistakes
- Reporting $5/2$ as the definite integral.
- Forgetting that below-axis regions contribute negatively.

## 9. Short In-Class Explanation
Integrating $x$ gives $3/2$. The triangle below the axis has area $1/2$, and the one above has area 2. Signed area subtracts them; geometric area adds them.
