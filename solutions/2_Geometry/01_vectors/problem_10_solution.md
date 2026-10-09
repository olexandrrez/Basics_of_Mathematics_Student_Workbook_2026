# Problem 10: Triangle Area from Vectors

## 1. Original Problem
The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

## 2. What We Are Trying to Find
We must construct the edge vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ from the given vertices, compute the area of the parallelogram spanned by them using the magnitude of their cross product, compute the triangle's area, and explain the geometric reason for the factor $1/2$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Cross Product and Area**: The magnitude of the cross product of two vectors equals the geometric area of the parallelogram they span:
  $$\text{Area}(\text{parallelogram}) = \|\overrightarrow{AB} \times \overrightarrow{AC}\|.$$
- **Area of a Triangle**: Any triangle formed by three points $A, B, C$ has an area equal to exactly half of the parallelogram spanned by vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$:
  $$\text{Area}(\Delta ABC) = \frac{1}{2} \|\overrightarrow{AB} \times \overrightarrow{AC}\|.$$

## 4. Step-by-Step Solution

### Step 1: Construct Vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$
Subtract point $A=(0,0,0)$ from $B$ and $C$:
$$\overrightarrow{AB} = B - A = (2 - 0, 1 - 0, 0 - 0) = (2, 1, 0),$$
$$\overrightarrow{AC} = C - A = (1 - 0, 3 - 0, 2 - 0) = (1, 3, 2).$$

### Step 2: Compute the Cross Product $\overrightarrow{AB} \times \overrightarrow{AC}$
$$\overrightarrow{AB} \times \overrightarrow{AC} = \det\begin{pmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & 0 \\ 1 & 3 & 2 \end{pmatrix}$$
- $\mathbf{i}$-component: $(1)(2) - (0)(3) = 2 - 0 = 2$.
- $\mathbf{j}$-component: $-[(2)(2) - (0)(1)] = -(4 - 0) = -4$.
- $\mathbf{k}$-component: $(2)(3) - (1)(1) = 6 - 1 = 5$.
Thus:
$$\overrightarrow{AB} \times \overrightarrow{AC} = (2, -4, 5).$$

### Step 3: Compute the Parallelogram Area
The area of the parallelogram is the magnitude of the cross product:
$$\text{Area}(\text{parallelogram}) = \|(2, -4, 5)\| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = \sqrt{9 \cdot 5} = 3\sqrt{5}.$$

### Step 4: Compute the Triangle Area
$$\text{Area}(\Delta ABC) = \frac{1}{2} \text{Area}(\text{parallelogram}) = \frac{1}{2} (3\sqrt{5}) = \frac{3\sqrt{5}}{2}.$$

### Step 5: Explain the Factor $\frac{1}{2}$
The diagonal segment joining $B$ and $C$ splits the parallelogram spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$ into two congruent triangles: $\Delta ABC$ and $\Delta DCB$ (where $D = B + \overrightarrow{AC}$).
Because the two triangles are congruent, their areas are identical.
The total area of the parallelogram is the sum of the areas of the two triangles:
$$\text{Area}(\text{parallelogram}) = 2 \cdot \text{Area}(\Delta ABC) \implies \text{Area}(\Delta ABC) = \frac{1}{2} \text{Area}(\text{parallelogram}).$$
Thus, the factor $1/2$ comes directly from the fact that a triangle is exactly half of the parallelogram formed by its two edge vectors.

## 5. Why Each Step Is Valid
- The cross-product magnitude $\|u \times v\| = \|u\| \|v\| \sin\theta = \text{base} \times \text{height}$ evaluates the exact area of the parallelogram.
- Euclidean plane geometry guarantees that a parallelogram is bisected into two congruent triangles by its diagonal.

## 6. Final Answer in Words
The edge vectors are $\overrightarrow{AB} = (2, 1, 0)$ and $\overrightarrow{AC} = (1, 3, 2)$. Their cross product is $(2, -4, 5)$, which has length $3\sqrt{5}$, giving a parallelogram area of $3\sqrt{5}$. The area of the triangle is $\frac{3\sqrt{5}}{2}$ (approximately $3.354$). The factor $1/2$ appears because the diagonal of a parallelogram cuts it into two congruent triangles of equal area.

## 7. Quick Verification
- Check with Heron's formula:
  $a = \|BC\| = \|(1-2, 3-1, 2-0)\| = \|(-1, 2, 2)\| = \sqrt{1+4+4} = \sqrt{9} = 3$.
  $b = \|AC\| = \|(1, 3, 2)\| = \sqrt{1+9+4} = \sqrt{14}$.
  $c = \|AB\| = \|(2, 1, 0)\| = \sqrt{4+1+0} = \sqrt{5}$.
  Using $\cos A = \frac{b^2 + c^2 - a^2}{2bc} = \frac{14 + 5 - 9}{2\sqrt{14}\sqrt{5}} = \frac{10}{2\sqrt{70}} = \frac{5}{\sqrt{70}}$.
  $\sin A = \sqrt{1 - 25/70} = \sqrt{45/70} = \frac{3\sqrt{5}}{\sqrt{70}}$.
  $\text{Area} = \frac{1}{2} b c \sin A = \frac{1}{2} \sqrt{14} \sqrt{5} \frac{3\sqrt{5}}{\sqrt{70}} = \frac{1}{2} \sqrt{70} \frac{3\sqrt{5}}{\sqrt{70}} = \frac{3\sqrt{5}}{2}$.
  Heron / sine formula confirms the result.

## 8. Common Mistakes
- Forgetting to take the square root of $45$ when calculating the vector norm.
- Omitting the factor $1/2$ and reporting the parallelogram's area as the triangle's area.

## 9. Short In-Class Explanation (3 Sentences)
We form the edge vectors $\overrightarrow{AB} = (2, 1, 0)$ and $\overrightarrow{AC} = (1, 3, 2)$ and compute their cross product $(2, -4, 5)$. The magnitude of this cross product is $\sqrt{45} = 3\sqrt{5}$, which represents the area of the parallelogram spanned by the two vectors. Taking half of this magnitude gives the triangle's area as $\frac{3\sqrt{5}}{2}$ because a triangle occupies exactly half of the parallelogram.
