# Problem 11: A Parameter in a System of Three Equations

## 1. Original Problem
Analyze the number of solutions depending on $t$:
$$\begin{cases}x+y+z=1,\\x+ty+z=2,\\x+y+tz=3.\end{cases}$$
Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

## 2. What We Are Trying to Find
We must determine the number of solutions to this $3 \times 3$ linear system as a function of the parameter $t \in \mathbb{R}$ using Gaussian elimination, specifically examining the critical value where division by zero would occur during back-substitution.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Gaussian Elimination with a Parameter**: Perform row operations that do not involve dividing by an expression containing the parameter until necessary.
- **Critical Parameter Values**: Whenever dividing by an expression like $(t - 1)$, we must separately analyze the case $t = 1$ because division by zero is undefined.
- **Consistency**: A row $[0 \; 0 \; 0 \mid c]$ with $c \neq 0$ indicates inconsistency (no solution).

## 4. Step-by-Step Solution

### Step 1: Set Up the Augmented Matrix
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 1 & t & 1 & 2 \\ 1 & 1 & t & 3 \end{array}\right].$$

### Step 2: Eliminate $x$ from Rows 2 and 3
Subtract Row 1 from Row 2 and Row 3:
- $R_2 \leftarrow R_2 - R_1$:
  $$(1, t, 1 \mid 2) - (1, 1, 1 \mid 1) = (0, t-1, 0 \mid 1).$$
- $R_3 \leftarrow R_3 - R_1$:
  $$(1, 1, t \mid 3) - (1, 1, 1 \mid 1) = (0, 0, t-1 \mid 2).$$
The augmented matrix is now in triangular form:
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & t-1 & 0 & 1 \\ 0 & 0 & t-1 & 2 \end{array}\right].$$

Notice how clean this structure is: the diagonal pivots in Rows 2 and 3 are both $t - 1$.

### Step 3: Analyze the Critical Value $t = 1$
When $t = 1$, the factor $t - 1$ becomes $0$.
Substitute $t = 1$ directly into the reduced matrix:
$$\left[\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 2 \end{array}\right].$$
- Row 2 represents: $0x + 0y + 0z = 1 \implies 0 = 1$.
- Row 3 represents: $0x + 0y + 0z = 2 \implies 0 = 2$.
Both rows produce contradictions ($0 = 1$ and $0 = 2$).
Therefore, for $t = 1$, the system is **inconsistent** and has **no solution**.

### Step 4: Analyze for $t \neq 1$
When $t \neq 1$, $t - 1 \neq 0$, so dividing by $t - 1$ is valid.
1. From Row 3:
   $$(t-1)z = 2 \implies z = \frac{2}{t-1}.$$
2. From Row 2:
   $$(t-1)y = 1 \implies y = \frac{1}{t-1}.$$
3. From Row 1:
   $$x + y + z = 1 \implies x = 1 - y - z = 1 - \frac{1}{t-1} - \frac{2}{t-1} = 1 - \frac{3}{t-1} = \frac{t - 1 - 3}{t-1} = \frac{t - 4}{t-1}.$$

Since every variable has a unique determined value, the system has **exactly one unique solution** for every $t \neq 1$.
Notice that the case of infinitely many solutions never occurs for any real value of $t$.

## 5. Why Each Step Is Valid
- Row replacements $R_2 - R_1$ and $R_3 - R_1$ do not involve dividing by $t$, preserving algebraic equivalence for all $t \in \mathbb{R}$.
- Separating $t = 1$ prevents the illegal algebraic error of dividing by zero.

## 6. Final Answer in Words
For $t = 1$, the system has no solution because elimination produces contradictory rows $0 = 1$ and $0 = 2$. For any $t \neq 1$, the system has a unique solution given by $x = \frac{t-4}{t-1}$, $y = \frac{1}{t-1}$, and $z = \frac{2}{t-1}$. The case of infinitely many solutions does not occur for any value of $t$.

## 7. Quick Verification
- Compute $\det A$:
  Subtracting row 1 as done above, the upper-triangular matrix has determinant $1 \cdot (t-1) \cdot (t-1) = (t-1)^2$.
  $\det A = (t-1)^2 = 0 \iff t = 1$.
  When $t \neq 1$, $\det A \neq 0$, guaranteeing a unique solution by Cramer's theorem.
- Test $t = 2$: $x = (2-4)/(2-1) = -2$, $y = 1/1 = 1$, $z = 2/1 = 2$.
  Eq 1: $-2 + 1 + 2 = 1$. (Matches)
  Eq 2: $-2 + 2(1) + 2 = 2$. (Matches)
  Eq 3: $-2 + 1 + 2(2) = 3$. (Matches)
  All satisfied.

## 8. Common Mistakes
- Dividing by $t - 1$ without explicitly stating that $t \neq 1$, missing the singular case $t = 1$.
- Guessing that $t=1$ might give infinitely many solutions without checking the right-hand side.

## 9. Short In-Class Explanation (3 Sentences)
Subtracting the first row from the second and third rows simplifies the system to $(t-1)y = 1$ and $(t-1)z = 2$. If $t = 1$, these equations become $0 = 1$ and $0 = 2$, which are impossible contradictions, so there is no solution. For every $t \neq 1$, the coefficient is non-zero, yielding the unique solution $x = (t-4)/(t-1)$, $y = 1/(t-1)$, and $z = 2/(t-1)$.
