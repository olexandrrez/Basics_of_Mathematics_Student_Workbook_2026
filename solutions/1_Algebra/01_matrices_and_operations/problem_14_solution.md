# Problem 14: Rotation Matrices

## 1. Original Problem
The matrix for a rotation through an angle $\theta$ is
$$R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}.$$
Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that
$$R(\alpha)R(\beta)=R(\alpha+\beta).$$
Explain the result geometrically.

## 2. What We Are Trying to Find
We must multiply two general $2 \times 2$ rotation matrices $R(\alpha)$ and $R(\beta)$, simplify the entries using the trigonometric addition identities, prove that the product equals $R(\alpha + \beta)$, and explain the geometric meaning of composing two planar rotations.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Trigonometric Angle-Sum Formulas**:
  $$\cos(\alpha + \beta) = \cos\alpha \cos\beta - \sin\alpha \sin\beta,$$
  $$\sin(\alpha + \beta) = \sin\alpha \cos\beta + \cos\alpha \sin\beta.$$
- **Geometric Composition**: Applying $R(\beta)$ rotates a vector counterclockwise by angle $\beta$. Applying $R(\alpha)$ to the resulting vector rotates it further by angle $\alpha$. The total rotation must be by angle $\alpha + \beta$.

## 4. Step-by-Step Solution

### Step 1: Set Up the Matrix Product
$$R(\alpha) R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix}.$$

### Step 2: Compute Entry by Entry
- **Top-left entry $(1,1)$**:
  $$\cos\alpha \cos\beta + (-\sin\alpha)(\sin\beta) = \cos\alpha \cos\beta - \sin\alpha \sin\beta.$$
  By the cosine angle-sum formula, this equals:
  $$\cos(\alpha + \beta).$$

- **Top-right entry $(1,2)$**:
  $$\cos\alpha (-\sin\beta) + (-\sin\alpha)(\cos\beta) = -(\sin\alpha \cos\beta + \cos\alpha \sin\beta).$$
  By the sine angle-sum formula, this equals:
  $$-\sin(\alpha + \beta).$$

- **Bottom-left entry $(2,1)$**:
  $$\sin\alpha \cos\beta + \cos\alpha \sin\beta.$$
  By the sine angle-sum formula, this equals:
  $$\sin(\alpha + \beta).$$

- **Bottom-right entry $(2,2)$**:
  $$\sin\alpha (-\sin\beta) + \cos\alpha \cos\beta = \cos\alpha \cos\beta - \sin\alpha \sin\beta.$$
  By the cosine angle-sum formula, this equals:
  $$\cos(\alpha + \beta).$$

### Step 3: Combine and Compare
Assembling the entries:
$$R(\alpha) R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha + \beta).$$

### Step 4: Geometric Explanation
A rotation matrix $R(\theta)$ rotates any vector in the Cartesian plane counterclockwise about the origin by angle $\theta$. Performing rotation by $\beta$ followed by rotation by $\alpha$ results in an overall counterclockwise rotation by the sum of the angles $\alpha + \beta$. Because matrix multiplication represents the composition of linear transformations, the product of the matrices must be the matrix of the combined transformation, $R(\alpha + \beta)$. Notice that rotations in the plane commute: $R(\alpha)R(\beta) = R(\alpha+\beta) = R(\beta)R(\alpha)$.

## 5. Why Each Step Is Valid
- Standard matrix multiplication definitions evaluate each entry as the dot product of rows from $R(\alpha)$ and columns from $R(\beta)$.
- Trigonometric angle-sum identities are exact mathematical theorems holding for all real angles $\alpha, \beta \in \mathbb{R}$.

## 6. Final Answer in Words
Direct multiplication of $R(\alpha)$ and $R(\beta)$ yields matrix entries that match the angle-sum identities for sine and cosine, establishing that $R(\alpha)R(\beta) = R(\alpha + \beta)$. Geometrically, rotating the plane by angle $\beta$ and then rotating the result by angle $\alpha$ is equivalent to a single rotation by the total angle $\alpha + \beta$.

## 7. Quick Verification
- Let $\alpha = 90^\circ$ and $\beta = 90^\circ$:
  $$R(90^\circ) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}.$$
  $$R(90^\circ) R(90^\circ) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} = R(180^\circ).$$
  Since $\cos(180^\circ) = -1$ and $\sin(180^\circ) = 0$, $R(180^\circ) = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}$. The formula holds.

## 8. Common Mistakes
- Sign errors when expanding the $(1,2)$ entry: $-(\cos\alpha \sin\beta + \sin\alpha \cos\beta)$ has both negative terms.
- Forgetting the minus sign in front of $\sin\theta$ in the original rotation matrix definition.

## 9. Short In-Class Explanation (3 Sentences)
Multiplying $R(\alpha)$ by $R(\beta)$ produces expressions that match the trigonometric addition formulas for sine and cosine. This proves algebraically that $R(\alpha)R(\beta) = R(\alpha+\beta)$. Geometrically, this means that applying a rotation by $\beta$ followed by a rotation by $\alpha$ is identical to a single rotation by the combined angle $\alpha+\beta$.
