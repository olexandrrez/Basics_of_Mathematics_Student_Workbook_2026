# Problem 9: Coplanarity and Linear Combination

## Problem

For which $t$ are $a=(1,0,1)$, $b=(0,1,1)$, and $c=(2,3,t)$ coplanar? Verify your answer by a linear combination.

## Worked Solution

The vectors $a$ and $b$ are independent, so they span a plane through the origin. For $c$ to lie in that plane, it must be a linear combination $c=\alpha a+\beta b$. Comparing the first and second components gives $\alpha=2$ and $\beta=3$. The third component must therefore be
$$t=\alpha+\beta=2+3=\boxed{5}.$$

Indeed, when $t=5$,
$$c=(2,3,5)=2(1,0,1)+3(0,1,1)=2a+3b,$$
which verifies coplanarity directly.

**Check.** The combination produces all three coordinates of $c$ exactly when $t=5$.
