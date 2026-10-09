# Problem 06: Parameter and Invertibility

## 1. Original Problem
For
$$A(t)=\begin{pmatrix}t&1\\2&t\end{pmatrix}$$
find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## 2. What We Are Trying to Find
We must determine all values of the real parameter $t$ that make the matrix $A(t)$ singular (non-invertible) and explain why the condition corresponds to the determinant vanishing.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Determinant Invertibility Theorem**: A square matrix $A$ fails to have an inverse if and only if its determinant is zero:
  $$A \text{ is not invertible} \iff \det A = 0.$$
- **Why this holds**: When $\det A = 0$, the transformation collapses two-dimensional area down to zero (mapping $\mathbb{R}^2$ onto a line or point), destroying information and making it impossible to invert the transformation.

## 4. Step-by-Step Solution

### Step 1: Calculate the Determinant of $A(t)$
Using the $2 \times 2$ determinant formula $\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc$:
$$\det A(t) = (t)(t) - (1)(2) = t^2 - 2.$$

### Step 2: Set the Determinant Equal to Zero
A matrix is not invertible if and only if $\det A(t) = 0$:
$$t^2 - 2 = 0.$$

### Step 3: Solve for the Parameter $t$
$$t^2 = 2 \implies t = \pm \sqrt{2}.$$

### Step 4: Explain the Relationship with Invertibility
- When $t \neq \pm \sqrt{2}$, $\det A(t) = t^2 - 2 \neq 0$, so the matrix is invertible, with explicit inverse:
  $$A(t)^{-1} = \frac{1}{t^2 - 2} \begin{pmatrix} t & -1 \\ -2 & t \end{pmatrix}.$$
- At $t = \sqrt{2}$ and $t = -\sqrt{2}$, the formula requires division by zero ($t^2 - 2 = 0$). At these exact values, the columns are scalar multiples of each other:
  For $t = \sqrt{2}$, the columns are $\begin{pmatrix} \sqrt{2} \\ 2 \end{pmatrix}$ and $\begin{pmatrix} 1 \\ \sqrt{2} \end{pmatrix}$, with Column 1 = $\sqrt{2} \times$ Column 2.
  Because the columns are linearly dependent, the matrix is singular and has no inverse.

## 5. Why Each Step Is Valid
- The algebraic equation $\det A(t) = 0$ is the exact analytical boundary separating invertible linear transformations from singular projections.
- Solving quadratic polynomial $t^2 - 2 = 0$ yields the two exact real roots $\pm\sqrt{2}$.

## 6. Final Answer in Words
The matrix $A(t)$ is not invertible for $t = \sqrt{2}$ and $t = -\sqrt{2}$. This occurs precisely because the determinant evaluates to $t^2 - 2$, and setting this expression to zero identifies the values of $t$ where the rows and columns become linearly dependent, making inversion impossible.

## 7. Quick Verification
- Test $t = \sqrt{2}$:
  $$\det A(\sqrt{2}) = (\sqrt{2})(\sqrt{2}) - 2 = 2 - 2 = 0.$$
- Test $t = -\sqrt{2}$:
  $$\det A(-\sqrt{2}) = (-\sqrt{2})(-\sqrt{2}) - 2 = 2 - 2 = 0.$$
- Test a regular value $t = 0$: $\det A(0) = -2 \neq 0$, which is invertible with inverse $\frac{1}{-2}\begin{pmatrix}0&-1\\-2&0\end{pmatrix}$.

## 8. Common Mistakes
- Forgetting the negative root, stating only $t = \sqrt{2}$ instead of $t = \pm \sqrt{2}$.
- Thinking the matrix is non-invertible when $t = 0$ (misidentifying parameter value zero with determinant zero).

## 9. Short In-Class Explanation (3 Sentences)
We calculate the determinant of the matrix as $t^2 - 2$ using the standard $2 \times 2$ formula. Setting this determinant equal to zero gives $t = \pm \sqrt{2}$ as the conditions for non-invertibility. At these two values, the columns become parallel, which collapses the area to zero and prevents the matrix from being inverted.
