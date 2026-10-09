# Problem 08: Sphere

## 1. Original Problem
Reduce
$$x^2+y^2+z^2-4x+2y-6z-2=0$$
to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

## 2. What We Are Trying to Find
We must:
1. Complete the square for all three spatial variables $x, y, z$ to transform the general equation into canonical sphere form:
   $$(x-x_0)^2 + (y-y_0)^2 + (z-z_0)^2 = R^2.$$
2. Identify the coordinates of the center $S = (x_0, y_0, z_0)$ and the radius $R > 0$.
3. Provide two concrete points lying on the sphere and verify that their coordinates satisfy the original equation.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Canonical Equation of a Sphere**:
  A sphere in $\mathbb{R}^3$ with center $S(x_0, y_0, z_0)$ and radius $R$ is defined by:
  $$(x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2 = R^2.$$
- **Completing the Square in Three Variables**:
  Apply $u^2 + 2ku = (u + k)^2 - k^2$ independently to $x, y,$ and $z$.

## 4. Step-by-Step Solution

### Step 1: Regroup terms by variable
Rearrange the equation by grouping each variable with its linear partner:
$$(x^2 - 4x) + (y^2 + 2y) + (z^2 - 6z) = 2.$$

### Step 2: Complete the square for each variable
- For $x$: $x^2 - 4x = (x - 2)^2 - 4$.
- For $y$: $y^2 + 2y = (y + 1)^2 - 1$.
- For $z$: $z^2 - 6z = (z - 3)^2 - 9$.

Substitute these into the regrouped equation:
$$\left[(x - 2)^2 - 4\right] + \left[(y + 1)^2 - 1\right] + \left[(z - 3)^2 - 9\right] = 2.$$

### Step 3: Combine constants on the right-hand side
Add $4 + 1 + 9 = 14$ to both sides:
$$(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 2 + 14 = 16.$$
Writing the right-hand side as a square:
$$(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 4^2.$$

### Step 4: Extract the center and radius
Comparing with $(x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2 = R^2$:
- **Center**: $S = (2, -1, 3)$.
- **Radius**: $R = \sqrt{16} = 4$.

### Step 5: Choose two points on the sphere
The simplest points to select are obtained by moving from the center by distance $R = 4$ along the principal coordinate directions:
1. **Point $P_1$ (shift along $x$-axis)**:
   $$P_1 = (2 + 4, -1, 3) = (6, -1, 3).$$
2. **Point $P_2$ (shift along $z$-axis)**:
   $$P_2 = (2, -1, 3 + 4) = (2, -1, 7).$$

### Step 6: Verify both points in the original equation
The original equation is $E(x, y, z) = x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0$.

- **Checking $P_1(6, -1, 3)$**:
  $$E(6, -1, 3) = 6^2 + (-1)^2 + 3^2 - 4(6) + 2(-1) - 6(3) - 2$$
  $$= 36 + 1 + 9 - 24 - 2 - 18 - 2$$
  $$= 46 - 46 = 0.$$
  Point $P_1$ satisfies the equation!

- **Checking $P_2(2, -1, 7)$**:
  $$E(2, -1, 7) = 2^2 + (-1)^2 + 7^2 - 4(2) + 2(-1) - 6(7) - 2$$
  $$= 4 + 1 + 49 - 8 - 2 - 42 - 2$$
  $$= 54 - 54 = 0.$$
  Point $P_2$ satisfies the equation!

## 5. Why Each Step Is Valid
1. **Grouping**: Commutativity of addition allows collecting each variable's terms separately.
2. **Completing the square**: Adding and subtracting $(B/2)^2$ creates a perfect square trinomial without altering the value of the expression.
3. **Translating along axes**: Since all points on a sphere have distance $R$ from the center, shifting only one coordinate by $R$ while keeping the other two equal to the center's coordinates guarantees a point on the sphere because $(R)^2 + 0^2 + 0^2 = R^2$.

## 6. Final Answer in Words
The canonical form of the equation is $(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16$. The sphere has center $S(2, -1, 3)$ and radius $R = 4$. Two points on this sphere are $P_1(6, -1, 3)$ and $P_2(2, -1, 7)$, both of which satisfy the original equation exactly.

## 7. Quick Verification
Calculate the Euclidean distance from the center $S(2, -1, 3)$ to $P_1(6, -1, 3)$:
$$d(S, P_1) = \sqrt{(6-2)^2 + (-1 - (-1))^2 + (3-3)^2} = \sqrt{4^2 + 0 + 0} = 4 = R.$$
Calculate the Euclidean distance from $S$ to $P_2(2, -1, 7)$:
$$d(S, P_2) = \sqrt{(2-2)^2 + (-1 - (-1))^2 + (7-3)^2} = \sqrt{0 + 0 + 4^2} = 4 = R.$$
Both distances equal the radius $4$.

## 8. Common Mistakes
- **Arithmetic errors when summing constants**: Forgetting to add one of the squared terms $(4, 1, \text{ or } 9)$ to the right-hand side.
- **Sign flip on center coordinates**: Thinking the center is $(-2, 1, -3)$ instead of $(+2, -1, +3)$.
- **Radius versus squared radius**: Stating that the radius is $16$ instead of $\sqrt{16} = 4$.

## 9. Short In-Class Explanation (3 Sentences)
We complete the square independently for $x$, $y$, and $z$, gathering all numerical constants on the right side to get $(x-2)^2 + (y+1)^2 + (z-3)^2 = 16$. This directly identifies the center as $(2, -1, 3)$ and the radius as $\sqrt{16} = 4$. By shifting the center along the coordinate axes by the radius, we obtain points like $(6, -1, 3)$ and $(2, -1, 7)$, which substitute back into the original equation to give zero.
