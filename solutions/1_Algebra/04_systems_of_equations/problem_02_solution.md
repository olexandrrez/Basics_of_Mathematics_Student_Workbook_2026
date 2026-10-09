# Problem 02: Gaussian Elimination — One Solution

## 1. Original Problem
Solve using Gaussian elimination:
$$\begin{cases}x+y+z=6,\\2x-y+z=3,\\x+2y-z=2.\end{cases}$$
After solving, substitute the result into all equations and check consistency.

## 2. What We Are Trying to Find
We must determine the unique values of variables $x, y, z$ that satisfy the linear system using Gaussian elimination on the augmented matrix and verify the solution by direct substitution into all three original equations.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Gaussian Elimination**: Form the augmented matrix $[A \mid b]$. Use elementary row operations to reduce the matrix to row echelon form (upper triangular), and solve for variables via back-substitution.
- **Consistency and Uniqueness**: If the coefficient matrix has three non-zero pivots, the system has rank 3, guaranteeing a unique solution.

## 4. Step-by-Step Solution

### Step 1: Form the Augmented Matrix
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 2 & -1 & 1 & 3 \\ 1 & 2 & -1 & 2 \end{array}\right].$$

### Step 2: Eliminate $x$ from Rows 2 and 3
- $R_2 \leftarrow R_2 - 2R_1$:
  $$(2, -1, 1 \mid 3) - 2(1, 1, 1 \mid 6) = (0, -3, -1 \mid -9).$$
- $R_3 \leftarrow R_3 - R_1$:
  $$(1, 2, -1 \mid 2) - (1, 1, 1 \mid 6) = (0, 1, -2 \mid -4).$$
The augmented matrix becomes:
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 0 & 1 & -2 & -4 \end{array}\right].$$

### Step 3: Eliminate $y$ from Row 3
Swap $R_2$ and $R_3$ to get a pivot of $1$ in Row 2:
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & -3 & -1 & -9 \end{array}\right].$$
Now eliminate the $y$ term in Row 3 using $R_3 \leftarrow R_3 + 3R_2$:
$$(0, -3, -1 \mid -9) + 3(0, 1, -2 \mid -4) = (0, 0, -1 - 6 \mid -9 - 12) = (0, 0, -7 \mid -21).$$
The upper-triangular echelon form is:
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & -7 & -21 \end{array}\right].$$

### Step 4: Back-Substitution
1. From Row 3:
   $$-7z = -21 \implies z = \frac{-21}{-7} = 3.$$
2. From Row 2:
   $$y - 2z = -4 \implies y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2.$$
3. From Row 1:
   $$x + y + z = 6 \implies x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1.$$

The unique solution is $(x, y, z) = (1, 2, 3)$.

### Step 5: Check Consistency in All Three Equations
- Equation 1: $1 + 2 + 3 = 6$. ($6 = 6$, True)
- Equation 2: $2(1) - 2 + 3 = 2 - 2 + 3 = 3$. ($3 = 3$, True)
- Equation 3: $1 + 2(2) - 3 = 1 + 4 - 3 = 2$. ($2 = 2$, True)
The solution satisfies all three equations.

## 5. Why Each Step Is Valid
- Elementary row operations preserve the solution set of the system.
- Achieving three pivot positions guarantees that the system is non-singular and has a unique solution point in $\mathbb{R}^3$.

## 6. Final Answer in Words
The system has the unique solution $x = 1$, $y = 2$, and $z = 3$, written as the vector $(1, 2, 3)^T$. Substituting these values into all three equations yields $6=6$, $3=3$, and $2=2$, confirming that the solution is consistent and correct.

## 7. Quick Verification
- Cramer's rule / Determinant check:
  $\det A$: using our echelon matrix pivots, $\det = 1 \cdot 1 \cdot (-7) \times (-1) = 7 \neq 0$. Non-zero determinant confirms a unique solution.
- All three equations were individually checked and satisfied.

## 8. Common Mistakes
- Arithmetic errors when subtracting multiples, such as $-1 - 2(1) = -3$ vs $+1$.
- Skipping the substitution check in all equations and checking only the first one.

## 9. Short In-Class Explanation (3 Sentences)
We set up the augmented matrix and use row operations to eliminate entries below the diagonal, reaching an upper-triangular system. Back-substitution immediately gives $z = 3$, followed by $y = 2$, and finally $x = 1$. Substituting the point $(1, 2, 3)$ into all three original equations confirms that it satisfies every equation in the system.
