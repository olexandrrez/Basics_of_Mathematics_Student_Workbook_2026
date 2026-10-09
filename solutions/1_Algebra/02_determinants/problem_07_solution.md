# Problem 07: Using Properties Instead of Recomputing

## 1. Original Problem
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute
$$\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).$$
Justify each answer using the appropriate property.

## 2. What We Are Trying to Find
We need to determine the determinants of four transformed matrices ($2A$, $A^T$, $A^2$, and $-A$) given that $A$ is a $3 \times 3$ matrix with $\det A = -4$, without knowing the individual entries of $A$, using determinant algebraic properties.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Scalar Multiple Property**: For an $n \times n$ matrix and scalar $c \in \mathbb{R}$,
  $$\det(cA) = c^n \det(A).$$
  (Each of the $n$ rows is scaled by $c$, pulling out a factor of $c$ for each row). Here $n = 3$.
- **Transpose Property**: The determinant of a matrix equals the determinant of its transpose:
  $$\det(A^T) = \det(A).$$
- **Multiplicative / Power Property**: For square matrices, $\det(AB) = \det(A)\det(B)$, which implies:
  $$\det(A^k) = (\det A)^k.$$
- **Negation Property**: As a special case of scalar scaling with $c = -1$:
  $$\det(-A) = (-1)^n \det(A).$$

## 4. Step-by-Step Solution

### Step 1: Compute $\det(2A)$
- Formula: $\det(cA) = c^n \det(A)$ with $c = 2$ and $n = 3$:
  $$\det(2A) = 2^3 \det(A) = 8 \cdot (-4) = -32.$$
- **Justification**: Factoring a scalar out of a determinant scales each row independently; since $A$ has 3 rows, a factor of 2 comes from each row, giving $2^3 = 8$.

### Step 2: Compute $\det(A^T)$
- Formula: $\det(A^T) = \det(A)$:
  $$\det(A^T) = -4.$$
- **Justification**: Transposition swaps rows and columns; the set of all terms in the Leibniz formula remains identical because a permutation and its inverse have the same sign.

### Step 3: Compute $\det(A^2)$
- Formula: $\det(A^2) = (\det A)^2$:
  $$\det(A^2) = (-4)^2 = 16.$$
- **Justification**: The determinant is a multiplicative map, so $\det(A \cdot A) = \det(A) \cdot \det(A)$.

### Step 4: Compute $\det(-A)$
- Formula: $\det(-A) = (-1)^n \det(A)$ with $n = 3$:
  $$\det(-A) = (-1)^3 \det(A) = -1 \cdot (-4) = 4.$$
- **Justification**: Multiplying $A$ by $-1$ negates each of its 3 rows; multiplying by $-1$ three times yields $(-1)^3 = -1$.

## 5. Why Each Step Is Valid
- These four identities are core structural theorems of multilinear alternating forms on $\mathbb{R}^n$.
- Dimension $n=3$ is explicitly specified in the problem statement, making $c^n = c^3$ the correct factor.

## 6. Final Answer in Words
The values are $\det(2A) = -32$, $\det(A^T) = -4$, $\det(A^2) = 16$, and $\det(-A) = 4$. Each calculation follows directly from properties: scaling pulls out $c^3 = 8$, transposing leaves the determinant unchanged, squaring squares the determinant, and negating pulls out $(-1)^3 = -1$.

## 7. Quick Verification
- Let $A$ be the diagonal matrix $\operatorname{diag}(-4, 1, 1)$, which has $\det A = -4$:
  - $2A = \operatorname{diag}(-8, 2, 2) \implies \det(2A) = (-8)(2)(2) = -32$.
  - $A^T = A \implies \det(A^T) = -4$.
  - $A^2 = \operatorname{diag}(16, 1, 1) \implies \det(A^2) = 16$.
  - $-A = \operatorname{diag}(4, -1, -1) \implies \det(-A) = 4(-1)(-1) = 4$.
  All test calculations match our results perfectly.

## 8. Common Mistakes
- Writing $\det(2A) = 2 \det(A) = -8$, forgetting that the scalar must be raised to the power of the matrix dimension $n=3$.
- Writing $\det(-A) = -4$ by assuming $-A$ always has the same sign as $A$, forgetting that $(-1)^3 = -1$ flips the negative sign to positive.

## 9. Short In-Class Explanation (3 Sentences)
For a $3 \times 3$ matrix, pulling out a scalar requires raising it to the third power, so $\det(2A) = 2^3(-4) = -32$ and $\det(-A) = (-1)^3(-4) = 4$. The transpose does not change the determinant, so $\det(A^T) = -4$. Finally, because the determinant distributes over matrix multiplication, $\det(A^2) = (-4)^2 = 16$.
