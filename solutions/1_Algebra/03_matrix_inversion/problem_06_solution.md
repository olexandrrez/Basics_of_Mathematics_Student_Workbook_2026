# Problem 06: Solving a System Using the Inverse

## 1. Original Problem
Solve
$$Ax=b,$$
where
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}5\\7\end{pmatrix},$$
using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## 2. What We Are Trying to Find
We must find the unique solution vector $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ to the matrix system $Ax = b$ by first computing the inverse matrix $A^{-1}$, multiplying it by the vector $b$, and verifying the solution by direct substitution back into the original system.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Matrix Inversion Method for Linear Systems**: For a square system $Ax = b$, if $\det A \neq 0$, the matrix $A$ has an inverse $A^{-1}$, and the unique solution is:
  $$x = A^{-1} b.$$
- **$2 \times 2$ Inverse Formula**:
  $$A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.$$

## 4. Step-by-Step Solution

### Step 1: Compute the Inverse Matrix $A^{-1}$
For $A = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}$:
$$\det A = (2)(3) - (1)(1) = 6 - 1 = 5.$$
Since $\det A = 5 \neq 0$, $A$ is invertible.
Using the $2 \times 2$ formula:
$$A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.$$

### Step 2: Compute the Solution Vector $x = A^{-1} b$
Multiply $A^{-1}$ by $b = \begin{pmatrix} 5 \\ 7 \end{pmatrix}$:
$$x = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\ 7 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 3(5) + (-1)(7) \\ -1(5) + 2(7) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 15 - 7 \\ -5 + 14 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 8 \\ 9 \end{pmatrix} = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}.$$

### Step 3: Check by Direct Substitution into $Ax = b$
Substitute $x = \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix}$ into $Ax$:
$$Ax = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix} = \begin{pmatrix} 2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\ 1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \end{pmatrix} = \begin{pmatrix} \frac{16 + 9}{5} \\ \frac{8 + 27}{5} \end{pmatrix} = \begin{pmatrix} \frac{25}{5} \\ \frac{35}{5} \end{pmatrix} = \begin{pmatrix} 5 \\ 7 \end{pmatrix} = b.$$
The result matches vector $b$ exactly.

## 5. Why Each Step Is Valid
- Multiplying both sides of $Ax = b$ on the left by $A^{-1}$ gives $A^{-1}(Ax) = A^{-1}b \implies (A^{-1}A)x = A^{-1}b \implies Ix = x = A^{-1}b$.
- Associativity of matrix multiplication guarantees this deduction is mathematically sound.

## 6. Final Answer in Words
The solution to the system is $x = \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix}$ (or $x_1 = 1.6$, $x_2 = 1.8$). Substituting these values back into the matrix equation yields $\begin{pmatrix} 5 \\ 7 \end{pmatrix}$, confirming that the vector satisfies the system.

## 7. Quick Verification
- Check equations in scalar form:
  Equation 1: $2(1.6) + 1.8 = 3.2 + 1.8 = 5$.
  Equation 2: $1.6 + 3(1.8) = 1.6 + 5.4 = 7$.
  Both equations hold without error.

## 8. Common Mistakes
- Multiplying on the wrong side: writing $x = b A^{-1}$ (which is dimensionally undefined for a column vector $b$).
- Forgetting to divide by the determinant 5 when computing $x$, leading to integer values $(8, 9)^T$.

## 9. Short In-Class Explanation (3 Sentences)
We first find the inverse matrix $A^{-1} = \frac{1}{5}\begin{pmatrix}3&-1\\-1&2\end{pmatrix}$ using the standard $2 \times 2$ formula with determinant 5. Next, we multiply this inverse on the left of vector $b$ to isolate $x = A^{-1}b$, giving the solution vector $(8/5, 9/5)^T$. Finally, substituting this vector back into the original system reproduces the vector $(5, 7)^T$, confirming the answer.
