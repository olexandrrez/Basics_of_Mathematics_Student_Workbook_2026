# Problem 01: Definition of the Inverse

## 1. Original Problem
For
$$A=\begin{pmatrix}2&1\\1&1\end{pmatrix},\qquad B=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$$
check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## 2. What We Are Trying to Find
We must determine if matrix $B$ is the multiplicative inverse of matrix $A$ directly from first principles by computing the two products $AB$ and $BA$ and checking whether both products equal the identity matrix $I$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Definition of the Inverse Matrix**: An $n \times n$ matrix $B$ is the inverse of $A$ (written $B = A^{-1}$) if and only if:
  $$AB = I \quad \text{and} \quad BA = I,$$
  where $I$ is the $n \times n$ identity matrix $\begin{pmatrix}1&0\\0&1\end{pmatrix}$.
- We do not use any ready-made inversion formulas; we test the defining algebraic condition directly.

## 4. Step-by-Step Solution

### Step 1: Compute the Product $AB$
Multiply rows of $A$ by columns of $B$:
$$AB = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}$$
- Top-left entry: $2(1) + 1(-1) = 2 - 1 = 1$.
- Top-right entry: $2(-1) + 1(2) = -2 + 2 = 0$.
- Bottom-left entry: $1(1) + 1(-1) = 1 - 1 = 0$.
- Bottom-right entry: $1(-1) + 1(2) = -1 + 2 = 1$.
Thus:
$$AB = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$$

### Step 2: Compute the Product $BA$
Multiply rows of $B$ by columns of $A$:
$$BA = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$$
- Top-left entry: $1(2) + (-1)(1) = 2 - 1 = 1$.
- Top-right entry: $1(1) + (-1)(1) = 1 - 1 = 0$.
- Bottom-left entry: $-1(2) + 2(1) = -2 + 2 = 0$.
- Bottom-right entry: $-1(1) + 2(1) = -1 + 2 = 1$.
Thus:
$$BA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$$

### Step 3: Relate to the Definition
Since both $AB = I$ and $BA = I$, matrix $B$ satisfies both the right-inverse and left-inverse conditions. Therefore, by the fundamental definition of an inverse matrix, $B = A^{-1}$.

## 5. Why Each Step Is Valid
- Matrix multiplication evaluates the composition of the two linear maps; producing the identity matrix shows that $B$ exactly reverses whatever transformation $A$ performs.
- Checking both directions ensures full compliance with the two-sided definition of an inverse matrix.

## 6. Final Answer in Words
Matrix $B$ is indeed the inverse of $A$. Computing both products yields $AB = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I$ and $BA = \begin{pmatrix}1&0\\0&1\end{pmatrix} = I$, which proves by the definition of matrix inverse that $B = A^{-1}$.

## 7. Quick Verification
- Determinant check: $\det A = 2(1) - 1(1) = 1$. $\det B = 1(2) - (-1)(-1) = 2 - 1 = 1$.
  By theory, $\det(A^{-1}) = 1/\det(A) = 1/1 = 1$, which matches $\det B$.
- Using the $2 \times 2$ adjugate formula: $A^{-1} = \frac{1}{1}\begin{pmatrix}1&-1\\-1&2\end{pmatrix} = B$. Perfect match.

## 8. Common Mistakes
- Computing only $AB = I$ and forgetting to verify or mention $BA = I$ (though for finite-dimensional square matrices one implies the other, the definition requires both).
- Confusing matrix inversion with taking reciprocals of individual entries ($1/2, 1/1$, etc.).

## 9. Short In-Class Explanation (3 Sentences)
To check whether $B$ is the inverse of $A$ without using formulas, we compute the products $AB$ and $BA$ directly. Multiplying them out shows that $AB = I$ and $BA = I$, where $I$ is the $2 \times 2$ identity matrix. Because their product in both directions yields the identity, $B$ satisfies the definition of the inverse matrix, so $B = A^{-1}$.
