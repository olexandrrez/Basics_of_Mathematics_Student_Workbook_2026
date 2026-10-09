# Problem 15: Combining Determinant Properties

## 1. Original Problem
Let $A$ and $B$ be invertible $2\times2$ matrices with
$$\det A=-2,\qquad \det B=3.$$
Without finding the entries of the matrices, compute
$$\det\left(B^{-1}A^TB\right).$$
State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

## 2. What We Are Trying to Find
We must evaluate the determinant of the similarity-like product matrix $B^{-1} A^T B$ using the given scalar determinants $\det A = -2$ and $\det B = 3$, state each applied theorem in sequence, and explain why the determinant of $B$ cancels out of the final expression.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Multiplicative Property of Determinants**: For any square matrices of the same size,
  $$\det(M N) = \det(M) \cdot \det(N).$$
  By extension to three matrices: $\det(M N P) = \det(M) \det(N) \det(P)$.
- **Determinant of an Inverse Matrix**: If $M$ is invertible,
  $$\det(M^{-1}) = \frac{1}{\det M}.$$
- **Determinant of a Transpose**: For any square matrix,
  $$\det(M^T) = \det(M).$$
- **Commutativity of Scalar Multiplication**: Determinants are real numbers; in the field $\mathbb{R}$, multiplication is commutative and associative.

## 4. Step-by-Step Solution

### Step 1: Apply the Multiplicative Property
Apply the product rule to the three factors in $B^{-1} A^T B$:
$$\det\left(B^{-1}A^TB\right) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B).$$

### Step 2: Apply the Inverse Property
Since $B$ is invertible and $\det B = 3 \neq 0$, the determinant of $B^{-1}$ is the reciprocal of $\det B$:
$$\det(B^{-1}) = \frac{1}{\det B} = \frac{1}{3}.$$

### Step 3: Apply the Transpose Property
Transposing a matrix does not change its determinant:
$$\det(A^T) = \det A = -2.$$

### Step 4: Substitute and Cancel
Substitute the values into the factored expression:
$$\det\left(B^{-1}A^TB\right) = \left(\frac{1}{\det B}\right) \cdot \det(A^T) \cdot \det(B) = \frac{1}{3} \cdot (-2) \cdot 3.$$
Because multiplication of real numbers is associative and commutative:
$$\left(\frac{1}{3} \cdot 3\right) \cdot (-2) = 1 \cdot (-2) = -2.$$

### Step 5: Explain Why the Factors Involving $B$ Cancel
In matrix algebra, $B^{-1}$ and $B$ cannot directly cancel because $A^T$ is between them, and matrix multiplication is non-commutative ($B^{-1} A^T B \neq A^T B^{-1} B$).
However, taking the determinant maps matrices to the real numbers $\mathbb{R}$.
In $\mathbb{R}$, multiplication is fully commutative:
$$\det(B^{-1}) \det(A^T) \det(B) = \det(B^{-1}) \det(B) \det(A^T) = \left(\frac{1}{\det B} \cdot \det B\right) \det A = 1 \cdot \det A = \det A.$$
The determinant of a matrix is invariant under similarity transformations: conjugate matrices share the exact same determinant.

## 5. Why Each Step Is Valid
- Cauchy-Binet theorem guarantees multiplicativity of determinants.
- The identity $\det(B^{-1}) = (\det B)^{-1}$ follows from $B B^{-1} = I$ and $\det I = 1$.
- Transposition preserves all Leibniz terms, ensuring $\det(A^T) = \det A$.
- Real scalar field arithmetic allows rearranging terms to cancel $3$ and $1/3$.

## 6. Final Answer in Words
The value of $\det(B^{-1} A^T B)$ is $-2$. In order, we used: (1) the multiplicative property for products, (2) the inverse property $\det(B^{-1}) = 1/\det B$, and (3) the transpose property $\det(A^T) = \det A$. The factors involving $B$ cancel because scalar multiplication in the real numbers is commutative, allowing $\frac{1}{\det B}$ and $\det B$ to multiply to 1.

## 7. Quick Verification
- Test with concrete diagonal matrices:
  Let $A = \begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix} \implies \det A = -2$.
  Let $B = \begin{pmatrix} 3 & 0 \\ 0 & 1 \end{pmatrix} \implies \det B = 3$.
  Then $B^{-1} = \begin{pmatrix} 1/3 & 0 \\ 0 & 1 \end{pmatrix}$ and $A^T = A$.
  $$B^{-1} A^T B = \begin{pmatrix} 1/3 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} -2/3 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix}.$$
  Its determinant is $(-2)(1) - 0 = -2$. The result matches.

## 8. Common Mistakes
- Canceling $B^{-1}$ and $B$ inside the matrix expression before applying the determinant (writing $B^{-1} A^T B = A^T$, which is false for matrices).
- Forgetting that $\det(A^T) = \det A$ and trying to invert or negate $\det A$.

## 9. Short In-Class Explanation (3 Sentences)
We split the determinant of the product into the product of the individual determinants using the multiplicative property. Because transposition preserves the determinant and inversion reciprocates it, the expression becomes $(1/\det B) \times \det A \times \det B$. Because multiplication of real numbers is commutative, the determinants of $B$ cancel out completely, leaving the final answer $-2$.
