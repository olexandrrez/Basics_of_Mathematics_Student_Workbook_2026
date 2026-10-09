# Problem 03: When Does the Inverse Not Exist?

## 1. Original Problem
For
$$A=\begin{pmatrix}2&4\\1&2\end{pmatrix}$$
explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## 2. What We Are Trying to Find
We must demonstrate why the matrix $A$ has no inverse using two complementary perspectives: algebraically via the determinant, and geometrically/linearly via the linear dependence of its rows.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Determinant Criterion**: An inverse matrix $A^{-1}$ exists if and only if $\det A \neq 0$. If $\det A = 0$, the inverse formula requires dividing by zero, which is impossible.
- **Row Dependence / Rank Criterion**: A matrix is invertible if and only if its rows are linearly independent and span the full space $\mathbb{R}^n$. If the rows are linearly dependent, the matrix has rank strictly less than $n$ and collapses space, losing information irreversibly.

## 4. Step-by-Step Solution

### Method 1: Using the Determinant
Compute the determinant of $A = \begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix}$:
$$\det A = (2)(2) - (4)(1) = 4 - 4 = 0.$$
- **Why this rules out the inverse**:
  If $A^{-1}$ existed, then by the product rule for determinants:
  $$\det(A A^{-1}) = \det(I) \implies \det(A) \cdot \det(A^{-1}) = 1.$$
  Substituting $\det A = 0$ gives:
  $$0 \cdot \det(A^{-1}) = 1,$$
  which has no solution in the real numbers ($0 = 1$ is a contradiction).
  Therefore, no inverse matrix can exist.

### Method 2: Using Dependence Between the Rows
Write out the rows of $A$:
$$R_1 = (2, 4),\qquad R_2 = (1, 2).$$
- Notice that:
  $$R_1 = 2 R_2 \quad \iff \quad R_1 - 2R_2 = (0, 0).$$
The rows are linearly dependent because the first row is an exact scalar multiple of the second row.
- **Why this rules out the inverse**:
  Because $R_1$ is proportional to $R_2$, the image of the linear transformation $T(x) = Ax$ is one-dimensional (a single line through the origin, $y = x/2$).
  Any vector not on this line has no pre-image (the transformation is not surjective).
  Furthermore, any non-zero vector $v = \begin{pmatrix} -2 \\ 1 \end{pmatrix}$ gives:
  $$Av = \begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} -4 + 4 \\ -2 + 2 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}.$$
  Since $Av = 0$ for a non-zero vector $v$, the transformation is not injective (it sends multiple points to zero).
  A function that is not bijective cannot have an inverse function.

## 5. Why Each Step Is Valid
- The determinant calculation $4 - 4 = 0$ is an exact algebraic evaluation.
- The existence of a non-trivial kernel (vectors mapped to zero) rigorously disproves injectivity, which is mandatory for any invertible operator.

## 6. Final Answer in Words
The inverse matrix $A^{-1}$ does not exist. First, its determinant is $(2)(2) - (4)(1) = 0$, which would require division by zero. Second, the first row is twice the second row ($R_1 = 2R_2$), meaning the rows are linearly dependent, the matrix collapses 2D space onto a 1D line, and distinct inputs are mapped to the same output.

## 7. Quick Verification
- Check columns as well: Column 2 is $\begin{pmatrix}4\\2\end{pmatrix} = 2 \begin{pmatrix}2\\1\end{pmatrix} = 2 \times$ Column 1. Both rows and columns are clearly dependent.
- If we tried Gaussian elimination: $R_1 \leftarrow R_1 - 2R_2$ yields a row of zeros $\begin{pmatrix}0&0\\1&2\end{pmatrix}$, making it impossible to produce the identity matrix on the left.

## 8. Common Mistakes
- Stating that $A^{-1}$ does not exist without explaining why $\det A = 0$ makes it impossible (i.e. $0 \cdot \det(A^{-1}) = 1$).
- Thinking that having non-zero entries prevents a matrix from being singular.

## 9. Short In-Class Explanation (3 Sentences)
First, the determinant of the matrix is $4 - 4 = 0$, and since an inverse exists only when the determinant is non-zero, $A^{-1}$ cannot exist. Second, the first row is exactly twice the second row, which means the rows are linearly dependent. This linear dependence collapses two-dimensional space onto a single line, making it impossible to reverse the transformation.
