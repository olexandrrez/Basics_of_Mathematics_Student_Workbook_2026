# Problem 7: Line of Intersection of Two Planes

## Problem

Find the line of intersection of $x+y+z=3$ and $x-y+z=1$. Verify your direction against both normals.

## Worked Solution

Subtract the second equation from the first to eliminate $x$ and $z$:
$$2y=2\quad\Longrightarrow\quad y=1.$$
Substitute into either plane equation to get $x+z=2$. Let $x=s$, so $z=2-s$. One point on the line is $(0,1,2)$ and a direction vector is $(1,0,-1)$. Thus
$$\boxed{(x,y,z)=(0,1,2)+s(1,0,-1)},\qquad s\in\mathbb R.$$

The plane normals are $n_1=(1,1,1)$ and $n_2=(1,-1,1)$. The direction is perpendicular to each:
$$n_1\cdot(1,0,-1)=1-1=0,\qquad n_2\cdot(1,0,-1)=1-1=0.$$

**Check.** For any $s$, $x+y+z=s+1+(2-s)=3$ and $x-y+z=s-1+(2-s)=1$.
