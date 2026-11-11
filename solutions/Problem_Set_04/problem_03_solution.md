# Problem 3: Vector, Parametric, and Canonical Line Equations

## Problem

Find the vector, parametric, and canonical equations of the line through $P=(2,-1)$ with direction $d=(3,2)$. Convert the result to a general equation $Ax+By+C=0$, and find the point corresponding to parameter $t=1$.

## Worked Solution

A point on a line plus a scalar multiple of its direction vector describes every point on the line. Therefore the vector equation is
$$\boxed{(x,y)=(2,-1)+t(3,2)},\qquad t\in\mathbb R.$$
Equating coordinates gives the parametric equations
$$\boxed{x=2+3t,\qquad y=-1+2t}.$$
Since both components of $d$ are nonzero, eliminate $t$ to obtain the canonical form
$$\boxed{\frac{x-2}{3}=\frac{y+1}{2}}.$$
Cross-multiplication gives $2(x-2)=3(y+1)$, so the general form is
$$\boxed{2x-3y-7=0}.$$
At $t=1$, the parametric equations give $x=5$ and $y=1$.

**Answer and check:** the point is $\boxed{(5,1)}$. It satisfies $2(5)-3(1)-7=0$.
