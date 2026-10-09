# Problem 03: Vector Normalization

## 1. Original Problem
For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

## 2. What We Are Trying to Find
We must find the unit vector $e$ pointing in the exact same direction as $v = (3, 4)$, verify that its Euclidean norm is $1$, show that $v$ decomposes into magnitude times direction ($v = \|v\|e$), and explain the geometric effect of normalization.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Vector Normalization**: A non-zero vector $v$ is normalized by dividing it by its scalar length:
  $$e = \frac{v}{\|v\|}.$$
- **Unit Vector Property**: The vector $e$ has length $\|e\| = 1$ while preserving the original direction and orientation.
- **Decomposition**: Any non-zero vector uniquely decomposes into a positive scalar magnitude $\|v\|$ and a unit direction vector $e$: $v = \|v\| e$.

## 4. Step-by-Step Solution

### Step 1: Compute the Length of $v$
For $v = (3, 4)$:
$$\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5.$$

### Step 2: Compute the Unit Vector $e$
Divide $v$ by its length $\|v\| = 5$:
$$e = \frac{1}{5} v = \frac{1}{5} (3, 4) = \left(\frac{3}{5}, \frac{4}{5}\right) = (0.6, 0.8).$$

### Step 3: Check That $\|e\| = 1$
Compute the length of $e$:
$$\|e\| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = \sqrt{1} = 1.$$
The vector $e$ is indeed a unit vector.

### Step 4: Reconstruct $v = \|v\| e$
Multiply the magnitude $\|v\| = 5$ by the unit vector $e$:
$$\|v\| e = 5 \left(\frac{3}{5}, \frac{4}{5}\right) = \left(5 \cdot \frac{3}{5}, 5 \cdot \frac{4}{5}\right) = (3, 4) = v.$$
The vector is reconstructed.

### Step 5: What Changes and What Remains Unchanged
- **What changes**: The **magnitude (length)** of the vector changes. The original vector had length $5$, whereas the normalized vector has length $1$.
- **What remains unchanged**:
  1. The **direction (line of action)** remains unchanged: $e$ lies on the same line through the origin with slope $m = 4/3$.
  2. The **orientation (sense)** remains unchanged: $e$ points into the first quadrant along the positive ray, because we scaled by a positive scalar $+1/5$.

## 5. Why Each Step Is Valid
- Dividing by a positive scalar $c > 0$ preserves orientation and scales length by $1/c$; choosing $c = \|v\|$ guarantees $\|e\| = \|v\| / \|v\| = 1$.
- Associativity of scalar multiplication guarantees that $\|v\| (v / \|v\|) = (\|v\| / \|v\|) v = 1 \cdot v = v$.

## 6. Final Answer in Words
The unit vector is $e = (3/5, 4/5) = (0.6, 0.8)$, and its length is $\|e\| = 1$. Reconstructing $v$ gives $5(3/5, 4/5) = (3, 4)$. Normalization changes the length of the vector to 1, while preserving its geometric direction and forward orientation.

## 7. Quick Verification
- Angle with $x$-axis: $\tan\theta = 4/3$ for both $v$ and $e$ ($\{4/5\} / \{3/5\} = 4/3$).
  Since $\theta = \arctan(4/3) \approx 53.13^\circ$ for both, direction is identical.

## 8. Common Mistakes
- Normalizing by dividing by the squared length $\|v\|^2 = 25$ instead of $\|v\| = 5$.
- Changing orientation by introducing negative signs.

## 9. Short In-Class Explanation (3 Sentences)
We calculate the length of $v = (3, 4)$ as $\sqrt{3^2 + 4^2} = 5$ and divide the vector by this length to obtain the unit vector $e = (3/5, 4/5)$. Checking its length confirms $\|e\| = \sqrt{9/25 + 16/25} = 1$, and multiplying it by 5 reconstructs $v = (3, 4)$. Normalization scales the magnitude to exactly 1 while keeping the direction and forward orientation completely unchanged.
