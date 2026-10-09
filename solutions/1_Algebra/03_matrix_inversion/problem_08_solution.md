# Problem 08: Inverse of a Transformation

## 1. Original Problem
The matrix
$$S=\begin{pmatrix}2&0\\0&\frac12\end{pmatrix}$$
describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## 2. What We Are Trying to Find
We must find the inverse matrix $S^{-1}$ of a diagonal scaling matrix $S$, interpret the inverse transformation geometrically as undoing the scale factors along the coordinate axes, and verify this action on a test vector.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Inverse of a Diagonal Matrix**: For a diagonal matrix $D = \begin{pmatrix} d_1 & 0 \\ 0 & d_2 \end{pmatrix}$ with $d_1, d_2 \neq 0$, the inverse is formed by taking the reciprocal of each diagonal entry:
  $$D^{-1} = \begin{pmatrix} 1/d_1 & 0 \\ 0 & 1/d_2 \end{pmatrix}.$$
- **Geometric Interpretation of Inversion**: If a transformation stretches the $x$-axis by factor $k_1$ and compresses the $y$-axis by factor $k_2$, its inverse must compress the $x$-axis by $1/k_1$ and stretch the $y$-axis by $1/k_2$ to restore the original shape.

## 4. Step-by-Step Solution

### Step 1: Compute $S^{-1}$
The matrix is diagonal with diagonal entries $s_{11} = 2$ and $s_{22} = 1/2$.
Compute determinant:
$$\det S = (2)\left(\frac{1}{2}\right) - (0)(0) = 1.$$
Since $\det S = 1 \neq 0$, $S$ is invertible.
The reciprocals of the diagonal entries are:
$$\frac{1}{s_{11}} = \frac{1}{2},\qquad \frac{1}{s_{22}} = \frac{1}{1/2} = 2.$$
Therefore:
$$S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}.$$

### Step 2: Geometric Explanation of the Transformation
- The original transformation $S$:
  - Doubles the horizontal coordinate: $x \mapsto 2x$ (horizontal stretching by factor 2).
  - Halves the vertical coordinate: $y \mapsto \frac{1}{2}y$ (vertical compression by factor 2).
  - Notice that $\det S = 1$, which means $S$ is an area-preserving (hyperbolic) stretch.
- The inverse transformation $S^{-1}$:
  - Halves the horizontal coordinate: $x \mapsto \frac{1}{2}x$ (horizontal compression by factor 2).
  - Doubles the vertical coordinate: $y \mapsto 2y$ (vertical stretching by factor 2).
Geometrically, $S^{-1}$ completely undoes the distortion caused by $S$, restoring any stretched or squished shape back to its exact initial geometry and orientation.

### Step 3: Test on a Simple Vector
Choose the vector $v = \begin{pmatrix} 4 \\ 6 \end{pmatrix}$.
1. Apply the transformation $S$:
   $$w = Sv = \begin{pmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} 4 \\ 6 \end{pmatrix} = \begin{pmatrix} 2(4) \\ \frac{1}{2}(6) \end{pmatrix} = \begin{pmatrix} 8 \\ 3 \end{pmatrix}.$$
2. Apply the inverse transformation $S^{-1}$ to $w$:
   $$S^{-1} w = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 8 \\ 3 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(8) \\ 2(3) \end{pmatrix} = \begin{pmatrix} 4 \\ 6 \end{pmatrix} = v.$$
The composition $S^{-1}(Sv)$ successfully returns the initial vector $v$.

## 5. Why Each Step Is Valid
- For a diagonal matrix, coordinates decouple into independent 1D scalar scalings $x' = 2x$ and $y' = y/2$; inverting each equation independently gives $x = x'/2$ and $y = 2y'$.
- The identity $S^{-1} S v = I v = v$ holds for all vectors $v \in \mathbb{R}^2$.

## 6. Final Answer in Words
The inverse matrix is $S^{-1} = \begin{pmatrix} 1/2 & 0 \\ 0 & 2 \end{pmatrix}$. Geometrically, while $S$ doubles the $x$-coordinate and halves the $y$-coordinate, $S^{-1}$ does the exact opposite: it halves the $x$-coordinate and doubles the $y$-coordinate. Applying $S$ transforms $(4, 6)$ to $(8, 3)$, and applying $S^{-1}$ returns it to $(4, 6)$.

## 7. Quick Verification
- Check matrix product:
  $$S S^{-1} = \begin{pmatrix} 2 & 0 \\ 0 & 1/2 \end{pmatrix} \begin{pmatrix} 1/2 & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2(1/2) & 0 \\ 0 & (1/2)(2) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$$

## 8. Common Mistakes
- Negating the entries instead of taking reciprocals (writing $\begin{pmatrix}-2&0\\0&-1/2\end{pmatrix}$).
- Inverting the determinant rather than the individual scaling factors.

## 9. Short In-Class Explanation (3 Sentences)
Because $S$ is a diagonal matrix, its inverse is obtained by taking the reciprocals of the diagonal entries, giving $S^{-1} = \begin{pmatrix}1/2&0\\0&2\end{pmatrix}$. Geometrically, $S^{-1}$ reverses the action of $S$ by compressing the horizontal axis by 2 and stretching the vertical axis by 2. When applied to the test vector $(4, 6)^T$, $S$ transforms it to $(8, 3)^T$, and $S^{-1}$ maps it directly back to $(4, 6)^T$.
