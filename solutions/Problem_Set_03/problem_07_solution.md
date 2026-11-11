# Problem 7: Area of a Triangle in Three Dimensions

## Problem

Find the area of the triangle with vertices $A=(0,0,0)$, $B=(2,0,1)$, and $C=(0,3,1)$.

## Worked Solution

The two sides from $A$ are
$$\overrightarrow{AB}=(2,0,1),\qquad \overrightarrow{AC}=(0,3,1).$$
The magnitude of their cross product is the area of the parallelogram they span; the triangle has half that area:
$$\overrightarrow{AB}\times\overrightarrow{AC}=(-3,-2,6),$$
$$\text{Area}=\frac12\|(-3,-2,6)\|=\frac12\sqrt{9+4+36}=\boxed{\frac72}.$$

**Check.** The cross product is nonzero, so the three vertices are not collinear and the triangle has positive area.
