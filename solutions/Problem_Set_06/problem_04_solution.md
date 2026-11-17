# Problem 4: Angles and Planes Parallel or Perpendicular to a Given Plane

## Problem

Find the acute angle between the planes $x+y=1$ and $x+z=2$. Also give a plane through the origin parallel to the first plane, and one perpendicular to it.

## Worked Solution

The normal vectors are $n_1=(1,1,0)$ and $n_2=(1,0,1)$. The acute angle between planes is the acute angle between their normals:
$$\cos\theta=\frac{|n_1\cdot n_2|}{\|n_1\|\|n_2\|}=\frac{|1|}{\sqrt2\sqrt2}=\frac12,$$
so $\boxed{\theta=60^\circ}$.

A plane parallel to $x+y=1$ has the same normal. Through the origin it is $\boxed{x+y=0}$. For a plane perpendicular to the first, choose a normal perpendicular to $n_1$. For example, $m=(1,-1,0)$ has $m\cdot n_1=0$, so the plane through the origin with this normal is $\boxed{x-y=0}$.

**Check.** The parallel plane has the same normal as the first. The chosen perpendicular plane has a normal orthogonal to $n_1$, so the two planes meet at a right angle.
