# Problem 12: A Normal Vector to a Plane

## 1. Original Problem
Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

## 2. What We Are Trying to Find
We must construct two displacement vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ lying in the plane defined by points $A, B, C$, compute a normal vector $n$ perpendicular to both vectors using the cross product, and verify the perpendicularity using dot products.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Vectors in a Plane**: The vectors $\overrightarrow{AB} = B - A$ and $\overrightarrow{AC} = C - A$ lie entirely within the plane passing through $A, B, C$.
- **Normal Vector Construction**: The cross product of two non-parallel vectors in a plane produces a **normal vector** $n$ perpendicular to the entire plane:
  $$n = \overrightarrow{AB} \times \overrightarrow{AC}.$$
- **Perpendicularity Check**: $n \cdot \overrightarrow{AB} = 0$ and $n \cdot \overrightarrow{AC} = 0$.

## 4. Step-by-Step Solution

### Step 1: Construct Two Vectors Lying in the Plane
Using point $A=(1, 0, 2)$ as the base point:
- Vector $\overrightarrow{AB} = B - A = (2 - 1, 1 - 0, 0 - 2) = (1, 1, -2)$.
- Vector $\overrightarrow{AC} = C - A = (0 - 1, 3 - 0, 1 - 2) = (-1, 3, -1)$.

### Step 2: Compute the Normal Vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$
Set up the cross product:
$$n = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & -2 \\ -1 & 3 & -1 \end{pmatrix}$$
- $\mathbf{i}$-component: $(1)(-1) - (-2)(3) = -1 - (-6) = -1 + 6 = 5$.
- $\mathbf{j}$-component: $-[(1)(-1) - (-2)(-1)] = -[-1 - 2] = -(-3) = 3$.
- $\mathbf{k}$-component: $(1)(3) - (1)(-1) = 3 - (-1) = 3 + 1 = 4$.
Thus:
$$n = (5, 3, 4).$$

### Step 3: Check Perpendicularity Using Dot Products
1. Test with $\overrightarrow{AB} = (1, 1, -2)$:
   $$n \cdot \overrightarrow{AB} = (5)(1) + (3)(1) + (4)(-2) = 5 + 3 - 8 = 0.$$
   Since the dot product is zero, $n \perp \overrightarrow{AB}$.
2. Test with $\overrightarrow{AC} = (-1, 3, -1)$:
   $$n \cdot \overrightarrow{AC} = (5)(-1) + (3)(3) + (4)(-1) = -5 + 9 - 4 = 0.$$
   Since the dot product is zero, $n \perp \overrightarrow{AC}$.

Both dot products evaluate to zero, confirming that $n = (5, 3, 4)$ is strictly perpendicular to both direction vectors in the plane.

## 5. Why Each Step Is Valid
- Subtracting point coordinates constructs valid vectors parallel to the plane.
- The cross product of two linearly independent vectors in $\mathbb{R}^3$ generates a vector orthogonal to the plane spanned by them.

## 6. Final Answer in Words
The two vectors in the plane are $\overrightarrow{AB} = (1, 1, -2)$ and $\overrightarrow{AC} = (-1, 3, -1)$. A normal vector perpendicular to both is $n = (5, 3, 4)$. The dot products $n \cdot \overrightarrow{AB} = 5 + 3 - 8 = 0$ and $n \cdot \overrightarrow{AC} = -5 + 9 - 4 = 0$ confirm that $n$ is perpendicular to both vectors.

## 7. Quick Verification
- Test with third side vector $\overrightarrow{BC} = C - B = (0 - 2, 3 - 1, 1 - 0) = (-2, 2, 1)$:
  $$n \cdot \overrightarrow{BC} = (5)(-2) + (3)(2) + (4)(1) = -10 + 6 + 4 = 0.$$
  $n$ is perpendicular to all three edges of the triangle formed by $A, B, C$.
- Equation of the plane through $A$: $5(x - 1) + 3(y - 0) + 4(z - 2) = 0 \implies 5x + 3y + 4z = 13$.
  Check $B$: $5(2) + 3(1) + 4(0) = 13$ (Matches). Check $C$: $5(0) + 3(3) + 4(1) = 13$ (Matches).

## 8. Common Mistakes
- Sign errors when expanding the determinants for the cross product (e.g., forgetting the negative sign on the $\mathbf{j}$ minor).
- Misidentifying vector components by subtracting $A$ from coordinates backwards.

## 9. Short In-Class Explanation (3 Sentences)
We form the direction vectors $\overrightarrow{AB} = (1, 1, -2)$ and $\overrightarrow{AC} = (-1, 3, -1)$ by subtracting the coordinates of point $A$ from $B$ and $C$. Computing their cross product gives the normal vector $n = (5, 3, 4)$. Evaluating the dot products $n \cdot \overrightarrow{AB} = 0$ and $n \cdot \overrightarrow{AC} = 0$ confirms that $n$ is perpendicular to both vectors and therefore normal to the entire plane.
