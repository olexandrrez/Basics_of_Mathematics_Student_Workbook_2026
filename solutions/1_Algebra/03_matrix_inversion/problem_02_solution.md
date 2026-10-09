# Problem 02: Formula for a 2×2 Matrix

## 1. Original Problem
Find the inverse of
$$A=\begin{pmatrix}3&2\\5&4\end{pmatrix}$$
using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## 2. What We Are Trying to Find
We need to find the inverse matrix $A^{-1}$ using the explicit $2 \times 2$ inversion formula (swapping diagonal entries, negating off-diagonal entries, and dividing by the determinant), and verify the result by showing $A A^{-1} = I$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **$2 \times 2$ Inverse Formula**: For a matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ with $\det A = ad - bc \neq 0$, the inverse is:
  $$A^{-1} = \frac{1}{\det A} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.$$
- **Three-step rule**:
  1. Swap the main diagonal entries ($a \leftrightarrow d$).
  2. Change the signs of the off-diagonal entries ($b \to -b, c \to -c$).
  3. Divide every entry by the determinant $\det A$.

## 4. Step-by-Step Solution

### Step 1: Compute the Determinant
For $A = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix}$:
$$\det A = (3)(4) - (2)(5) = 12 - 10 = 2.$$
Since $\det A = 2 \neq 0$, the matrix is invertible.

### Step 2: Form the Adjugate Matrix
- Swap diagonal entries: $3$ and $4$ become $4$ and $3$.
- Negate off-diagonal entries: $2$ becomes $-2$, and $5$ becomes $-5$.
$$\operatorname{adj}(A) = \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix}.$$

### Step 3: Multiply by $1/\det A$
$$A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}.$$

### Step 4: Verification by Computing $A A^{-1}$
Multiply $A$ by $A^{-1}$:
$$A A^{-1} = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}$$
- Top-left: $3(2) + 2\left(-\frac{5}{2}\right) = 6 - 5 = 1$.
- Top-right: $3(-1) + 2\left(\frac{3}{2}\right) = -3 + 3 = 0$.
- Bottom-left: $5(2) + 4\left(-\frac{5}{2}\right) = 10 - 10 = 0$.
- Bottom-right: $5(-1) + 4\left(\frac{3}{2}\right) = -5 + 6 = 1$.
Thus:
$$A A^{-1} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I.$$

## 5. Why Each Step Is Valid
- The adjugate matrix formula $A \operatorname{adj}(A) = (\det A) I$ holds for all square matrices; dividing by the non-zero scalar $\det A$ produces the exact inverse matrix.
- Verification confirms that the computed matrix undoes the linear mapping defined by $A$.

## 6. Final Answer in Words
The inverse matrix is $A^{-1} = \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}$ (or $\frac{1}{2}\begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix}$). Multiplying $A$ by $A^{-1}$ yields the identity matrix $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$, confirming the correctness of the inverse.

## 7. Quick Verification
- Also check the reverse product $A^{-1} A$:
  $$\frac{1}{2} \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix} \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 12 - 10 & 8 - 8 \\ -15 + 15 & -10 + 12 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 2 & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}.$$
  Both products yield $I$.

## 8. Common Mistakes
- Negating diagonal elements instead of swapping them, or swapping off-diagonal elements instead of negating them.
- Forgetting to divide by the determinant ($2$), leaving only the adjugate matrix.

## 9. Short In-Class Explanation (3 Sentences)
We first calculate the determinant of $A$, which is $12 - 10 = 2$. Next, we use the $2 \times 2$ inverse formula by swapping the diagonal entries, negating the off-diagonal entries, and dividing by 2 to get $A^{-1} = \begin{pmatrix}2&-1\\-5/2&3/2\end{pmatrix}$. Multiplying this result by $A$ gives the identity matrix $I$, which verifies the solution.
