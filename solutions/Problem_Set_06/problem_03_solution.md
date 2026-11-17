# Problem 3: Plane Given by Two Direction Vectors

## Problem

A plane is given by
$$ (x,y,z)=(1,2,-1)+s(1,0,1)+t(0,2,1).$$
Find its general equation and determine whether the origin lies on it.

## Worked Solution

The two direction vectors are $u=(1,0,1)$ and $v=(0,2,1)$. Their cross product gives a normal to the plane:
$$n=u\times v=(-2,-1,2).$$
Using the point $(1,2,-1)$, the plane equation is
$$(-2,-1,2)\cdot(x-1,y-2,z+1)=0.$$
Expanding gives $-2x-y+2z+6=0$. Multiplying by $-1$ gives the equivalent general equation
$$\boxed{2x+y-2z-6=0}.$$
At the origin the left side equals $-6$, not zero. Thus the origin does not lie on the plane.

**Check.** The normal is perpendicular to both spanning directions: $(-2,-1,2)\cdot(1,0,1)=0$ and $(-2,-1,2)\cdot(0,2,1)=0$.
