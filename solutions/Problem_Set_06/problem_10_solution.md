# Problem 10: A Parameterized Line and a Plane

## Problem

For each real $a$, consider
$$L_a:(x,y,z)=(0,0,a)+t(1,1,0),\qquad t\in\mathbb R,$$
and the plane $\Pi:x-y+z=2$. Substitute the line's parametric equations into the plane equation. Determine for which $a$ the entire line lies in $\Pi$, and for which $a$ it is parallel to but does not meet $\Pi$. For $a=0$, calculate the distance from $L_0$ to $\Pi$ using the point-to-plane distance formula. Explain why every point of $L_0$ has the same distance to $\Pi$.

## Worked Solution

The parametric coordinates of the line are $x=t$, $y=t$, and $z=a$. Substituting into the plane equation gives
$$t-t+a=a.$$
The condition for a point on the line to be in the plane is therefore $a=2$:

- If $a=2$, every value of $t$ satisfies the plane equation, so the entire line lies in $\Pi$.
- If $a\ne2$, no value of $t$ satisfies it. The line is parallel to the plane because its direction $d=(1,1,0)$ is perpendicular to the plane normal $n=(1,-1,1)$: $d\cdot n=0$. Thus for $a\ne2$ it is parallel and disjoint.

For $a=0$, take the point $(0,0,0)$ on $L_0$. The point-to-plane distance is
$$d=\frac{|0-0+0-2|}{\sqrt{1^2+(-1)^2+1^2}}=\boxed{\frac2{\sqrt3}}.$$
Every point on $L_0$ has form $(t,t,0)$, and its plane-expression value is $t-t+0-2=-2$, independent of $t$. Consequently every point has the same distance $2/\sqrt3$ from the plane.

**Check.** The line direction is parallel to the plane, while its signed plane value remains constant along the line.
