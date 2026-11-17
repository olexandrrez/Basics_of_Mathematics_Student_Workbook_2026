# Problem 10: Classifying a Parameterized Circle

## Problem

Classify the real curve
$$x^2+y^2-2x+4y+k=0$$
according to $k$. Include the degenerate and empty cases.

## Worked Solution

Complete the squares in $x$ and $y$:
$$x^2-2x+y^2+4y=-k,$$
$$ (x-1)^2-1+(y+2)^2-4=-k.$$
Therefore
$$\boxed{(x-1)^2+(y+2)^2=5-k}.$$
The centre is fixed at $(1,-2)$, while the right side determines the real points:

- If $k<5$, then $5-k>0$: a circle of radius $\sqrt{5-k}$.
- If $k=5$, then the radius is zero and the curve degenerates to the single point $(1,-2)$.
- If $k>5$, then the left side, a sum of squares, cannot equal the negative number $5-k$; there are no real points.

**Check.** These cases exhaust whether $5-k$ is positive, zero, or negative.
