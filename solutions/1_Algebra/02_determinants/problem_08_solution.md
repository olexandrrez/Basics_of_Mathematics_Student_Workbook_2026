# Problem 08: Determinant of a Product

## 1. Original Problem
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

## 2. What We Are Trying to Find
We must compute the determinants of products $AB$ and $BA$ as well as the inverse-product $A^{-1}B$, and explain why $\det(AB) = \det(BA)$ holds universally despite matrix multiplication being non-commutative.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Product Rule for Determinants**: For any two $n \times n$ matrices $A$ and $B$,
  $$\det(AB) = \det(A) \cdot \det(B).$$
- **Inverse Determinant Rule**: If $\det A \neq 0$, then $A^{-1}$ exists and:
  $$\det(A^{-1}) = \frac{1}{\det A}.$$
- **Commutativity of Scalar Multiplication**: While matrix multiplication is non-commutative ($AB \neq BA$), multiplication of real numbers is commutative ($xy = yx$).

## 4. Step-by-Step Solution

### Step 1: Compute $\det(AB)$
Using the multiplicative property:
$$\det(AB) = \det(A) \cdot \det(B) = 3 \cdot (-5) = -15.$$

### Step 2: Compute $\det(BA)$
Using the multiplicative property:
$$\det(BA) = \det(B) \cdot \det(A) = (-5) \cdot 3 = -15.$$

### Step 3: Compute $\det(A^{-1}B)$
Since $\det A = 3 \neq 0$, the inverse $A^{-1}$ exists.
Its determinant is:
$$\det(A^{-1}) = \frac{1}{\det A} = \frac{1}{3}.$$
Now apply the product rule:
$$\det(A^{-1}B) = \det(A^{-1}) \cdot \det(B) = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.$$

### Step 4: Explain Why $\det(AB) = \det(BA)$
Although the matrices $AB$ and $BA$ are usually completely different matrices ($AB \neq BA$), their determinants are scalar numbers in $\mathbb{R}$.
Because multiplication of real numbers is commutative:
$$\det(AB) = \det(A) \cdot \det(B) = \det(B) \cdot \det(A) = \det(BA).$$
The determinant measures the factor by which volume is scaled; whether space is scaled by $3$ then $-5$, or by $-5$ then $3$, the net volume scaling factor is identically $-15$.

## 5. Why Each Step Is Valid
- Cauchy-Binet formula guarantees that $\det(MN) = \det(M)\det(N)$ for square matrices.
- The existence of $A^{-1}$ is guaranteed by $\det A = 3 \neq 0$.
- Scalar field axioms ensure commutativity of real multiplication.

## 6. Final Answer in Words
The determinants are $\det(AB) = -15$, $\det(BA) = -15$, and $\det(A^{-1}B) = -\frac{5}{3}$. The products $AB$ and $BA$ have identical determinants because, even though matrix multiplication is non-commutative, the product of their scalar determinants obeys ordinary commutative multiplication ($3 \times (-5) = (-5) \times 3$).

## 7. Quick Verification
- Check using identity $A A^{-1} = I$:
  $$\det(A A^{-1}) = \det(I) = 1 \implies \det(A)\det(A^{-1}) = 1 \implies \det(A^{-1}) = 1/3.$$
- Then $\det(A^{-1}B) = (1/3)(-5) = -5/3$.
- Check ratio: $\det(AB) / \det(A)^2 = -15 / 9 = -5/3 = \det(A^{-1}B)$. Perfect consistency.

## 8. Common Mistakes
- Thinking that because $AB \neq BA$, their determinants must also be different.
- Inverting the determinant of $B$ instead of $A$ when calculating $\det(A^{-1}B)$.

## 9. Short In-Class Explanation (3 Sentences)
By the multiplicative property of determinants, both $\det(AB)$ and $\det(BA)$ equal the product of the individual determinants, giving $3 \times (-5) = -15$. Even though matrix multiplication itself is non-commutative, multiplying real numbers is commutative, so the two determinants are always equal. Since $\det A \neq 0$, the inverse exists and has determinant $1/3$, giving $\det(A^{-1}B) = -5/3$.
