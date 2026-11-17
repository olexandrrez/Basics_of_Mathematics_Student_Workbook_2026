# Problem 5: Line Through Two Points in Space

## Problem

Find vector, parametric, and symmetric equations of the line through $P=(1,-1,2)$ and $Q=(3,0,1)$.

## Worked Solution

Subtract the point coordinates to obtain a direction vector:
$$d=Q-P=(3-1,0-(-1),1-2)=(2,1,-1).$$
Using $P$ as a point on the line, the vector equation is
$$\boxed{(x,y,z)=(1,-1,2)+t(2,1,-1)},\qquad t\in\mathbb R.$$
Equating components gives the parametric equations
$$\boxed{x=1+2t,\quad y=-1+t,\quad z=2-t}.$$
Since each direction component is nonzero, the symmetric form is
$$\boxed{\frac{x-1}{2}=\frac{y+1}{1}=\frac{z-2}{-1}}.$$

**Check.** At $t=0$ the line gives $P$, and at $t=1$ it gives $Q$.
