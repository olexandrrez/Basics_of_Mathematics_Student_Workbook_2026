# Problem 11: Parameter and Invertibility

## 1. Original Problem
For
$$A(t)=\begin{pmatrix}1&t\\t&1\end{pmatrix}$$
find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## 2. What We Are Trying to Find
We must determine the range of values for parameter $t \in \mathbb{R}$ for which $A(t)$ has an inverse, compute the general parameter-dependent inverse formula $A(t)^{-1}$, and explain why the formula breaks down at the excluded values.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Determinant Criterion**: $A(t)$ is invertible if and only if $\det A(t) \neq 0$.
- **$2 \times 2$ Inverse Formula**:
  $$A(t)^{-1} = \frac{1}{\det A(t)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.$$
- **Geometric Collapse**: When $\det A(t) = 0$, dividing by zero in the formula reflects the collapse of 2D area onto a 1D line in the plane.

## 4. Step-by-Step Solution

### Step 1: Compute the Determinant of $A(t)$
For $A(t) = \begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix}$:
$$\det A(t) = (1)(1) - (t)(t) = 1 - t^2.$$

### Step 2: Determine Invertibility Condition
The matrix is invertible if and only if:
$$\det A(t) \neq 0 \iff 1 - t^2 \neq 0 \iff t^2 \neq 1 \iff t \neq \pm 1.$$
Therefore, $A(t)$ is invertible for all $t \in \mathbb{R} \setminus \{-1, 1\}$.

### Step 3: Find the Formula for $A(t)^{-1}$
Using the $2 \times 2$ inverse formula:
- Swap diagonal entries: $1$ and $1$ remain $1$ and $1$.
- Negate off-diagonal entries: $t$ and $t$ become $-t$ and $-t$.
$$A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}.$$

### Step 4: Explain What Happens at Excluded Values
At $t = 1$ and $t = -1$:
1. **Division by Zero**: The scaling factor $\frac{1}{1 - t^2}$ becomes $\frac{1}{0}$, which is undefined.
2. **Row / Column Proportionality**:
   - For $t = 1$: $A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}$. The two rows are identical ($R_1 = R_2$). The matrix projects all vectors in $\mathbb{R}^2$ onto the single line $y = x$.
   - For $t = -1$: $A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}$. The second row is the exact negative of the first ($R_2 = -R_1$).
   At these values, the dimension of the image drops from $2$ to $1$, destroying information. Because the transformation is not one-to-one, no inverse function or matrix can exist.

## 5. Why Each Step Is Valid
- The polynomial equation $1 - t^2 = 0$ has exactly two real solutions $t = 1$ and $t = -1$.
- For all other values, dividing by $1 - t^2$ is algebraically valid in $\mathbb{R}$.

## 6. Final Answer in Words
The matrix $A(t)$ is invertible for all real numbers $t$ except $t = 1$ and $t = -1$. For all $t \neq \pm 1$, the inverse is $A(t)^{-1} = \frac{1}{1 - t^2}\begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}$. At the excluded values $t = \pm 1$, the determinant becomes zero, causing division by zero and reflecting the fact that the rows become parallel and collapse the plane onto a single line.

## 7. Quick Verification
- Test with $t = 0$: $A(0) = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$.
  Formula gives $A(0)^{-1} = \frac{1}{1 - 0}\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$. Correct!
- Test with $t = 2$: $A(2) = \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}$.
  Formula gives $A(2)^{-1} = \frac{1}{1 - 4}\begin{pmatrix} 1 & -2 \\ -2 & 1 \end{pmatrix} = -\frac{1}{3}\begin{pmatrix} 1 & -2 \\ -2 & 1 \end{pmatrix}$.
  Check product: $\begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} \left(-\frac{1}{3}\right)\begin{pmatrix} 1 & -2 \\ -2 & 1 \end{pmatrix} = -\frac{1}{3}\begin{pmatrix} 1-4 & -2+2 \\ 2-2 & -4+1 \end{pmatrix} = -\frac{1}{3}\begin{pmatrix} -3 & 0 \\ 0 & -3 \end{pmatrix} = I$. Correct!

## 8. Common Mistakes
- Factoring $1 - t^2$ and forgetting the negative root, stating only $t \neq 1$.
- Swapping the parameter sign incorrectly in the adjugate matrix.

## 9. Short In-Class Explanation (3 Sentences)
We compute the determinant as $1 - t^2$, which shows that the matrix is invertible for all real $t$ except $t = \pm 1$. For all other values, the inverse formula gives $A(t)^{-1} = \frac{1}{1 - t^2}\begin{pmatrix}1 & -t \\ -t & 1\end{pmatrix}$. At the excluded values $\pm 1$, the determinant is zero, meaning the rows become parallel and the matrix cannot be inverted.
