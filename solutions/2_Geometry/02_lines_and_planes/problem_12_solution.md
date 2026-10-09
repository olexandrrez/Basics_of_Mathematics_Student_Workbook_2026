# Problem 12: Intersection Line of Two Planes

## 1. Original Problem
Find a parametric equation of the line that is the intersection of
$$x+y+z=3,\qquad x-y+z=1.$$
Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## 2. What We Are Trying to Find
We must determine the parametric equations of the line formed by the intersection of two non-parallel planes, find its direction vector using Gaussian elimination and using the cross product of the normal vectors, and compare the two approaches.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Intersection Line as a Linear System**: The intersection line consists of all points $(x, y, z)$ simultaneously satisfying both plane equations. Since there are 2 equations and 3 variables, setting one variable as a free parameter yields the parametric form of the line.
- **Direction via Cross Product**: The intersection line lies entirely within both planes. Therefore, its direction vector $v$ must be perpendicular to both normal vectors $n_1$ and $n_2$:
  $$v = n_1 \times n_2.$$

## 4. Step-by-Step Solution

### Step 1: Method 1 — Solve the System of Equations
Given the system:
$$\begin{cases} (1) \quad x + y + z = 3, \\ (2) \quad x - y + z = 1. \end{cases}$$
1. Add the two equations:
   $$(x + y + z) + (x - y + z) = 3 + 1 \implies 2x + 2z = 4 \implies x + z = 2 \implies x = 2 - z.$$
2. Subtract Equation (2) from Equation (1):
   $$(x + y + z) - (x - y + z) = 3 - 1 \implies 2y = 2 \implies y = 1.$$
3. Set $z = t$ as the free parameter ($t \in \mathbb{R}$):
   $$\begin{cases} x = 2 - t, \\ y = 1, \\ z = t. \end{cases}$$
In vector form:
$$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}.$$
From this algebraic method, the base point is $P_0 = (2, 1, 0)$ and the direction vector is:
$$v_{\text{alg}} = (-1, 0, 1).$$

### Step 2: Method 2 — Using the Cross Product of Normal Vectors
From the plane equations:
- Plane 1: $x + y + z = 3 \implies n_1 = (1, 1, 1)$.
- Plane 2: $x - y + z = 1 \implies n_2 = (1, -1, 1)$.

Compute the cross product $n_1 \times n_2$:
$$v_{\text{geom}} = n_1 \times n_2 = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & 1 \\ 1 & -1 & 1 \end{pmatrix}$$
- $\mathbf{i}$-component: $(1)(1) - (1)(-1) = 1 - (-1) = 1 + 1 = 2$.
- $\mathbf{j}$-component: $-[(1)(1) - (1)(1)] = -(1 - 1) = 0$.
- $\mathbf{k}$-component: $(1)(-1) - (1)(1) = -1 - 1 = -2$.
Thus:
$$v_{\text{geom}} = (2, 0, -2).$$

### Step 3: Compare the Results
Comparing the two direction vectors:
$$v_{\text{geom}} = (2, 0, -2) = -2(-1, 0, 1) = -2 v_{\text{alg}}.$$
The two vectors are **scalar multiples of each other** (proportional with factor $-2$).
Because any non-zero scalar multiple of a direction vector describes the exact same straight line in space (simply reparameterizing the speed and orientation along the line), both methods produce the identical direction for the line.

## 5. Why Each Step Is Valid
- The solution space of an underdetermined consistent $2 \times 3$ system is an affine line.
- The cross product of two planes' normals is orthogonal to both normals, and any vector orthogonal to both normals is tangent to both planes, meaning it must lie along their line of intersection.

## 6. Final Answer in Words
The parametric equation of the intersection line is $(x, y, z) = (2, 1, 0) + t(-1, 0, 1)$ for $t \in \mathbb{R}$. The algebraic method gives direction vector $(-1, 0, 1)$, while the cross product of the normal vectors gives $(2, 0, -2)$. These results are identical because $(2, 0, -2) = -2(-1, 0, 1)$, confirming that both vectors point along the same line.

## 7. Quick Verification
- Check base point $(2, 1, 0)$ in both planes:
  Plane 1: $2 + 1 + 0 = 3$. (Matches)
  Plane 2: $2 - 1 + 0 = 1$. (Matches)
- Check direction vector $(-1, 0, 1)$ against both normals:
  $(-1, 0, 1) \cdot (1, 1, 1) = -1 + 0 + 1 = 0$.
  $(-1, 0, 1) \cdot (1, -1, 1) = -1 + 0 + 1 = 0$.
  The direction is strictly contained in both planes.

## 8. Common Mistakes
- Thinking that $(-1, 0, 1)$ and $(2, 0, -2)$ are different answers, forgetting that direction vectors are defined up to non-zero scalar multiples.
- Failing to find a base point when using the cross product method.

## 9. Short In-Class Explanation (3 Sentences)
Adding and subtracting the two plane equations eliminates variables to give $x = 2 - z$ and $y = 1$, yielding the parametric line $(2, 1, 0) + t(-1, 0, 1)$. Taking the cross product of the plane normals $(1, 1, 1) \times (1, -1, 1)$ gives the direction vector $(2, 0, -2)$. These two results match because $(2, 0, -2)$ is simply $-2$ times $(-1, 0, 1)$, representing the same direction in space.
