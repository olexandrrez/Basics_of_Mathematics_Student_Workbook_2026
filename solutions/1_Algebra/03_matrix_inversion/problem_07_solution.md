# Problem 07: Inverse of a Product

## 1. Original Problem
For
$$A=\begin{pmatrix}1&1\\0&1\end{pmatrix},\qquad B=\begin{pmatrix}2&0\\0&3\end{pmatrix}$$
compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## 2. What We Are Trying to Find
We must compute the product $AB$ and invert it to find $(AB)^{-1}$, compute the inverses $A^{-1}$ and $B^{-1}$ individually and multiply them in reverse order $B^{-1}A^{-1}$, verify that both calculations produce identical matrices, and explain why the factor order must reverse.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Inverse of a Product Theorem**: For any invertible matrices $A$ and $B$,
  $$(AB)^{-1} = B^{-1} A^{-1}.$$
- **Why order reverses (The "Shoe-and-Sock Rule")**: When putting on shoes and socks, you put on socks first ($B$), then shoes ($A$). When taking them off, you must take off shoes first ($A^{-1}$), and only then socks ($B^{-1}$). Algebraically:
  $$(AB)(B^{-1}A^{-1}) = A (B B^{-1}) A^{-1} = A I A^{-1} = A A^{-1} = I.$$

## 4. Step-by-Step Solution

### Step 1: Compute $AB$ and Its Inverse
Multiply $A$ by $B$:
$$AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 1(2)+1(0) & 1(0)+1(3) \\ 0(2)+1(0) & 0(0)+1(3) \end{pmatrix} = \begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix}.$$
Compute determinant of $AB$:
$$\det(AB) = (2)(3) - (3)(0) = 6.$$
Using the $2 \times 2$ inverse formula on $AB$:
$$(AB)^{-1} = \frac{1}{6} \begin{pmatrix} 3 & -3 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{6} & -\frac{3}{6} \\ 0 & \frac{2}{6} \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}.$$

### Step 2: Compute $A^{-1}$ and $B^{-1}$
- For $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$: $\det A = 1(1) - 1(0) = 1$.
  $$A^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}.$$
- For $B = \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}$: $\det B = (2)(3) - 0 = 6$.
  Being a diagonal matrix, its inverse simply inverts the diagonal entries:
  $$B^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix}.$$

### Step 3: Compute $B^{-1} A^{-1}$
Multiply $B^{-1}$ by $A^{-1}$:
$$B^{-1} A^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(1)+0 & \frac{1}{2}(-1)+0 \\ 0+\frac{1}{3}(0) & 0+\frac{1}{3}(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}.$$

### Step 4: Comparison and Meaning of Reversed Order
Comparing the results:
$$(AB)^{-1} = B^{-1} A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}.$$
The results are identical.
**Meaning of reversed order**: To undo the composite action of $A$ following $B$, we must undo $A$ first (by applying $A^{-1}$), which leaves $B$ exposed to be undone second by $B^{-1}$. If we mistakenly applied $A^{-1} B^{-1}$, the product $(AB)(A^{-1}B^{-1})$ would not allow the inner matrices to cancel because $B$ and $A^{-1}$ do not commute.

## 5. Why Each Step Is Valid
- Matrix associativity allows $(AB)(B^{-1}A^{-1}) = A(B B^{-1})A^{-1} = A I A^{-1} = I$, proving that $B^{-1}A^{-1}$ is the unique two-sided inverse of $AB$.
- Inverting diagonal entries of a diagonal matrix is a direct consequence of diagonal matrix multiplication.

## 6. Final Answer in Words
Both $(AB)^{-1}$ and $B^{-1} A^{-1}$ evaluate to $\begin{pmatrix} 1/2 & -1/2 \\ 0 & 1/3 \end{pmatrix}$. The reversed order is necessary because undoing a sequence of operations must proceed in reverse chronological order: the last operation applied ($A$) must be the first one undone ($A^{-1}$).

## 7. Quick Verification
- What if we tried the incorrect order $A^{-1} B^{-1}$?
  $$A^{-1} B^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1/2 & 0 \\ 0 & 1/3 \end{pmatrix} = \begin{pmatrix} 1/2 & -1/3 \\ 0 & 1/3 \end{pmatrix} \neq (AB)^{-1}.$$
  The entry in the top right is $-1/3$ instead of $-1/2$. This clearly shows that the order of inversion matters.

## 8. Common Mistakes
- Writing $(AB)^{-1} = A^{-1} B^{-1}$ without reversing the factors.
- Incorrectly inverting the upper-triangular matrix $AB$.

## 9. Short In-Class Explanation (3 Sentences)
We compute $AB = \begin{pmatrix}2&3\\0&3\end{pmatrix}$ and invert it directly to get $\begin{pmatrix}1/2&-1/2\\0&1/3\end{pmatrix}$. Computing $B^{-1}A^{-1}$ separately yields the exact same matrix, verifying the property $(AB)^{-1} = B^{-1}A^{-1}$. The order of factors must reverse because the last operation applied must be the first one undone to allow adjacent terms to cancel to the identity.
