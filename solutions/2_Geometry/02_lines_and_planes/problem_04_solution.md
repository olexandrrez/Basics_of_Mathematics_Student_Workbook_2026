# Problem 04: Plane Through Three Points

## 1. Original Problem
Find the equation of the plane through
$$A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).$$
First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## 2. What We Are Trying to Find
We must determine the Cartesian equation of the plane passing through the three standard intercept points $A, B, C$ by constructing two direction vectors within the plane, finding a normal vector using their cross product, and verifying the equation on all three points.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Two Coplanar Direction Vectors**: $\overrightarrow{AB} = B - A$ and $\overrightarrow{AC} = C - A$.
- **Normal Vector via Cross Product**: Since both vectors lie in the plane, their cross product is perpendicular to both, providing a normal vector:
  $$n = \overrightarrow{AB} \times \overrightarrow{AC}.$$
- **Equation of Plane**: $n \cdot (X - A) = 0$.

## 4. Step-by-Step Solution

### Step 1: Construct Two Vectors Lying in the Plane
Using $A = (1, 0, 0)$ as the base point:
- $\overrightarrow{AB} = B - A = (0 - 1, 1 - 0, 0 - 0) = (-1, 1, 0)$.
- $\overrightarrow{AC} = C - A = (0 - 1, 0 - 0, 1 - 0) = (-1, 0, 1)$.

### Step 2: Compute the Normal Vector via Cross Product
$$n = \overrightarrow{AB} \times \overrightarrow{AC} = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{pmatrix}$$
- $\mathbf{i}$-component: $(1)(1) - (0)(0) = 1 - 0 = 1$.
- $\mathbf{j}$-component: $-[(-1)(1) - (0)(-1)] = -[-1 - 0] = 1$.
- $\mathbf{k}$-component: $(-1)(0) - (1)(-1) = 0 - (-1) = 1$.
Thus:
$$n = (1, 1, 1).$$

### Step 3: Write the Equation of the Plane
Using normal vector $n = (1, 1, 1)$ and base point $A = (1, 0, 0)$:
$$1(x - 1) + 1(y - 0) + 1(z - 0) = 0 \implies x - 1 + y + z = 0 \implies x + y + z = 1.$$

### Step 4: Check on All Three Points
1. Point $A=(1, 0, 0)$:
   $$1 + 0 + 0 = 1. \quad (\text{True})$$
2. Point $B=(0, 1, 0)$:
   $$0 + 1 + 0 = 1. \quad (\text{True})$$
3. Point $C=(0, 0, 1)$:
   $$0 + 0 + 1 = 1. \quad (\text{True})$$
All three points satisfy the equation $x + y + z = 1$.

## 5. Why Each Step Is Valid
- Vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are linearly independent because their ratio is not constant.
- The cross product produces a vector strictly orthogonal to the 2D subspace spanned by the edge vectors.
- A plane in $\mathbb{R}^3$ is uniquely determined by three non-collinear points.

## 6. Final Answer in Words
The direction vectors are $\overrightarrow{AB} = (-1, 1, 0)$ and $\overrightarrow{AC} = (-1, 0, 1)$, giving the normal vector $n = (1, 1, 1)$. The equation of the plane is $x + y + z = 1$ (or $x + y + z - 1 = 0$). Substituting points $A(1, 0, 0)$, $B(0, 1, 0)$, and $C(0, 0, 1)$ yields $1 = 1$ in all three cases, verifying the equation.

## 7. Quick Verification
- Intercept form of a plane: $\frac{x}{a} + \frac{y}{b} + \frac{z}{c} = 1$, where $a, b, c$ are the axis intercepts.
  Here the intercepts are $a = 1, b = 1, c = 1$.
  The intercept equation immediately gives:
  $$\frac{x}{1} + \frac{y}{1} + \frac{z}{1} = 1 \iff x + y + z = 1.$$
  This provides an instantaneous check of the result.

## 8. Common Mistakes
- Negating components in the cross product incorrectly (e.g., getting $-1$ for the $\mathbf{j}$ or $\mathbf{k}$ component).
- Testing only point $A$ and neglecting to verify $B$ and $C$.

## 9. Short In-Class Explanation (3 Sentences)
We construct direction vectors $\overrightarrow{AB} = (-1, 1, 0)$ and $\overrightarrow{AC} = (-1, 0, 1)$ and compute their cross product to find the normal vector $n = (1, 1, 1)$. Using the point-normal formula with point $A$ produces the symmetric plane equation $x + y + z = 1$. Testing points $A$, $B$, and $C$ into this equation gives $1=1$ in all three cases, confirming that the plane contains all three points.
