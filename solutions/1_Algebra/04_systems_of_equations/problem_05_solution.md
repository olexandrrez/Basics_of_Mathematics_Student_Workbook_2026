# Problem 05: Row Echelon Form and Number of Solutions

## 1. Original Problem
For the augmented matrix
$$\left[\begin{array}{ccc|c}1&2&-1&3\\0&1&2&1\\0&0&0&0\end{array}\right]$$
determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

## 2. What We Are Trying to Find
We must read off the consistency and number of solutions directly from a given row echelon augmented matrix, explain how pivot columns determine the number of free variables, and express the infinite solution set in parametric form.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Rank and Free Variables**:
  - Let $n$ be the number of variables (here $n = 3$, corresponding to variables $x_1, x_2, x_3$).
  - Let $r = \operatorname{rank}(A)$ be the number of non-zero rows (pivots) in the coefficient matrix.
  - If the system is consistent (no row of the form $[0 \; 0 \dots 0 \mid c]$ with $c \neq 0$), the number of free variables is:
    $$\text{Number of free variables} = n - r.$$
  - If $n - r > 0$, the system has **infinitely many solutions** parameterized by $n - r$ free variables.

## 4. Step-by-Step Solution

### Step 1: Analyze the Matrix Structure and Pivots
The augmented matrix is:
$$\left[\begin{array}{ccc|c} 1 & 2 & -1 & 3 \\ 0 & 1 & 2 & 1 \\ 0 & 0 & 0 & 0 \end{array}\right].$$
- Row 1 has leading entry (pivot) in Column 1 ($x_1$).
- Row 2 has leading entry (pivot) in Column 2 ($x_2$).
- Row 3 is $[0 \; 0 \; 0 \mid 0]$, which is a consistent trivial identity $0 = 0$.
The system is consistent.
The number of pivots is $r = 2$.
The number of variables is $n = 3$.

### Step 2: Determine the Number of Free Variables
$$\text{Number of free variables} = n - r = 3 - 2 = 1.$$
Column 3 has no pivot, so variable $x_3$ is the free variable.
Because there is $1$ free variable and the system is consistent, there are **infinitely many solutions**.

### Step 3: Express Leading Variables in Terms of Parameter
Let $x_3 = t$, where $t \in \mathbb{R}$ is an arbitrary parameter.
1. From Row 2:
   $$x_2 + 2x_3 = 1 \implies x_2 + 2t = 1 \implies x_2 = 1 - 2t.$$
2. From Row 1:
   $$x_1 + 2x_2 - x_3 = 3.$$
   Substitute $x_2 = 1 - 2t$ and $x_3 = t$:
   $$x_1 + 2(1 - 2t) - t = 3 \implies x_1 + 2 - 4t - t = 3 \implies x_1 - 5t = 1 \implies x_1 = 1 + 5t.$$

### Step 4: Write the Solution in Parametric Form
$$\mathbf{x} = \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 1 + 5t \\ 1 - 2t \\ t \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} 5 \\ -2 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}.$$

## 5. Why Each Step Is Valid
- The coefficient matrix has rank 2, and the augmented matrix has rank 2; by Rouché-Capelli, the system is consistent.
- Subtracting the rank from the total number of unknowns strictly identifies the dimension of the affine solution subspace ($3 - 2 = 1$, a line).

## 6. Final Answer in Words
The system is consistent and has infinitely many solutions with one degree of freedom. We know that exactly one variable can be chosen freely because there are 3 variables but only 2 pivot columns ($3 - 2 = 1$). In parametric form, the solution set is $x_1 = 1 + 5t$, $x_2 = 1 - 2t$, and $x_3 = t$ for any real number $t$.

## 7. Quick Verification
- Test $t = 0$: $(x_1, x_2, x_3) = (1, 1, 0)$.
  Row 1: $1 + 2(1) - 0 = 3$. (Matches)
  Row 2: $0 + 1 + 2(0) = 1$. (Matches)
- Test $t = 1$: $(x_1, x_2, x_3) = (6, -1, 1)$.
  Row 1: $6 + 2(-1) - 1 = 6 - 2 - 1 = 3$. (Matches)
  Row 2: $0 + (-1) + 2(1) = 1$. (Matches)
Both points satisfy the system.

## 8. Common Mistakes
- Miscounting the free variables by treating the right-hand side column as a variable column.
- Algebra errors when substituting $x_2$ into Row 1: distributing $2(1 - 2t)$ as $2 - 2t$ instead of $2 - 4t$.

## 9. Short In-Class Explanation (3 Sentences)
The augmented matrix is in row echelon form with two pivots in the first two columns and a bottom row of zeros, showing the system is consistent. Because there are three variables but only two pivots, the number of free variables is $3 - 2 = 1$, meaning there are infinitely many solutions. Setting $x_3 = t$ allows us to back-substitute and express the solution line as $(1+5t, 1-2t, t)^T$.
