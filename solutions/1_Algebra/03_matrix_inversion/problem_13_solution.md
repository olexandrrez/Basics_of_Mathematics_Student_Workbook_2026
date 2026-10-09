# Problem 13: Undoing a Composite Transformation

## 1. Original Problem
The matrices
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad H=\begin{pmatrix}1&1\\0&1\end{pmatrix}$$
describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:
1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.
Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## 2. What We Are Trying to Find
We must compute the composite matrix $T = HS$ and invert it directly, compute the inverse by reversing the order of factor inverses $S^{-1}H^{-1}$, compare the two methods, calculate the wrong-order product $H^{-1}S^{-1}$ to see why it fails, and explain the geometric logic behind the reverse-order rule.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Inverse of a Matrix Product**: For any invertible matrices $A$ and $B$,
  $$(AB)^{-1} = B^{-1} A^{-1}.$$
- **Why order reverses**: If transformation $S$ is applied first followed by $H$, the last modification applied to the space was $H$. To return to the initial state, one must undo $H$ first (applying $H^{-1}$), which leaves the intermediate scaled shape, and then undo $S$ (applying $S^{-1}$).

## 4. Step-by-Step Solution

### Step 1: Method 1 — Compute $T$ First, Then Invert
Compute $T = HS$:
$$T = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(2)+1(0) & 1(0)+1(1) \\ 0(2)+1(0) & 0(0)+1(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}.$$
Compute determinant of $T$:
$$\det T = (2)(1) - (1)(0) = 2.$$
Compute $T^{-1}$ using the $2 \times 2$ inverse formula:
$$T^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}.$$

### Step 2: Method 2 — Using $(HS)^{-1} = S^{-1} H^{-1}$
First compute individual inverses:
- For $S = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}$: diagonal matrix, so:
  $$S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix}.$$
- For $H = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$: unit-determinant shear matrix, so:
  $$H^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}.$$
Now multiply in reverse order:
$$S^{-1} H^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(1)+0 & \frac{1}{2}(-1)+0 \\ 0+1(0) & 0+1(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}.$$
Both Method 1 and Method 2 yield the identical matrix.

### Step 3: Compute the Incorrect Order $H^{-1} S^{-1}$
Multiply in the un-reversed order:
$$H^{-1} S^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1\left(\frac{1}{2}\right)-1(0) & 1(0)-1(1) \\ 0\left(\frac{1}{2}\right)+1(0) & 0(0)+1(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -1 \\ 0 & 1 \end{pmatrix}.$$
Notice that:
$$\begin{pmatrix} \frac{1}{2} & -1 \\ 0 & 1 \end{pmatrix} \neq \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix} = T^{-1}.$$
The top-right entry is $-1$ instead of $-1/2$. The incorrect order fails.

### Step 4: Explain the Rule
When composite transformations are performed, each step builds on the geometry created by the preceding step. If you put on socks then shoes, you cannot remove socks while your shoes are still on. Similarly, because $H$ was the outer (last) transformation applied, $H^{-1}$ must be executed first to remove the shear. Only after the shear is undone can the horizontal compression $S^{-1}$ restore the original scale.

## 5. Why Each Step Is Valid
- $(HS)(S^{-1}H^{-1}) = H(S S^{-1})H^{-1} = H I H^{-1} = H H^{-1} = I$ is algebraically exact.
- Computing $H^{-1}S^{-1}$ demonstrates that $(HS)(H^{-1}S^{-1}) = H(S H^{-1})S^{-1} \neq I$ because $S$ and $H^{-1}$ do not commute.

## 6. Final Answer in Words
Both methods produce the correct inverse $T^{-1} = \begin{pmatrix} 1/2 & -1/2 \\ 0 & 1 \end{pmatrix}$. Computing the incorrect order yields $H^{-1}S^{-1} = \begin{pmatrix} 1/2 & -1 \\ 0 & 1 \end{pmatrix}$, which fails to invert $T$. Undoing operations from the end is required because the last transformation applied must be undone first before previous layers can be accessed.

## 7. Quick Verification
- Multiply $T$ by the wrong-order matrix:
  $$T(H^{-1}S^{-1}) = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1/2 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2+1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} \neq I.$$
  It leaves an un-canceled shear of $-1$, confirming that $H^{-1}S^{-1}$ is not the inverse.

## 8. Common Mistakes
- Thinking that because individual inverses are easy, multiplying them in either order produces the inverse.
- Forgetting that the last operation applied is the leftmost factor in the matrix product $T = HS$.

## 9. Short In-Class Explanation (3 Sentences)
We find the composite matrix $T = \begin{pmatrix}2&1\\0&1\end{pmatrix}$ and invert it directly to obtain $\begin{pmatrix}1/2&-1/2\\0&1\end{pmatrix}$. Applying the product rule in reverse order $S^{-1}H^{-1}$ yields the exact same inverse, whereas the forward order $H^{-1}S^{-1}$ produces an incorrect matrix with entry $-1$. This illustrates the fundamental principle that composite operations must be undone in reverse order, just like removing shoes before socks.
