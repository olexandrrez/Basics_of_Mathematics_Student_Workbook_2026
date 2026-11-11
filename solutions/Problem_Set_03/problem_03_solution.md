# Problem 3: Internal Division of a Segment

## Problem

Find the point $P$ dividing the segment from $A=(-2,1,3)$ to $B=(4,7,-3)$ internally in the ratio $AP:PB=1:2$.

## Worked Solution

The ratio says that $P$ is one third of the way from $A$ to $B$. First find the displacement:
$$\overrightarrow{AB}=B-A=(4-(-2),7-1,-3-3)=(6,6,-6).$$
One third of this displacement is $(2,2,-2)$, so
$$P=A+\frac13\overrightarrow{AB}=(-2,1,3)+(2,2,-2)=\boxed{(0,3,1)}.$$

Equivalently, the section formula gives $P=(2A+B)/3$ because the point is closer to $A$ and the opposite segment weight is $2$.

**Check.** $P-A=(2,2,-2)$ and $B-P=(4,4,-4)$, so $|AP|:|PB|=1:2$.
