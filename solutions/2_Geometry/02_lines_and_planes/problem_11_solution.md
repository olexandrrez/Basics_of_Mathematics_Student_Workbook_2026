# Problem 11: Plane Containing a Line and a Point

## 1. Original Problem
Find the equation of the plane containing
$$(x,y,z)=(1,0,2)+t(1,1,-1)$$
and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

## 2. What We Are Trying to Find
We must construct the Cartesian equation of the plane containing a given line $L$ and an external point $P$, and verify the derived equation by demonstrating that point $P$ and all points on line $L$ for every parameter $t$ satisfy the equation.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Two Non-Collinear Vectors in the Plane**:
  1. The direction vector of the line: $v = (1, 1, -1)$.
  2. The displacement vector connecting the line's base point $P_0 = (1, 0, 2)$ to the external point $P = (0, 2, 1)$: $u = P - P_0$.
- **Normal Vector via Cross Product**:
  $$n = v \times u.$$
- **Point-Normal Plane Equation**: $n \cdot (X - P) = 0$.

## 4. Step-by-Step Solution

### Step 1: Extract Base Point and Direction Vector of the Line
From $L: (x, y, z) = (1, 0, 2) + t(1, 1, -1)$:
- Base point: $P_0 = (1, 0, 2)$.
- Direction vector: $v = (1, 1, -1)$.

### Step 2: Construct the Connecting Vector $u$
Subtract $P_0$ from $P = (0, 2, 1)$:
$$u = P - P_0 = (0 - 1, 2 - 0, 1 - 2) = (-1, 2, -1).$$

### Step 3: Compute the Normal Vector $n = v \times u$
Compute the cross product:
$$n = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & -1 \\ -1 & 2 & -1 \end{pmatrix}$$
- $\mathbf{i}$-component: $(1)(-1) - (-1)(2) = -1 - (-2) = -1 + 2 = 1$.
- $\mathbf{j}$-component: $-[(1)(-1) - (-1)(-1)] = -[-1 - 1] = -(-2) = 2$.
- $\mathbf{k}$-component: $(1)(2) - (1)(-1) = 2 - (-1) = 2 + 1 = 3$.
Thus:
$$n = (1, 2, 3).$$

### Step 4: Write the Cartesian Equation of the Plane
Using normal vector $n = (1, 2, 3)$ and point $P = (0, 2, 1)$:
$$1(x - 0) + 2(y - 2) + 3(z - 1) = 0.$$
Expand and simplify:
$$x + 2y - 4 + 3z - 3 = 0 \implies x + 2y + 3z - 7 = 0 \implies x + 2y + 3z = 7.$$

### Step 5: Check That Point $P$ and the Entire Line Lie in the Plane
1. **Check Point $P(0, 2, 1)$**:
   $$0 + 2(2) + 3(1) = 0 + 4 + 3 = 7.$$
   $7 = 7$, True! Point $P$ lies in the plane.
2. **Check the Entire Line**:
   A general point on line $L$ is $(x(t), y(t), z(t)) = (1 + t, t, 2 - t)$.
   Substitute into the plane equation $x + 2y + 3z = 7$:
   $$(1 + t) + 2(t) + 3(2 - t) = 1 + t + 2t + 6 - 3t = (1 + 6) + (t + 2t - 3t) = 7 + 0t = 7.$$
   The equation $7 = 7$ holds for **all real numbers $t$**.
This proves that every single point of line $L$ lies within the plane.

## 5. Why Each Step Is Valid
- Vectors $v$ and $u$ are non-parallel, ensuring their cross product is non-zero.
- The condition $n \cdot v = 0$ guarantees the plane is parallel to $L$, and $P_0 \in \Pi$ guarantees the plane contains $L$.

## 6. Final Answer in Words
The equation of the plane is $x + 2y + 3z = 7$ (or $x + 2y + 3z - 7 = 0$). Point $P(0, 2, 1)$ satisfies the equation since $0 + 4 + 3 = 7$. Substituting the parametric line coordinates $(1+t, t, 2-t)$ yields $7 = 7$ identically for all $t$, confirming that the entire line lies in the plane.

## 7. Quick Verification
- Check base point $P_0(1, 0, 2)$ directly:
  $$1 + 2(0) + 3(2) = 1 + 0 + 6 = 7.$$
  Matches.
- Check normal perpendicularity:
  $n \cdot v = (1, 2, 3) \cdot (1, 1, -1) = 1 + 2 - 3 = 0$.
  $n \cdot u = (1, 2, 3) \cdot (-1, 2, -1) = -1 + 4 - 3 = 0$.
  Both dot products equal zero.

## 8. Common Mistakes
- Misidentifying the vector $u$: taking $P$ itself instead of $P - P_0$.
- Sign errors when expanding the cross product for the $\mathbf{j}$ term.

## 9. Short In-Class Explanation (3 Sentences)
We take the line's direction vector $v = (1, 1, -1)$ and the connecting vector $u = P - P_0 = (-1, 2, -1)$ and compute their cross product to get the normal vector $n = (1, 2, 3)$. Using point $P(0, 2, 1)$ yields the plane equation $x + 2y + 3z = 7$. Substituting the parametric equations of the line simplifies to $7 = 7$ for all $t$, proving that the plane contains both the point and the entire line.
