# Problem 13: Do Four Points Lie in One Plane?

## 1. Original Problem
Given
$$A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

## 2. What We Are Trying to Find
We must construct vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$, find the normal vector $n$ to the plane containing $A, B, C$ via cross product, compute the dot product of displacement $\overrightarrow{AD}$ with $n$, and decide if point $D$ is coplanar with $A, B, C$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Coplanarity Condition via Scalar Triple Product**: Four points $A, B, C, D$ lie in the same plane (are coplanar) if and only if the displacement vector $\overrightarrow{AD}$ lies in the plane spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
- **Normal Criterion**: A vector $\overrightarrow{AD}$ lies in the plane if and only if it is perpendicular to the plane's normal vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$:
  $$\overrightarrow{AD} \cdot n = 0 \iff D \text{ lies in the plane } ABC.$$
- Geometrically, $\overrightarrow{AD} \cdot n$ is the scalar triple product $[\overrightarrow{AB}, \overrightarrow{AC}, \overrightarrow{AD}]$, which measures the volume of the parallelepiped spanned by the three vectors; volume is zero if and only if the points are coplanar.

## 4. Step-by-Step Solution

### Step 1: Construct Vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$
Since $A = (0, 0, 0)$ is the origin:
$$\overrightarrow{AB} = B - A = (1 - 0, 2 - 0, 0 - 0) = (1, 2, 0),$$
$$\overrightarrow{AC} = C - A = (0 - 0, 1 - 0, 1 - 0) = (0, 1, 1).$$

### Step 2: Find the Normal Vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$
Compute the cross product:
$$n = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}$$
- $\mathbf{i}$-component: $(2)(1) - (0)(1) = 2 - 0 = 2$.
- $\mathbf{j}$-component: $-[(1)(1) - (0)(0)] = -(1 - 0) = -1$.
- $\mathbf{k}$-component: $(1)(1) - (2)(0) = 1 - 0 = 1$.
Thus:
$$n = (2, -1, 1).$$

### Step 3: Construct $\overrightarrow{AD}$ and Check $\overrightarrow{AD} \cdot n$
Construct $\overrightarrow{AD}$:
$$\overrightarrow{AD} = D - A = (2 - 0, 5 - 0, 1 - 0) = (2, 5, 1).$$
Compute the dot product with $n = (2, -1, 1)$:
$$\overrightarrow{AD} \cdot n = (2)(2) + (5)(-1) + (1)(1) = 4 - 5 + 1 = 0.$$
The dot product is identically zero.

### Step 4: Decision and Geometric Justification
- **Decision**: Point $D$ **does lie in the plane** determined by $A, B, C$.
- **Justification**: The normal vector $n$ is perpendicular to every direction within the plane $ABC$. Any point $P$ lies in the plane through $A$ if and only if the displacement $\overrightarrow{AP}$ is perpendicular to $n$, which means $\overrightarrow{AP} \cdot n = 0$. Since $\overrightarrow{AD} \cdot n = 0$, the vector $\overrightarrow{AD}$ is perpendicular to the normal, meaning it has zero displacement in the perpendicular direction. Therefore, point $D$ lies entirely in the plane.

## 5. Why Each Step Is Valid
- The cross product produces a non-zero normal vector because $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are linearly independent.
- The scalar triple product criterion is an exact necessary and sufficient condition for coplanarity.

## 6. Final Answer in Words
The vectors are $\overrightarrow{AB} = (1, 2, 0)$ and $\overrightarrow{AC} = (0, 1, 1)$, giving the normal vector $n = (2, -1, 1)$. The vector to the fourth point is $\overrightarrow{AD} = (2, 5, 1)$, and its dot product with $n$ is $4 - 5 + 1 = 0$. Therefore, point $D$ lies in the plane determined by $A, B, C$ because its displacement vector is perpendicular to the plane's normal vector.

## 7. Quick Verification
- Check linear combination directly: can $\overrightarrow{AD} = a \overrightarrow{AB} + b \overrightarrow{AC}$?
  $$(2, 5, 1) = a(1, 2, 0) + b(0, 1, 1) = (a, 2a + b, b).$$
  Matching components: $a = 2$, $b = 1$.
  Check middle component: $2a + b = 2(2) + 1 = 5$, which matches!
  Since $\overrightarrow{AD} = 2\overrightarrow{AB} + \overrightarrow{AC}$, $\overrightarrow{AD}$ is an exact linear combination of the other two vectors, definitively proving coplanarity.

## 8. Common Mistakes
- Miscomputing the cross product $n$ (such as writing $+1$ instead of $-1$ for the $\mathbf{j}$-component).
- Concluding coplanarity without computing the dot product to verify zero.

## 9. Short In-Class Explanation (3 Sentences)
We construct the vectors $\overrightarrow{AB} = (1, 2, 0)$ and $\overrightarrow{AC} = (0, 1, 1)$ and compute their cross product to find the normal vector $n = (2, -1, 1)$. Taking the dot product of $\overrightarrow{AD} = (2, 5, 1)$ with $n$ yields $4 - 5 + 1 = 0$. Because this dot product is zero, the vector $\overrightarrow{AD}$ has no component perpendicular to the plane, proving that point $D$ lies in the same plane as $A$, $B$, and $C$.
