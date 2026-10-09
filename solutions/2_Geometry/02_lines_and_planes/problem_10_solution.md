# Problem 10: Projection of a Point onto a Plane

## 1. Original Problem
Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

## 2. What We Are Trying to Find
We must find the orthogonal projection point $P'$ of point $P$ onto plane $\Pi$, calculate the reflected point $P''$ across the plane, and verify that the midpoint of the segment $[P, P'']$ is $P'$ and satisfies the equation of the plane.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Normal Line Through $P$**: The line dropped from $P$ perpendicular to plane $\Pi$ has direction equal to the normal vector $n$:
  $$L_{\text{norm}}: X(t) = P + t n.$$
- **Orthogonal Projection $P'$**: The intersection of this normal line with the plane occurs at parameter $t_0$, giving $P' = P + t_0 n$.
- **Symmetric Reflection $P''$**: Moving twice as far along the normal line gives the reflection:
  $$P'' = P + 2 t_0 n = 2 P' - P.$$
- **Midpoint Property**: The midpoint $M = \frac{P + P''}{2}$ must equal $P'$ and lie on $\Pi$.

## 4. Step-by-Step Solution

### Step 1: Set Up the Normal Line Through $P$
For plane $\Pi: x + y + z = 3$, the normal vector is:
$$n = (1, 1, 1).$$
The line through $P = (2, 1, 3)$ in direction $n$ is:
$$\begin{pmatrix} x(t) \\ y(t) \\ z(t) \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \\ 3 \end{pmatrix} + t \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix} = \begin{pmatrix} 2 + t \\ 1 + t \\ 3 + t \end{pmatrix}.$$

### Step 2: Find the Projection $P'$
Substitute the parametric coordinates into the plane equation $x + y + z = 3$:
$$(2 + t) + (1 + t) + (3 + t) = 3.$$
Simplify:
$$6 + 3t = 3 \implies 3t = 3 - 6 = -3 \implies t = -1.$$
Substitute $t = -1$ into the line equations to find $P'$:
$$P' = \begin{pmatrix} 2 + (-1) \\ 1 + (-1) \\ 3 + (-1) \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \\ 2 \end{pmatrix}.$$
The orthogonal projection of $P$ onto the plane is $P' = (1, 0, 2)$.

### Step 3: Find the Reflection $P''$
The reflection corresponds to twice the parameter step: $t = 2(-1) = -2$:
$$P'' = P + 2(-1)n = \begin{pmatrix} 2 - 2(1) \\ 1 - 2(1) \\ 3 - 2(1) \end{pmatrix} = \begin{pmatrix} 0 \\ -1 \\ 1 \end{pmatrix}.$$
The reflection of $P$ across the plane is $P'' = (0, -1, 1)$.

### Step 4: Check That the Midpoint Lies on the Plane
Compute the midpoint $M$ of segment $[P, P'']$:
$$M = \frac{P + P''}{2} = \frac{(2, 1, 3) + (0, -1, 1)}{2} = \frac{(2 + 0, 1 + (-1), 3 + 1)}{2} = \frac{(2, 0, 4)}{2} = (1, 0, 2).$$
Notice that:
$$M = P' = (1, 0, 2).$$
Now substitute $M = (1, 0, 2)$ into the plane equation $x + y + z = 3$:
$$\text{LHS} = 1 + 0 + 2 = 3.$$
$$\text{RHS} = 3.$$
$3 = 3$, which is true! The midpoint lies on the plane, verifying both the projection and the reflection.

## 5. Why Each Step Is Valid
- Moving along the normal vector $n$ guarantees that the displacement is perpendicular to the plane.
- The parameter value $t = -1$ uniquely solves the intersection condition, and $t = -2$ places $P''$ symmetrically at equal distance on the opposite side of the plane.

## 6. Final Answer in Words
The orthogonal projection is $P' = (1, 0, 2)$, and the reflection across the plane is $P'' = (0, -1, 1)$. The midpoint of the segment joining $P$ and $P''$ is $M = (1, 0, 2)$, which is identical to the projection $P'$ and satisfies the plane equation $1 + 0 + 2 = 3$, confirming the result.

## 7. Quick Verification
- Distance check:
  $d(P, P') = \|(2-1, 1-0, 3-2)\| = \|(1, 1, 1)\| = \sqrt{3}$.
  $d(P', P'') = \|(1-0, 0-(-1), 2-1)\| = \|(1, 1, 1)\| = \sqrt{3}$.
  Both distances are equal to $\sqrt{3}$, confirming perfect reflection symmetry.

## 8. Common Mistakes
- Miscalculating the reflection by using $t = +1$ instead of $t = -2$, moving further away from the plane instead of across it.
- Arithmetic sign errors when adding negative coordinates in the midpoint formula.

## 9. Short In-Class Explanation (3 Sentences)
We construct a line through $P(2, 1, 3)$ along the normal direction $(1, 1, 1)$ and find that it hits the plane at parameter $t = -1$, yielding the projection $P' = (1, 0, 2)$. Stepping twice as far to $t = -2$ gives the reflected point $P'' = (0, -1, 1)$. The midpoint of $P$ and $P''$ is $(1, 0, 2)$, which satisfies the plane equation $1 + 0 + 2 = 3$, verifying the symmetry of the reflection.
