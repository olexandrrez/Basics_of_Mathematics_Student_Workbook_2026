# Problem 09: Cross Product as a Perpendicular Direction

## 1. Original Problem
For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

## 2. What We Are Trying to Find
We must compute the cross product vector $u \times v$ in $\mathbb{R}^3$, verify that this vector is perpendicular to both original vectors $u$ and $v$ using the dot product, compute the reversed cross product $v \times u$, and analyze the anticommutative relationship between them.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Cross Product Definition**: For vectors in $\mathbb{R}^3$,
  $$u \times v = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{pmatrix} = (u_2 v_3 - u_3 v_2, u_3 v_1 - u_1 v_3, u_1 v_2 - u_2 v_1).$$
- **Geometric Orthogonality**: The cross product $u \times v$ produces a vector perpendicular to the plane containing $u$ and $v$:
  $$(u \times v) \cdot u = 0 \quad \text{and} \quad (u \times v) \cdot v = 0.$$
- **Anticommutativity**: Swapping the factors reverses the orientation by the right-hand rule:
  $$v \times u = -(u \times v).$$

## 4. Step-by-Step Solution

### Step 1: Compute $u \times v$
For $u = (1, 2, 0)$ and $v = (0, 1, 3)$:
$$u \times v = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & 0 \\ 0 & 1 & 3 \end{pmatrix}$$
- $\mathbf{i}$-component: $(2)(3) - (0)(1) = 6 - 0 = 6$.
- $\mathbf{j}$-component: $-[(1)(3) - (0)(0)] = -(3 - 0) = -3$.
- $\mathbf{k}$-component: $(1)(1) - (2)(0) = 1 - 0 = 1$.
Thus:
$$u \times v = (6, -3, 1).$$

### Step 2: Verify Perpendicularity Using Dot Products
1. Test with $u = (1, 2, 0)$:
   $$(u \times v) \cdot u = (6)(1) + (-3)(2) + (1)(0) = 6 - 6 + 0 = 0.$$
   Since the dot product is zero, $u \times v \perp u$.
2. Test with $v = (0, 1, 3)$:
   $$(u \times v) \cdot v = (6)(0) + (-3)(1) + (1)(3) = 0 - 3 + 3 = 0.$$
   Since the dot product is zero, $u \times v \perp v$.
The vector $(6, -3, 1)$ is strictly perpendicular to both $u$ and $v$.

### Step 3: Compute $v \times u$
For $v = (0, 1, 3)$ and $u = (1, 2, 0)$:
$$v \times u = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 0 & 1 & 3 \\ 1 & 2 & 0 \end{pmatrix}$$
- $\mathbf{i}$-component: $(1)(0) - (3)(2) = 0 - 6 = -6$.
- $\mathbf{j}$-component: $-[(0)(0) - (3)(1)] = -(0 - 3) = +3$.
- $\mathbf{k}$-component: $(0)(2) - (1)(1) = 0 - 1 = -1$.
Thus:
$$v \times u = (-6, 3, -1).$$

### Step 4: Compare the Results
Comparing the two vectors:
$$v \times u = (-6, 3, -1) = -(6, -3, 1) = -(u \times v).$$
The vector $v \times u$ has the exact same magnitude and lies along the exact same line in space, but points in the **opposite direction**.
This confirms that the cross product is **anticommutative**: changing the order of arguments reverses the sign of the result.

## 5. Why Each Step Is Valid
- Expanding the symbolic $3 \times 3$ determinant evaluates the standard vector cross product.
- $(u \times v) \cdot u = \det[u, u, v] = 0$ because a determinant with two identical rows is identically zero.
- Swapping the two rows in the determinant definition multiplies the result by $-1$.

## 6. Final Answer in Words
The cross product is $u \times v = (6, -3, 1)$. The dot products $(u \times v) \cdot u = 0$ and $(u \times v) \cdot v = 0$ confirm that it is perpendicular to both original vectors. The reversed product is $v \times u = (-6, 3, -1) = -(u \times v)$, demonstrating that the cross product is anticommutative.

## 7. Quick Verification
- Length of cross product: $\|u \times v\| = \sqrt{6^2 + (-3)^2 + 1^2} = \sqrt{36 + 9 + 1} = \sqrt{46}$.
  $\|v \times u\| = \sqrt{(-6)^2 + 3^2 + (-1)^2} = \sqrt{36 + 9 + 1} = \sqrt{46}$.
  Magnitudes are equal, confirming pure direction reversal.

## 8. Common Mistakes
- Forgetting the negative sign on the $\mathbf{j}$-component cofactor: $-[(1)(3) - (0)(0)] = -3$.
- Assuming the cross product is commutative and writing $v \times u = u \times v$.

## 9. Short In-Class Explanation (3 Sentences)
We compute $u \times v = (6, -3, 1)$ using the standard 3D determinant formula. Computing its dot products with $u$ and $v$ yields $6 - 6 = 0$ and $-3 + 3 = 0$, confirming that it is perpendicular to both vectors. Reversing the order yields $v \times u = (-6, 3, -1)$, which shows that swapping the vectors points the cross product in the opposite direction.
