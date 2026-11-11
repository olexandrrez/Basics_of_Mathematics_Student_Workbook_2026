# Problem 10: Polar and Cylindrical Coordinates

## Problem

Convert the polar point $(r,\theta)=(4,5\pi/6)$ to Cartesian coordinates. Convert $P=(-\sqrt3,-1)$ to polar coordinates with $r\ge0$ and $0\le\theta<2\pi$. Finally, convert $Q=(1,\sqrt3,2)$ from Cartesian to cylindrical coordinates $(r,\theta,z)$. In each part, write the conversion formulas and show the substitutions.

## Worked Solution

### (a) Polar to Cartesian

Use $x=r\cos\theta$ and $y=r\sin\theta$. Since $\cos(5\pi/6)=-\sqrt3/2$ and $\sin(5\pi/6)=1/2$,
$$x=4\left(-\frac{\sqrt3}{2}\right)=-2\sqrt3,\qquad y=4\left(\frac12\right)=2.$$
Thus the Cartesian point is $\boxed{(-2\sqrt3,2)}$.

### (b) Cartesian to polar

Use $r=\sqrt{x^2+y^2}$. Then
$$r=\sqrt{(-\sqrt3)^2+(-1)^2}=\sqrt4=2.$$
The reference angle satisfies $\tan\alpha=|y/x|=1/\sqrt3$, so $\alpha=\pi/6$. Since $P$ is in quadrant III, the angle in the required range is $\theta=\pi+\pi/6=7\pi/6$. Therefore
$$\boxed{(r,\theta)=(2,7\pi/6)}.$$

### (c) Cartesian to cylindrical

For $Q=(x,y,z)$, cylindrical coordinates are $r=\sqrt{x^2+y^2}$, $\theta=\operatorname{atan2}(y,x)$, and the same $z$. Hence
$$r=\sqrt{1^2+(\sqrt3)^2}=2,\qquad \theta=\pi/3,\qquad z=2,$$
so $\boxed{(r,\theta,z)=(2,\pi/3,2)}$.

**Check.** Substituting $(r,\theta)=(2,7\pi/6)$ gives $x=-\sqrt3$ and $y=-1$. Substituting $(2,\pi/3,2)$ gives $(x,y,z)=(1,\sqrt3,2)$.
