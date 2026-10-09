# Problem 02: Distance as the Length of a Vector

## 1. Original Problem
The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

## 2. What We Are Trying to Find
We must construct the displacement vector from point $A$ to point $B$, compute its Euclidean norm (length), compute the distance between points $A$ and $B$ using the Euclidean distance formula, and explain why distance is identical to vector length.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Displacement Vector**: The vector connecting initial point $A$ to terminal point $B$ is given by subtracting coordinates:
  $$\overrightarrow{AB} = B - A = (x_B - x_A, y_B - y_A, z_B - z_A).$$
- **Length (Norm) of a Vector**: The length of vector $v = (v_1, v_2, v_3)$ is:
  $$\|v\| = \sqrt{v_1^2 + v_2^2 + v_3^2}.$$
- **Euclidean Distance Formula**: The distance $d(A, B)$ is the straight-line distance defined by the 3D Pythagorean theorem.

## 4. Step-by-Step Solution

### Step 1: Construct the Vector $\overrightarrow{AB}$
Subtract the coordinates of point $A=(1, 2, 3)$ from point $B=(4, -2, 6)$:
$$\overrightarrow{AB} = (4 - 1, -2 - 2, 6 - 3) = (3, -4, 3).$$

### Step 2: Compute the Length of $\overrightarrow{AB}$
Apply the norm formula:
$$\|\overrightarrow{AB}\| = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}.$$

### Step 3: Compute Distance Using the Coordinate Formula
The distance formula between two points in $\mathbb{R}^3$ is:
$$d(A, B) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2 + (z_B - z_A)^2}.$$
Substitute coordinates:
$$d(A, B) = \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}.$$

### Step 4: Explain Why Both Calculations Give the Same Result
Both calculations yield the identical result $\sqrt{34}$ because they are algebraically and geometrically the exact same operation:
- The vector $\overrightarrow{AB}$ stores the coordinate differences: $\Delta x = x_B - x_A$, $\Delta y = y_B - y_A$, and $\Delta z = z_B - z_A$.
- The length of $\overrightarrow{AB}$ is $\sqrt{(\Delta x)^2 + (\Delta y)^2 + (\Delta z)^2}$.
- The point-distance formula is nothing other than the length of this displacement vector: $d(A, B) = \|\overrightarrow{AB}\|$.
Distance is defined as the magnitude of translation required to move from $A$ to $B$.

## 5. Why Each Step Is Valid
- The displacement vector is well-defined by subtracting position vectors $\mathbf{r}_B - \mathbf{r}_A$.
- The Pythagorean theorem in 3 dimensions establishes that the hypotenuse of spatial displacements $\Delta x, \Delta y, \Delta z$ is $\sqrt{\Delta x^2 + \Delta y^2 + \Delta z^2}$.

## 6. Final Answer in Words
The displacement vector is $\overrightarrow{AB} = (3, -4, 3)$, and its length is $\sqrt{34}$. The distance formula between the points gives $d(A, B) = \sqrt{34}$. The two calculations agree because the distance between two points in Euclidean space is defined as the length of the displacement vector connecting them.

## 7. Quick Verification
- Check the reverse vector $\overrightarrow{BA} = A - B = (-3, 4, -3)$.
  $\|\overrightarrow{BA}\| = \sqrt{(-3)^2 + 4^2 + (-3)^2} = \sqrt{9 + 16 + 9} = \sqrt{34}$.
  Distance is symmetric: $d(A, B) = d(B, A) = \sqrt{34}$.
- Approximate value: $\sqrt{34} \approx 5.831$.

## 8. Common Mistakes
- Squaring $-4$ and writing $-16$ instead of $+16$: $(-4)^2 = 16$.
- Subtracting coordinates in reverse ($A - B$) when asked for $\overrightarrow{AB}$ (terminal point minus initial point).

## 9. Short In-Class Explanation (3 Sentences)
Subtracting the coordinates of $A$ from $B$ produces the displacement vector $\overrightarrow{AB} = (3, -4, 3)$. Calculating its length by the Pythagorean theorem gives $\sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{34}$. This matches the distance formula between points $A$ and $B$ because Euclidean distance is simply the length of the vector connecting the two points.
