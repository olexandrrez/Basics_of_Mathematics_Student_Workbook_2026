# Problem 07: Choosing a Method Deliberately

## 1. Original Problem
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:
1. one system with a triangular coefficient matrix
   $$\begin{cases}2x-y=3,\\4y=8;\end{cases}$$
2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

## 2. What We Are Trying to Find
We must analyze three computational scenarios, select the optimal mathematical method for each based on the matrix structure and the number of right-hand sides, execute the solution for the triangular system, and describe the strategic computational efficiency plan for the other two.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Triangular Systems $\to$ Direct Back-Substitution**: A triangular matrix already has zeros below (or above) the diagonal, requiring zero elimination steps; solving directly from the bottom up is immediate and requires minimal arithmetic.
- **Multiple Right-Hand Sides with Known $A^{-1} \to$ Matrix-Vector Multiplication**: If $A^{-1}$ is already known, finding each solution $x_i$ takes only one matrix-vector multiplication $x_i = A^{-1} b_i$. The precomputed inverse is fully reusable across all $b_i$.
- **Single System with Unknown Inverse $\to$ Gaussian Elimination**: Finding $A^{-1}$ requires roughly $n^3$ operations, whereas Gaussian elimination with back-substitution takes only $\frac{1}{3} n^3$ operations. For a single right-hand side, computing the full inverse is completely unnecessary overhead.

## 4. Step-by-Step Solution

### Scenario 1: Triangular System
- **Chosen Method**: Direct Back-Substitution.
- **Justification**: The coefficient matrix is already in upper-triangular echelon form; no row operations or matrix inversions are needed.
- **Execution**:
  $$\begin{cases} 2x - y = 3, \\ 4y = 8. \end{cases}$$
  1. From the second equation:
     $$4y = 8 \implies y = \frac{8}{4} = 2.$$
  2. Substitute $y = 2$ into the first equation:
     $$2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}.$$
  The unique solution is $(x, y) = (5/2, 2)$.

### Scenario 2: Three Systems $Ax = b_i$ with Known Invertible $A^{-1}$
- **Chosen Method**: Matrix Multiplication $x_i = A^{-1} b_i$.
- **Justification and Plan**:
  Since $A^{-1}$ is already computed, we calculate each solution vector directly:
  $$x_1 = A^{-1} b_1,\qquad x_2 = A^{-1} b_2,\qquad x_3 = A^{-1} b_3.$$
- **Reusable vs Unnecessary**:
  - The matrix $A^{-1}$ is completely **reusable** for all three vectors (and any future vectors).
  - Running three separate Gaussian eliminations from scratch on each $[A \mid b_i]$ would redundantly repeat the exact same row operations on $A$ three times, wasting effort.

### Scenario 3: Single $3 \times 3$ System without Known Inverse
- **Chosen Method**: Gaussian Elimination with Back-Substitution.
- **Justification and Plan**:
  Augment the matrix $[A \mid b]$, perform row operations to reach upper-triangular echelon form, and find $x$ via back-substitution.
- **Reusable vs Unnecessary**:
  - Inverting $A$ requires augmenting with the full identity matrix $[A \mid I_3]$ and running elimination on 3 right-hand columns, which takes roughly three times more arithmetic operations.
  - Computing $A^{-1}$ is **unnecessary** because the goal is solely to find one single solution vector $x$, so the inverse would never be used again.

## 5. Why Each Step Is Valid
- The back-substitution steps $4y=8 \implies y=2$ and $2x-2=3 \implies x=5/2$ are exact algebraic deductions.
- The computational complexity arguments ($\mathcal{O}(n^3/3)$ for elimination vs $\mathcal{O}(n^3)$ for full inversion) rigorously substantiate the method choices.

## 6. Final Answer in Words
For Case 1, direct back-substitution is optimal, yielding $y = 2$ and $x = 5/2$. For Case 2, matrix-vector multiplication $x_i = A^{-1} b_i$ is optimal because the precomputed inverse is reused three times. For Case 3, Gaussian elimination is optimal because computing the entire inverse matrix is unnecessary and computationally wasteful for a single solution vector.

## 7. Quick Verification
- Check Case 1 solution:
  $2(5/2) - 2 = 5 - 2 = 3$ (True).
  $4(2) = 8$ (True).
  Both equations satisfied.

## 8. Common Mistakes
- Blindly computing $A^{-1}$ for every linear system regardless of size or context.
- Forgetting that when $A^{-1}$ is already given, solving is just a matrix-vector multiplication.

## 9. Short In-Class Explanation (3 Sentences)
For the triangular system, we immediately back-substitute to find $y = 2$ and $x = 5/2$ without needing any row operations. When solving multiple systems with the same matrix and an already known inverse, we simply multiply $x_i = A^{-1}b_i$ to reuse the inverse efficiently. For a single system with an unknown inverse, Gaussian elimination is the best choice because computing the full inverse requires three times more work than necessary.
