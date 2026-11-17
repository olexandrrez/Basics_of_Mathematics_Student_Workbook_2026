# Problem 9: Point-to-Plane Distance and Line-to-Plane Angle

## Problem

**(a)** Find the distance from $P=(1,2,3)$ to $2x-y+2z=0$.

**(b)** Find the acute angle between a line with direction $(1,0,1)$ and the plane $z=0$.

## Worked Solution

### (a) Distance from a point to a plane

For $Ax+By+Cz+D=0$, the distance from $(x_0,y_0,z_0)$ is
$$d=\frac{|Ax_0+By_0+Cz_0+D|}{\sqrt{A^2+B^2+C^2}}.$$
Here $(A,B,C,D)=(2,-1,2,0)$, so
$$d=\frac{|2(1)-2+2(3)|}{\sqrt{4+1+4}}=\frac63=\boxed2.$$

### (b) Angle between a line and a plane

The plane $z=0$ has normal $n=(0,0,1)$. If $\alpha$ is the angle between the line direction $d=(1,0,1)$ and the plane, then $\sin\alpha=|d\cdot n|/(\|d\|\|n\|)$:
$$\sin\alpha=\frac1{\sqrt2},\qquad\boxed{\alpha=45^\circ}.$$

**Check.** The direction makes a $45^\circ$ angle with the plane normal as well; therefore its acute angle with the plane is also $45^\circ$ in this case.
