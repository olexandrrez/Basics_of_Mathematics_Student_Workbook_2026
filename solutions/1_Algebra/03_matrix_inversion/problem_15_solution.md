# Problem 15: Two Methods for Solving the Same System

## 1. Original Problem
For
$$A=\begin{pmatrix}2&1\\1&3\end{pmatrix},\qquad b=\begin{pmatrix}7\\8\end{pmatrix}$$
solve $Ax=b$ in two ways:
1. using $A^{-1}b$,
2. using Gaussian elimination.
Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## 2. What We Are Trying to Find
We must solve the $2 \times 2$ system $Ax = b$ using two different methods: matrix inversion and Gaussian elimination. We compare the computational steps required by each method and evaluate which approach is more efficient for this problem.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Method 1 (Matrix Inversion)**: Compute $\det A$, find $A^{-1}$ using the adjugate formula, and evaluate $x = A^{-1} b$.
- **Method 2 (Gaussian Elimination)**: Form the augmented matrix $[A \mid b]$, perform row operations to reach upper-triangular echelon form, and solve for the variables by back-substitution.
- **Method Comparison**: Elimination solves directly for the given right-hand side. A known inverse can be reused for other right-hand sides, but elimination factors can also be reused; this example compares the work for one right-hand side only.

## 4. Step-by-Step Solution

### Method 1: Using $A^{-1} b$
1. Compute the determinant:
   $$\det A = (2)(3) - (1)(1) = 6 - 1 = 5.$$
2. Compute the inverse matrix $A^{-1}$:
   $$A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.$$
3. Multiply by $b = \begin{pmatrix} 7 \\ 8 \end{pmatrix}$:
   $$x = A^{-1} b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 7 \\ 8 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 3(7) - 1(8) \\ -1(7) + 2(8) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 21 - 8 \\ -7 + 16 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 13 \\ 9 \end{pmatrix} = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}.$$

### Method 2: Using Gaussian Elimination
1. Form the augmented matrix:
   $$\left[\begin{array}{cc|c} 2 & 1 & 7 \\ 1 & 3 & 8 \end{array}\right].$$
2. First swap $R_1$ and $R_2$ to obtain a pivot of 1:
   $$\left[\begin{array}{cc|c} 1 & 3 & 8 \\ 2 & 1 & 7 \end{array}\right].$$
3. Eliminate the first column in Row 2 using $R_2 \leftarrow R_2 - 2R_1$:
   - Left side: $(2, 1) - 2(1, 3) = (0, -5)$.
   - Right side: $7 - 2(8) = 7 - 16 = -9$.
   $$\left[\begin{array}{cc|c} 1 & 3 & 8 \\ 0 & -5 & -9 \end{array}\right].$$
4. Back-substitution:
   - From Row 2: $-5x_2 = -9 \implies x_2 = \frac{9}{5}$.
   - From Row 1: $x_1 + 3x_2 = 8 \implies x_1 = 8 - 3\left(\frac{9}{5}\right) = \frac{40 - 27}{5} = \frac{13}{5}$.
Thus $x = \begin{pmatrix} 13/5 \\ 9/5 \end{pmatrix}$.

### Step 3: Comparison of the Methods
- Both methods yield the exact same solution: $x_1 = 13/5 = 2.6$, $x_2 = 9/5 = 1.8$.
- **Comparison for this example**:
  - Method 1 computes the determinant and all four entries of $A^{-1}$, then multiplies by $b$.
  - Method 2 first swaps the two rows, then performs one row replacement and two back-substitution steps.
- **Which method was simpler here**: Gaussian elimination was more direct for this one right-hand side because it did not require computing the full inverse. For multiple right-hand sides, a known inverse can be reused; alternatively, elimination factors can be reused to solve each system.

## 5. Why Each Step Is Valid
- Matrix inversion uses the exact algebraic inverse $A^{-1} A = I$.
- Gaussian elimination applies elementary row operations that preserve the solution set of the linear system.

## 6. Final Answer in Words
Both methods yield the unique solution $x = \begin{pmatrix} 13/5 \\ 9/5 \end{pmatrix}$. For solving a single system, Gaussian elimination was simpler because it eliminated the variable in one step and used back-substitution without needing to compute the full inverse matrix.

## 7. Quick Verification
- Check in original system:
  - Equation 1: $2(13/5) + 1(9/5) = (26 + 9)/5 = 35/5 = 7$.
  - Equation 2: $1(13/5) + 3(9/5) = (13 + 27)/5 = 40/5 = 8$.
  Both original equations are satisfied.

## 8. Common Mistakes
- Arithmetic errors with fractions when back-substituting in Gaussian elimination: $8 - 27/5 = (40-27)/5 = 13/5$.
- Multiplying $b$ by $A^{-1}$ on the wrong side.

## 9. Short In-Class Explanation (3 Sentences)
We solve the system first by computing $A^{-1} = \frac{1}{5}\begin{pmatrix}3&-1\\-1&2\end{pmatrix}$ and multiplying by $b$, and second by using Gaussian elimination to reduce the augmented matrix. Both approaches yield the exact same solution vector $(13/5, 9/5)^T$. For a single system, Gaussian elimination is simpler and faster because it avoids the overhead of calculating the entire inverse matrix.
