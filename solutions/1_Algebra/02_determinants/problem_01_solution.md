# Problem 01: Determinant of a 2×2 Matrix

## 1. Original Problem
Compute
$$\det\begin{pmatrix}3&-2\\5&4\end{pmatrix},\qquad \det\begin{pmatrix}1&7\\2&14\end{pmatrix}.$$
Which matrix is invertible? Justify your answer.

## 2. What We Are Trying to Find
We need to calculate the determinants of two given $2 \times 2$ matrices using the standard formula and use the determinant invertibility criterion to determine which matrix has an inverse.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Determinant of a $2 \times 2$ Matrix**: For a matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is defined as:
  $$\det M = ad - bc.$$
- **Invertibility Criterion**: A square matrix $M$ is invertible if and only if $\det M \neq 0$. If $\det M = 0$, the matrix is singular (non-invertible).

## 4. Step-by-Step Solution

### Step 1: Compute the First Determinant
Let $A = \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$.
Using the formula $ad - bc$ with $a=3, b=-2, c=5, d=4$:
$$\det A = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22.$$

### Step 2: Compute the Second Determinant
Let $B = \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$.
Using the formula $ad - bc$ with $a=1, b=7, c=2, d=14$:
$$\det B = (1)(14) - (7)(2) = 14 - 14 = 0.$$

### Step 3: Determine Invertibility
- For matrix $A$: Since $\det A = 22 \neq 0$, matrix $A$ is invertible.
- For matrix $B$: Since $\det B = 0$, matrix $B$ is not invertible (it is singular).

## 5. Why Each Step Is Valid
- The $2 \times 2$ determinant formula measures the oriented area spanned by the column vectors; when it is non-zero, the columns are linearly independent, guaranteeing that the linear map is bijective and thus invertible.
- In matrix $B$, the second row $(2, 14)$ is exactly twice the first row $2 \times (1, 7)$, which causes the rows to be linearly dependent and makes the determinant collapse to zero.

## 6. Final Answer in Words
The determinant of the first matrix is $22$, and the determinant of the second matrix is $0$. The first matrix is invertible because its determinant is non-zero, while the second matrix is not invertible because its determinant is zero.

## 7. Quick Verification
- Check row dependence in $B$: $R_2 - 2R_1 = (2, 14) - (2, 14) = (0, 0)$. A zero row confirms $\det B = 0$.
- Formula check for $A$: $3(4) = 12$, $(-2)(5) = -10$, $12 - (-10) = 22$. Arithmetic is solid.

## 8. Common Mistakes
- Sign errors when subtracting a negative product: writing $12 - 10 = 2$ instead of $12 - (-10) = 22$.
- Confusing the condition for invertibility (thinking $\det M = 0$ means invertible).

## 9. Short In-Class Explanation (3 Sentences)
We compute the determinants using the formula $ad - bc$, which yields $22$ for the first matrix and $0$ for the second matrix. By the invertibility theorem, a square matrix has an inverse if and only if its determinant is non-zero. Therefore, only the first matrix is invertible, while the second is singular because its second row is a direct multiple of its first row.
