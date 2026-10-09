# Problem 10: Inverse of a Diagonal Matrix

## 1. Original Problem
Given
$$D=\begin{pmatrix}2&0&0\\0&-3&0\\0&0&5\end{pmatrix},\qquad E=\begin{pmatrix}2&0&0\\0&0&0\\0&0&5\end{pmatrix}.$$
Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## 2. What We Are Trying to Find
We must determine which of the two diagonal matrices ($D$ or $E$) is invertible by inspecting their structure, provide the explicit inverse for the invertible matrix, and verify it by matrix multiplication.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Invertibility of Diagonal Matrices**: A diagonal matrix $\operatorname{diag}(d_1, d_2, \dots, d_n)$ is invertible if and only if **all** of its diagonal entries are non-zero:
  $$\det(\operatorname{diag}(d_1, \dots, d_n)) = d_1 d_2 \dots d_n \neq 0 \iff d_i \neq 0 \quad \forall i.$$
- **Inverse of a Diagonal Matrix**: If all $d_i \neq 0$, the inverse is simply the diagonal matrix of the reciprocals:
  $$\operatorname{diag}(d_1, d_2, \dots, d_n)^{-1} = \operatorname{diag}\left(\frac{1}{d_1}, \frac{1}{d_2}, \dots, \frac{1}{d_n}\right).$$
- If any diagonal entry is zero, the determinant is zero and an entire coordinate axis is annihilated to zero, making inversion impossible.

## 4. Step-by-Step Solution

### Step 1: Analyze Matrix $D$
Matrix $D = \begin{pmatrix} 2 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 5 \end{pmatrix}$.
- Diagonal entries are $d_1 = 2$, $d_2 = -3$, and $d_3 = 5$.
- None of the diagonal entries are zero.
- Determinant: $\det D = 2 \cdot (-3) \cdot 5 = -30 \neq 0$.
- **Conclusion**: Matrix $D$ is **invertible**.

### Step 2: Analyze Matrix $E$
Matrix $E = \begin{pmatrix} 2 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 5 \end{pmatrix}$.
- The second diagonal entry is $e_{22} = 0$.
- The second row is a row of all zeros $(0, 0, 0)$.
- Determinant: $\det E = 2 \cdot 0 \cdot 5 = 0$.
- **Conclusion**: Matrix $E$ is **not invertible** (it is singular).

### Step 3: Compute the Inverse of Matrix $D$
Take the reciprocals of the diagonal entries:
$$\frac{1}{d_1} = \frac{1}{2},\qquad \frac{1}{d_2} = -\frac{1}{3},\qquad \frac{1}{d_3} = \frac{1}{5}.$$
Thus:
$$D^{-1} = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\ 0 & -\frac{1}{3} & 0 \\ 0 & 0 & \frac{1}{5} \end{pmatrix}.$$

### Step 4: Check by Multiplication
Multiply $D$ by $D^{-1}$:
$$D D^{-1} = \begin{pmatrix} 2 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 5 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 & 0 \\ 0 & -\frac{1}{3} & 0 \\ 0 & 0 & \frac{1}{5} \end{pmatrix} = \begin{pmatrix} 2\left(\frac{1}{2}\right) & 0 & 0 \\ 0 & (-3)\left(-\frac{1}{3}\right) & 0 \\ 0 & 0 & 5\left(\frac{1}{5}\right) \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I.$$
The product is the $3 \times 3$ identity matrix.

## 5. Why Each Step Is Valid
- For diagonal matrices, multiplying corresponding diagonal entries directly evaluates the product matrix entries.
- The reciprocal of a non-zero real number $x$ uniquely solves $x \cdot (1/x) = 1$.
- Having a zero diagonal entry in $E$ means that the basis vector $e_2$ maps to $0$, creating a non-trivial kernel and preventing injectivity.

## 6. Final Answer in Words
Matrix $D$ is invertible because all of its diagonal entries are non-zero (giving $\det D = -30$), whereas matrix $E$ is not invertible because it contains a zero on the diagonal (giving $\det E = 0$ and a row of zeros). The inverse of $D$ is $D^{-1} = \operatorname{diag}(1/2, -1/3, 1/5)$, and multiplying $D$ by $D^{-1}$ yields the identity matrix.

## 7. Quick Verification
- Check determinant: $\det(D^{-1}) = (1/2)(-1/3)(1/5) = -1/30 = 1/\det(D)$.
- Multiplication in reverse order: $D^{-1} D = \operatorname{diag}((1/2)2, (-1/3)(-3), (1/5)5) = \operatorname{diag}(1, 1, 1) = I$.

## 8. Common Mistakes
- Attempting to take the reciprocal of 0 for matrix $E$, claiming $1/0$ is part of an inverse.
- Using full Gauss-Jordan elimination when the diagonal structure allows the answer to be written down by inspection.

## 9. Short In-Class Explanation (3 Sentences)
A diagonal matrix is invertible if and only if all of its diagonal entries are non-zero, which means $D$ is invertible while $E$ is not because of the zero in its second row. For matrix $D$, the inverse is obtained immediately by replacing each diagonal entry with its reciprocal, giving $\operatorname{diag}(1/2, -1/3, 1/5)$. Multiplying $D$ by this inverse yields the identity matrix, confirming the result.
