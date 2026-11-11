# Problem 1: Vector Arithmetic and a Unit Vector

## Problem

Let $u=(2,-1,2)$ and $v=(1,3,-2)$. Find $2u-v$, $\|u\|$, and a unit vector in the direction of $u$.

## Worked Solution

Scale each component of $u$ by $2$, then subtract the corresponding component of $v$:
$$2u-v=(4,-2,4)-(1,3,-2)=\boxed{(3,-5,6)}.$$

The Euclidean norm is the square root of the sum of the squared components:
$$\|u\|=\sqrt{2^2+(-1)^2+2^2}=\sqrt9=3.$$
A unit vector in the direction of a nonzero vector is the vector divided by its norm. Therefore
$$\widehat u=\frac{u}{\|u\|}=\boxed{\left(\frac23,-\frac13,\frac23\right)}.$$

**Check.** Its norm is $\sqrt{4/9+1/9+4/9}=1$, and it points in the same direction as $u$ because it is a positive scalar multiple of $u$.
