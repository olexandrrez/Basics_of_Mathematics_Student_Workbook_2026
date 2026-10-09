# Problem 08: Two Systems with the Same Coefficient Matrix

## 1. Original Problem
Solve by elimination the two systems
$$\begin{cases}2x+y=5,\\x-y=1,\end{cases}$$
$$\begin{cases}2x+y=1,\\x-y=4.\end{cases}$$
Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

## 2. What We Are Trying to Find
We must solve two linear systems sharing the identical coefficient matrix but having different right-hand side constant vectors, compare the row elimination steps applied to each, and explain why the operations performed on the coefficient side are identical.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Role of the Coefficient Matrix in Elimination**: In Gaussian elimination, the sequence of elementary row operations is determined entirely by the entries of the coefficient matrix $A$ to clear its off-diagonal positions.
- **Combined Elimination**: Two systems $Ax = b_1$ and $Ax = b_2$ can be solved simultaneously by augmenting the matrix with multiple right-hand columns: $[A \mid b_1 \quad b_2]$.

## 4. Step-by-Step Solution

### Step 1: Solve System 1
$$\begin{cases} 2x + y = 5, \\ x - y = 1. \end{cases}$$
Set up the augmented matrix:
$$\left[\begin{array}{cc|c} 2 & 1 & 5 \\ 1 & -1 & 1 \end{array}\right].$$
Swap $R_1$ and $R_2$:
$$\left[\begin{array}{cc|c} 1 & -1 & 1 \\ 2 & 1 & 5 \end{array}\right].$$
Eliminate $x$ in Row 2 using $R_2 \leftarrow R_2 - 2R_1$:
- Left: $(2, 1) - 2(1, -1) = (0, 3)$.
- Right: $5 - 2(1) = 3$.
$$\left[\begin{array}{cc|c} 1 & -1 & 1 \\ 0 & 3 & 3 \end{array}\right].$$
Back-substitution:
- $3y = 3 \implies y = 1$.
- $x - y = 1 \implies x - 1 = 1 \implies x = 2$.
Solution for System 1: $(x, y) = (2, 1)$.

### Step 2: Solve System 2
$$\begin{cases} 2x + y = 1, \\ x - y = 4. \end{cases}$$
Set up the augmented matrix:
$$\left[\begin{array}{cc|c} 2 & 1 & 1 \\ 1 & -1 & 4 \end{array}\right].$$
Swap $R_1$ and $R_2$:
$$\left[\begin{array}{cc|c} 1 & -1 & 4 \\ 2 & 1 & 1 \end{array}\right].$$
Eliminate $x$ in Row 2 using $R_2 \leftarrow R_2 - 2R_1$:
- Left: $(2, 1) - 2(1, -1) = (0, 3)$.
- Right: $1 - 2(4) = 1 - 8 = -7$.
$$\left[\begin{array}{cc|c} 1 & -1 & 4 \\ 0 & 3 & -7 \end{array}\right].$$
Back-substitution:
- $3y = -7 \implies y = -\frac{7}{3}$.
- $x - y = 4 \implies x - \left(-\frac{7}{3}\right) = 4 \implies x + \frac{7}{3} = \frac{12}{3} \implies x = \frac{5}{3}$.
Solution for System 2: $(x, y) = (5/3, -7/3)$.

### Step 3: Compare Elimination Steps and Explain
- **Identical Parts**:
  - The row swap $R_1 \leftrightarrow R_2$ was identical in both systems.
  - The row replacement operation $R_2 \leftarrow R_2 - 2R_1$ was identical in both systems.
  - The reduced coefficient matrix $\begin{pmatrix} 1 & -1 \\ 0 & 3 \end{pmatrix}$ was identical in both systems.
- **Why this happens**:
  The choice of which row operations to perform depends solely on the coefficients on the left-hand side (to turn $A$ into an echelon matrix). The constants on the right-hand side merely follow along and get modified by the chosen operations, but they never dictate which row operations are selected.

## 5. Why Each Step Is Valid
- Elementary row operations act linearly across the augmented matrix.
- Because both systems share the same $A$, the exact same sequence of elementary matrices $E = E_k \dots E_1$ transforms $A$ into upper-triangular form $U = EA$.

## 6. Final Answer in Words
System 1 has solution $(x, y) = (2, 1)$, while System 2 has solution $(x, y) = (5/3, -7/3)$. The entire sequence of row operations applied to the coefficient matrix—swapping rows and subtracting twice the first row—is identical in both calculations because the choice of elimination steps is determined exclusively by the entries of $A$, independently of the right-hand side constants.

## 7. Quick Verification
- Check System 1: $2(2) + 1 = 5$ (True), $2 - 1 = 1$ (True).
- Check System 2: $2(5/3) + (-7/3) = (10 - 7)/3 = 3/3 = 1$ (True), $5/3 - (-7/3) = 12/3 = 4$ (True).
Both solutions verified.

## 8. Common Mistakes
- Repeating the derivation of which row operations to use instead of executing them simultaneously in a two-column augmented matrix $[A \mid b_1 \quad b_2]$.
- Arithmetic errors with fractions when solving for $x$ in System 2.

## 9. Short In-Class Explanation (3 Sentences)
We solve both systems by swapping the rows and subtracting twice the new first row from the second, giving solutions $(2, 1)$ and $(5/3, -7/3)$. The row operations performed on the left-hand side of the augmented matrix are completely identical in both cases. This occurs because the elimination steps are chosen entirely to clear the entries of the coefficient matrix, which is the same in both systems.
