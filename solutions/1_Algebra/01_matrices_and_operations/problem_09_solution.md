# Problem 09: Composing Transformations

## 1. Original Problem
Let
$$S=\begin{pmatrix}2&0\\0&1\end{pmatrix},\qquad R=\begin{pmatrix}0&-1\\1&0\end{pmatrix}.$$
The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.
For
$$x=\begin{pmatrix}1\\2\end{pmatrix}$$
compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## 2. What We Are Trying to Find
We need to apply two successive linear transformations (scaling $S$ and rotation $R$) to the vector $x$ in both possible orders ($RSx$ and $SRx$), compare the resulting vectors, and explain the geometric reason why the order affects the final location.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Composition of Linear Transformations**: The expression $RSx$ means applying $S$ first to vector $x$, and then applying $R$ to the result $Sx$. The expression $SRx$ means applying $R$ first, and then $S$.
- **Geometric Noncommutativity**: Scaling along the $x$-axis scales horizontal distances. If a rotation occurs first, what was originally the horizontal coordinate is rotated onto the vertical axis, meaning scaling afterward affects a completely different geometric direction.

## 4. Step-by-Step Solution

### Step 1: Compute $RSx$ (Scale first, then Rotate)
- First compute $Sx$:
  $$Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2(1) \\ 1(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}.$$
- Next apply $R$ to $Sx$:
  $$RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(2) - 1(2) \\ 1(2) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}.$$

### Step 2: Compute $SRx$ (Rotate first, then Scale)
- First compute $Rx$:
  $$Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(1) - 1(2) \\ 1(1) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}.$$
- Next apply $S$ to $Rx$:
  $$SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} 2(-2) \\ 1(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}.$$

### Step 3: Compare Results and Geometric Explanation
We observe that:
$$RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\ 1 \end{pmatrix} = SRx.$$
**Geometric explanation**:
- In $RSx$, the point $(1,2)$ is first stretched horizontally by a factor of 2 to $(2,2)$. Then the $90^\circ$ rotation turns this symmetric vector $(2,2)$ into $(-2,2)$.
- In $SRx$, the vector $(1,2)$ is first rotated by $90^\circ$ into $(-2,1)$. Now the original $y$-component ($2$) has become the negative $x$-component ($-2$). When $S$ stretches the horizontal axis by 2, it stretches this coordinate to $-4$, yielding $(-4,1)$.
Because scaling acts directionally (only along the $x$-axis), changing the orientation before scaling changes which component gets amplified.

## 5. Why Each Step Is Valid
- Matrix associativity ensures that $R(Sx) = (RS)x$ and $S(Rx) = (SR)x$.
- Computing the composition step-by-step tracks the intermediate position of the vector in $\mathbb{R}^2$ after each transformation.

## 6. Final Answer in Words
The result of scaling first then rotating is $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$. The result of rotating first then scaling is $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$. The results differ because nonuniform scaling only expands along the fixed horizontal axis; rotating first moves the vector's components into different axes before the stretch occurs.

## 7. Quick Verification
- Compute product matrices:
  $$RS = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix} \implies RSx = \begin{pmatrix} 0(1)-1(2) \\ 2(1)+0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}.$$
  $$SR = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix} \implies SRx = \begin{pmatrix} 0(1)-2(2) \\ 1(1)+0(2) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}.$$
  Both methods produce identical results.

## 8. Common Mistakes
- Evaluating $RSx$ by multiplying $R$ on the right of $x$, forgetting that transformations act from the left ($T(x) = Tx$).
- Assuming rotation and scaling always commute (they only commute if the scaling is uniform, i.e., $S = cI$).

## 9. Short In-Class Explanation (3 Sentences)
Applying the stretch first and then the rotation produces the vector $(-2, 2)^T$, whereas rotating first and then stretching gives $(-4, 1)^T$. The order matters because the matrix $S$ only stretches horizontally along the $x$-axis. When we rotate first, the components change axes, so the stretch amplifies a completely different part of the original vector.
