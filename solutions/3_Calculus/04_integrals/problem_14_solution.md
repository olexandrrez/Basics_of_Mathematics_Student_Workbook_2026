# Problem 14: A Piecewise-Defined Function

## 1. Original Problem
For $f(x)=x+1$ on $[-1,1)$ and $f(x)=2$ on $[1,3]$, sketch, split and calculate $\int_{-1}^3 f(x)dx$, then verify geometrically.

## 2. What We Are Trying to Find
The function changes formula at 1, so we divide the integral there and compare the calculation with the areas of simple shapes.

## 3. Key Idea or Theorem Needed Before the Calculation
Definite integrals are additive across adjacent intervals. A piecewise definition must be followed on its corresponding interval.

## 4. Step-by-Step Solution
Split at $x=1$:
$$\int_{-1}^3f(x)dx=\int_{-1}^1(x+1)dx+\int_1^3 2dx.$$
The first term evaluates to
$$\left[\frac{x^2}{2}+x\right]_{-1}^1=\frac32-\left(-\frac12\right)=2.$$
The second is $[2x]_1^3=6-2=4$. The total is 6.

The graph is the line segment from $(-1,0)$ to $(1,2)$ followed by a horizontal segment at height 2 to $x=3$. The first area is a triangle with base and height 2, area 2; the second is a rectangle $2\times2$, area 4.

## 5. Why Each Step Is Valid
The split matches the definition's breakpoint. Both graph sections lie above the axis, so ordinary geometric area equals the definite integral.

## 6. Final Answer in Words
The integral is 6, matching triangle area 2 plus rectangle area 4.

## 7. Quick Verification
The antiderivative calculation gives 2+4, and the geometric calculation independently gives the same total.

## 8. Common Mistakes
- Using $x+1$ over the whole interval.
- Forgetting to split at the change of formula.

## 9. Short In-Class Explanation
Split the integral where the formula changes. The line section contributes area 2 and the constant section contributes 4, so the total is 6.

```text
y
2 |          ●────────────●
  |        ╱
  |      ╱
0 ●────╱────────────────────→ x
  −1   1                    3
```
