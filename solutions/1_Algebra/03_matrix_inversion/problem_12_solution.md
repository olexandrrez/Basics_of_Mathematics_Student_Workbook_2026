# Problem 12: Finding Inverses Without Starting from Scratch

## 1. Original Problem
It is known that
$$A^{-1}=\begin{pmatrix}2&-1\\-3&2\end{pmatrix}.$$
Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## 2. What We Are Trying to Find
We must compute the inverses of $3A$, $A^T$, and $A^2$ directly from the known inverse matrix $A^{-1}$, without finding the original matrix $A$, using fundamental algebraic properties of matrix inverses.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Scalar Multiple of Inverse**: For any non-zero scalar $c$,
  $$(cA)^{-1} = \frac{1}{c} A^{-1}.$$
- **Transpose of Inverse**: The inverse of the transpose equals the transpose of the inverse:
  $$(A^T)^{-1} = (A^{-1})^T.$$
- **Power of Inverse**: For any integer power $k$,
  $$(A^k)^{-1} = (A^{-1})^k.$$

## 4. Step-by-Step Solution

### Step 1: Compute $(3A)^{-1}$
Using the property $(cA)^{-1} = \frac{1}{c} A^{-1}$ with $c = 3$:
$$(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3} \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{3} \\ -1 & \frac{2}{3} \end{pmatrix}.$$
- **Justification**: $(3A)\left(\frac{1}{3}A^{-1}\right) = 3 \cdot \frac{1}{3} (A A^{-1}) = 1 \cdot I = I$.

### Step 2: Compute $(A^T)^{-1}$
Using the property $(A^T)^{-1} = (A^{-1})^T$:
$$(A^T)^{-1} = \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}^T = \begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}.$$
- **Justification**: Transposing the relation $A A^{-1} = I$ gives $(A A^{-1})^T = I^T \implies (A^{-1})^T A^T = I$, which proves that $(A^{-1})^T$ is the inverse of $A^T$.

### Step 3: Compute $(A^2)^{-1}$
Using the property $(A^2)^{-1} = (A^{-1})^2$:
$$(A^2)^{-1} = A^{-1} A^{-1} = \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}.$$
Multiply row by column:
- Top-left: $2(2) + (-1)(-3) = 4 + 3 = 7$.
- Top-right: $2(-1) + (-1)(2) = -2 - 2 = -4$.
- Bottom-left: $-3(2) + 2(-3) = -6 - 6 = -12$.
- Bottom-right: $-3(-1) + 2(2) = 3 + 4 = 7$.
Thus:
$$(A^2)^{-1} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}.$$
- **Justification**: By the product-of-inverses theorem, $(A \cdot A)^{-1} = A^{-1} A^{-1}$.

## 5. Why Each Step Is Valid
- Each property derives directly from the definition of an inverse matrix without requiring knowledge of the specific entries of $A$.
- Standard matrix arithmetic evaluates the resulting products.

## 6. Final Answer in Words
The inverse of $3A$ is $\begin{pmatrix} 2/3 & -1/3 \\ -1 & 2/3 \end{pmatrix}$. The inverse of $A^T$ is $\begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}$. The inverse of $A^2$ is $\begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}$. All three were found directly from $A^{-1}$ using the rules $(cA)^{-1} = \frac{1}{c}A^{-1}$, $(A^T)^{-1} = (A^{-1})^T$, and $(A^2)^{-1} = (A^{-1})^2$.

## 7. Quick Verification
- Let us find $A$ to cross-check: $A = (A^{-1})^{-1}$.
  $\det(A^{-1}) = 2(2) - (-1)(-3) = 4 - 3 = 1$.
  $A = \begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix}$.
  Check $A^2 = \begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} 7 & 4 \\ 12 & 7 \end{pmatrix}$.
  Invert $A^2$: $\det(A^2) = 49 - 48 = 1 \implies (A^2)^{-1} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}$. Matches identically!

## 8. Common Mistakes
- Writing $(3A)^{-1} = 3 A^{-1}$ instead of $\frac{1}{3} A^{-1}$.
- Squaring entries individually rather than performing matrix multiplication $A^{-1} A^{-1}$.

## 9. Short In-Class Explanation (3 Sentences)
We find $(3A)^{-1}$ by dividing $A^{-1}$ by 3 because scalars invert by reciprocal, giving $\frac{1}{3}\begin{pmatrix}2&-1\\-3&2\end{pmatrix}$. For $(A^T)^{-1}$, we simply transpose $A^{-1}$ to obtain $\begin{pmatrix}2&-3\\-1&2\end{pmatrix}$. Finally, $(A^2)^{-1}$ is the square of $A^{-1}$, and multiplying $A^{-1}$ by itself yields $\begin{pmatrix}7&-4\\-12&7\end{pmatrix}$.
