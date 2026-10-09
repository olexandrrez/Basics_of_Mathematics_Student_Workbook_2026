# Problem 09: Distances

## 1. Original Problem
Compute:
1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

## 2. What We Are Trying to Find
We must compute the perpendicular distance from a 2D point to a line and from a 3D point to a plane using standard distance formulas, compare the mathematical structures of the formulas, and explain why both originate from projection onto the normal vector.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Point-to-Line Distance (2D)**: For point $P = (x_0, y_0)$ and line $A x + B y + C = 0$:
  $$d(P, L) = \frac{|A x_0 + B y_0 + C|}{\sqrt{A^2 + B^2}} = \frac{|A x_0 + B y_0 + C|}{\|n\|}.$$
- **Point-to-Plane Distance (3D)**: For point $Q = (x_0, y_0, z_0)$ and plane $A x + B y + C z + D = 0$:
  $$d(Q, \Pi) = \frac{|A x_0 + B y_0 + C z_0 + D|}{\sqrt{A^2 + B^2 + C^2}} = \frac{|A x_0 + B y_0 + C z_0 + D|}{\|n\|}.$$
- **Normal Projection Principle**: The shortest distance from any point $X$ to a hyper-plane is the length of the orthogonal projection of the displacement vector $(X - X_0)$ onto the unit normal vector:
  $$d = |(X - X_0) \cdot \hat{n}| = \frac{|(X - X_0) \cdot n|}{\|n\|}.$$

## 4. Step-by-Step Solution

### Step 1: Distance from $P=(2, 3)$ to Line $3x + 4y - 10 = 0$
- Point: $(x_0, y_0) = (2, 3)$.
- Line coefficients: $A = 3, B = 4, C = -10$.
- Normal vector: $n = (3, 4)$, with length:
  $$\|n\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5.$$
- Substitute into the distance formula:
  $$d(P, L) = \frac{|3(2) + 4(3) - 10|}{5} = \frac{|6 + 12 - 10|}{5} = \frac{|8|}{5} = \frac{8}{5} = 1.6.$$

### Step 2: Distance from $Q=(2, -1, 3)$ to Plane $2x - 2y + z - 4 = 0$
- Point: $(x_0, y_0, z_0) = (2, -1, 3)$.
- Plane coefficients: $A = 2, B = -2, C = 1, D = -4$.
- Normal vector: $n = (2, -2, 1)$, with length:
  $$\|n\| = \sqrt{2^2 + (-2)^2 + 1^2} = \sqrt{4 + 4 + 1} = \sqrt{9} = 3.$$
- Substitute into the distance formula:
  $$d(Q, \Pi) = \frac{|2(2) - 2(-1) + 1(3) - 4|}{3} = \frac{|4 + 2 + 3 - 4|}{3} = \frac{|5|}{3} = \frac{5}{3} \approx 1.667.$$

### Step 3: Compare the Formulas and Explain Connection to Normal
- **Structural Comparison**:
  Both formulas have the identical mathematical form:
  $$d = \frac{|f(x_0)|}{\|n\|},$$
  where $f(x)$ is the affine function defining the object ($f(x) = 0$), and $\|n\|$ is the Euclidean norm of the normal vector.
- **Connection to Normal Direction**:
  The shortest path from a point to a flat surface is along the unique line that meets the surface at a right angle (the normal direction).
  Let $X_0$ be any point on the line/plane (so $f(X_0) = 0$). The displacement from $X_0$ to our external point is $w = X - X_0$.
  The scalar projection of $w$ onto the unit normal vector $\hat{n} = n / \|n\|$ is:
  $$\text{proj}_{\hat{n}} w = |w \cdot \hat{n}| = \frac{|(X - X_0) \cdot n|}{\|n\|} = \frac{|n \cdot X - n \cdot X_0|}{\|n\|} = \frac{|A x_0 + B y_0 + \dots + \text{Const}|}{\|n\|}.$$
  Both formulas are simply the length of the orthogonal projection of the displacement vector onto the normal line.

## 5. Why Each Step Is Valid
- The 2D line and 3D plane distance formulas are direct consequences of vector dot product projection.
- Taking the absolute value guarantees that geometric distance is strictly non-negative.

## 6. Final Answer in Words
The distance from point $P$ to the line is $8/5 = 1.6$, and the distance from point $Q$ to the plane is $5/3 \approx 1.67$. Both formulas share the exact same mathematical structure: evaluating the Cartesian equation at the point and dividing by the length of the normal vector. This occurs because the shortest distance in both cases is the orthogonal projection of the point onto the normal vector.

## 7. Quick Verification
- Check line: Point on line closest to $(2, 3)$ is $(2, 3) - \frac{8}{25}(3, 4) = (2 - 24/25, 3 - 32/25) = (26/25, 43/25)$.
  Check on line: $3(26/25) + 4(43/25) - 10 = (78 + 172)/25 - 10 = 250/25 - 10 = 0$.
  Distance = $\frac{8}{25} \|(3, 4)\| = \frac{8}{25}(5) = 8/5$. Verified!
- Check plane: Point on plane closest to $Q$ is $(2, -1, 3) - \frac{5}{9}(2, -2, 1) = (8/9, 1/9, 22/9)$.
  Check in plane: $2(8/9) - 2(1/9) + 22/9 - 4 = (16 - 2 + 22)/9 - 4 = 36/9 - 4 = 0$.
  Distance = $\frac{5}{9}(3) = 5/3$. Verified!

## 8. Common Mistakes
- Forgetting to take the square root in the denominator: dividing by $A^2 + B^2$ rather than $\sqrt{A^2 + B^2}$.
- Sign errors when substituting negative coordinates: $-2(-1) = +2$, not $-2$.

## 9. Short In-Class Explanation (3 Sentences)
We plug point $P(2, 3)$ into the line equation and divide by the normal length $\sqrt{3^2+4^2}=5$ to get the distance $8/5 = 1.6$. Similarly, plugging $Q(2, -1, 3)$ into the plane equation and dividing by the normal length $\sqrt{2^2+(-2)^2+1^2}=3$ gives the distance $5/3$. Both formulas share the exact same structure because the shortest distance in both dimensions is the orthogonal projection of the point onto the normal direction.
