# Problem 09: Area and the Determinant

## 1. Original Problem
The vectors
$$u=\begin{pmatrix}3\\1\end{pmatrix},\qquad v=\begin{pmatrix}1\\4\end{pmatrix}$$
span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## 2. What We Are Trying to Find
We must calculate the geometric area of the parallelogram formed by vectors $u$ and $v$ using a $2 \times 2$ determinant, evaluate the determinant when the order of the vectors is reversed, and explain the difference between the signed algebraic determinant and the non-negative geometric area.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Geometric Meaning of $2 \times 2$ Determinant**: The determinant of the matrix whose columns (or rows) are $u$ and $v$ equals the signed area of the parallelogram spanned by $u$ and $v$:
  $$\text{Area} = |\det\begin{pmatrix} u & v \end{pmatrix}|.$$
- **Orientation and Sign**:
  - A positive determinant indicates that the pair $(u, v)$ has positive (counterclockwise) orientation.
  - Swapping the vectors reverses orientation, changing the sign of the determinant, while geometric area is an absolute physical magnitude that remains invariant.

## 4. Step-by-Step Solution

### Step 1: Form the Matrix and Compute Area
Place $u$ and $v$ as columns into matrix $M = [u \mid v]$:
$$M = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}.$$
Compute the determinant:
$$\det M = (3)(4) - (1)(1) = 12 - 1 = 11.$$
The geometric area is the absolute value of the determinant:
$$\text{Area} = |\det M| = |11| = 11.$$

### Step 2: Reverse the Order of Vectors
Place $v$ and $u$ as columns into matrix $N = [v \mid u]$:
$$N = \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}.$$
Compute the determinant:
$$\det N = (1)(1) - (3)(4) = 1 - 12 = -11.$$

### Step 3: Compare Determinant and Area
- The determinant changed sign from $+11$ to $-11$.
- The geometric area is the absolute value: $|-11| = 11$, which is unchanged.

### Step 4: Geometric Explanation
- The determinant measures **oriented (signed) area**. In the pair $(u, v)$, turning from $u = (3,1)$ to $v = (1,4)$ is a counterclockwise rotation (the positive direction in the Cartesian plane), yielding $+11$.
- In the pair $(v, u)$, turning from $v$ to $u$ is a clockwise rotation (the negative direction), yielding $-11$.
- The **geometric area** represents the physical two-dimensional size of the shape, which depends only on the boundary shape and cannot be negative. Taking the absolute value $|\det|$ strips away orientation to return physical area.

## 5. Why Each Step Is Valid
- The cross-product magnitude in $\mathbb{R}^3$ for vectors in the $xy$-plane $(3,1,0) \times (1,4,0) = (0, 0, 11)$ has norm $11$, proving that $|ad - bc|$ strictly computes Euclidean area.
- Swapping columns swaps two vectors in an alternating 2-form, multiplying the algebraic value by $-1$.

## 6. Final Answer in Words
The area of the parallelogram is $11$. When the order of the vectors is reversed, the determinant changes sign from $11$ to $-11$, reflecting a change from counterclockwise to clockwise orientation. The geometric area does not change because physical area is the absolute value of the determinant, which remains $11$.

## 7. Quick Verification
- Base-height verification:
  Length of base $u$: $\|u\| = \sqrt{3^2 + 1^2} = \sqrt{10}$.
  Line containing $u$: $x - 3y = 0$.
  Height $h$ from $v=(1,4)$ to line: $h = \frac{|1 - 3(4)|}{\sqrt{1^2 + (-3)^2}} = \frac{|-11|}{\sqrt{10}} = \frac{11}{\sqrt{10}}$.
  $\text{Area} = \text{base} \times \text{height} = \sqrt{10} \times \frac{11}{\sqrt{10}} = 11$.
  Confirms the determinant result with elementary geometry.

## 8. Common Mistakes
- Stating that the area becomes $-11$ (area is a geometric quantity and can never be negative).
- Forgetting that taking the absolute value $|\det|$ is necessary when computing geometric area.

## 9. Short In-Class Explanation (3 Sentences)
We place the vectors into a matrix and compute the determinant to find an oriented area of $11$, so the physical area of the parallelogram is $11$. When we reverse the order of the vectors, the determinant flips its sign to $-11$ because the orientation switches from counterclockwise to clockwise. However, the geometric area remains $11$ because physical area is always the absolute value of the determinant.
