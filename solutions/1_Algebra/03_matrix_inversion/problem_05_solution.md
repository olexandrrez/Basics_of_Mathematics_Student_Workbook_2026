# Problem 05: A 3×3 Matrix

## 1. Original Problem
Use Gauss–Jordan elimination to find the inverse of
$$A=\begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix}.$$
Check the result by multiplication.

## 2. What We Are Trying to Find
We must find the inverse of a $3 \times 3$ cyclic matrix $A$ using full Gauss-Jordan elimination on the augmented matrix $[A \mid I]$ and verify the resulting inverse by multiplying it by $A$ to obtain $I$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Gauss-Jordan for $3 \times 3$**: We form $[A \mid I_3]$ and use row operations to reach reduced row echelon form $[I_3 \mid A^{-1}]$.
- **Checking by Multiplication**: $A A^{-1} = I$ is a necessary and sufficient check for correctness.

## 4. Step-by-Step Solution

### Step 1: Set Up the Augmented Matrix
$$[A \mid I] = \left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right].$$

### Step 2: Clear Below the First Pivot
Row 1 pivot is $a_{11}=1$. Entry $a_{21}=0$ is already zero. Eliminate $a_{31}=1$ using $R_3 \leftarrow R_3 - R_1$:
- Left: $(1, 0, 1) - (1, 1, 0) = (0, -1, 1)$.
- Right: $(0, 0, 1) - (1, 0, 0) = (-1, 0, 1)$.
$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right].$$

### Step 3: Clear Below the Second Pivot
Row 2 pivot is $a_{22}=1$. Eliminate $a_{32}=-1$ using $R_3 \leftarrow R_3 + R_2$:
- Left: $(0, -1, 1) + (0, 1, 1) = (0, 0, 2)$.
- Right: $(-1, 0, 1) + (0, 1, 0) = (-1, 1, 1)$.
$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right].$$

### Step 4: Scale Row 3 to Make Pivot 1
Perform $R_3 \leftarrow \frac{1}{2} R_3$:
$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right].$$

### Step 5: Clear Above the Third Pivot
Eliminate $a_{23}=1$ using $R_2 \leftarrow R_2 - R_3$:
- Left: $(0, 1, 1) - (0, 0, 1) = (0, 1, 0)$.
- Right: $(0, 1, 0) - (-1/2, 1/2, 1/2) = (1/2, 1/2, -1/2)$.
$$\left[\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 1/2 & 1/2 & -1/2 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right].$$

### Step 6: Clear Above the Second Pivot
Eliminate $a_{12}=1$ using $R_1 \leftarrow R_1 - R_2$:
- Left: $(1, 1, 0) - (0, 1, 0) = (1, 0, 0)$.
- Right: $(1, 0, 0) - (1/2, 1/2, -1/2) = (1/2, -1/2, 1/2)$.
$$\left[\begin{array}{ccc|ccc} 1 & 0 & 0 & 1/2 & -1/2 & 1/2 \\ 0 & 1 & 0 & 1/2 & 1/2 & -1/2 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right].$$

The left side is $I_3$. The inverse is:
$$A^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}.$$

### Step 7: Check by Multiplication
Multiply $A$ by $A^{-1}$:
$$A A^{-1} = \begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix} \cdot \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}$$
- Row 1: $\frac{1}{2} (1(1)+1(1)+0(-1), 1(-1)+1(1)+0(1), 1(1)+1(-1)+0(1)) = \frac{1}{2}(2, 0, 0) = (1, 0, 0)$.
- Row 2: $\frac{1}{2} (0(1)+1(1)+1(-1), 0(-1)+1(1)+1(1), 0(1)+1(-1)+1(1)) = \frac{1}{2}(0, 2, 0) = (0, 1, 0)$.
- Row 3: $\frac{1}{2} (1(1)+0(1)+1(-1), 1(-1)+0(1)+1(1), 1(1)+0(-1)+1(1)) = \frac{1}{2}(0, 0, 2) = (0, 0, 1)$.
Thus $A A^{-1} = I$, confirming the inverse.

## 5. Why Each Step Is Valid
- Gauss-Jordan elimination applies a sequence of elementary row operations that systematically clear off-diagonal entries.
- The existence of non-zero pivots at every diagonal position confirms that the matrix has full rank ($3$) and is invertible.

## 6. Final Answer in Words
The inverse matrix is $A^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}$. Multiplying $A$ by $A^{-1}$ yields the $3 \times 3$ identity matrix, verifying the calculation.

## 7. Quick Verification
- Compute $\det A$: Sarrus rule gives $1(1)(1) + 1(1)(1) + 0 - (0 + 0 + 0) = 2$.
  $\det(A^{-1}) = (1/2)^3 \det\begin{pmatrix}1&-1&1\\1&1&-1\\-1&1&1\end{pmatrix} = \frac{1}{8} [1(2) - (-1)(0) + 1(2)] = \frac{1}{8}(4) = 1/2$.
  Since $\det(A^{-1}) = 1/\det A = 1/2$, the determinant check passes.

## 8. Common Mistakes
- Forgetting to scale Row 3 by $1/2$ before back-substituting, which leads to arithmetic errors in $R_2$ and $R_1$.
- Sign confusion when subtracting fractional rows: $0 - (-1/2) = +1/2$.

## 9. Short In-Class Explanation (3 Sentences)
We set up the augmented matrix $[A \mid I]$ and use row operations to eliminate entries below and then above the main diagonal until the left block becomes the identity matrix. Scaling the third row by $1/2$ produces the fractional entries on the right-hand side. Multiplying the original matrix $A$ by our resulting matrix gives the identity matrix $I$, confirming the inverse.
