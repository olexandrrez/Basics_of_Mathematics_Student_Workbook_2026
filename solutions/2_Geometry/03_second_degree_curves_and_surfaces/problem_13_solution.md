# Problem 13: Intersection of a Sphere and a Plane

## 1. Original Problem
Given the sphere
$$x^2+y^2+z^2=25$$
and the plane $z=3$, find the equation of the intersection curve and its radius. Then describe what happens for $z=c$ depending on $c$.

## 2. What We Are Trying to Find
We must:
1. Find the algebraic equation describing the intersection curve of the sphere $x^2 + y^2 + z^2 = 25$ with the horizontal plane $z = 3$.
2. Calculate the radius of this intersection circle.
3. Analyze systematically how the intersection changes when slicing by an arbitrary horizontal plane $z = c$, categorizing the geometric outcomes based on the value of $c$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Intersection of a Sphere and a Plane**:
  A sphere centered at the origin with radius $R$ intersected by a plane $z = c$ perpendicular to the $z$-axis produces the system:
  $$\begin{cases} x^2 + y^2 + z^2 = R^2 \\ z = c \end{cases} \implies x^2 + y^2 = R^2 - c^2 \quad \text{in the plane } z = c.$$
- **Classification by the Discriminant Term $R^2 - c^2$**:
  - If $|c| < R$: The plane cuts through the interior of the sphere, creating a **circle** of radius $r = \sqrt{R^2 - c^2}$.
  - If $|c| = R$: The plane touches the sphere at a single tangent point $(0, 0, \pm R)$.
  - If $|c| > R$: The plane does not intersect the sphere; the intersection is **empty**.

## 4. Step-by-Step Solution

### Step 1: Find the intersection with the plane $z = 3$
The sphere has center $(0, 0, 0)$ and radius $R = \sqrt{25} = 5$.
Substitute $z = 3$ into the sphere equation:
$$x^2 + y^2 + 3^2 = 25.$$
Compute $3^2 = 9$ and subtract from $25$:
$$x^2 + y^2 + 9 = 25 \implies x^2 + y^2 = 25 - 9 = 16.$$
In the plane $z = 3$, this is:
$$x^2 + y^2 = 4^2.$$

### Step 2: Determine the geometric features of the intersection curve
- The curve is a **circle** lying entirely in the horizontal plane $z = 3$.
- **Center**: $C = (0, 0, 3)$.
- **Radius**: $r = \sqrt{16} = 4$.

### Step 3: Analyze the general horizontal plane $z = c$
Substitute $z = c$ into $x^2 + y^2 + z^2 = 25$:
$$x^2 + y^2 = 25 - c^2.$$
The nature of the solution set depends on the value of $25 - c^2$:

#### Case 1: $|c| < 5$ (i.e., $-5 < c < 5$)
- Here $c^2 < 25$, so $25 - c^2 > 0$.
- The intersection is a **circle** lying in the plane $z = c$ with center $(0, 0, c)$ and radius:
  $$r(c) = \sqrt{25 - c^2}.$$
- When $c = 0$, the plane passes through the equator, giving the maximal radius $r(0) = 5 = R$ (a great circle).
- As $|c|$ increases from $0$ to $5$, the radius $r(c)$ strictly decreases from $5$ toward $0$.

#### Case 2: $|c| = 5$ (i.e., $c = 5$ or $c = -5$)
- Here $c^2 = 25$, so $25 - c^2 = 0$:
  $$x^2 + y^2 = 0 \implies x = 0, y = 0.$$
- The plane is tangent to the sphere at exactly one point:
  - For $c = 5$: the north pole $(0, 0, 5)$.
  - For $c = -5$: the south pole $(0, 0, -5)$.

#### Case 3: $|c| > 5$ (i.e., $c > 5$ or $c < -5$)
- Here $c^2 > 25$, so $25 - c^2 < 0$:
  $$x^2 + y^2 = 25 - c^2 < 0.$$
- Since $x^2 + y^2 \ge 0$ for all real $x, y$, there are no real points satisfying this equality.
- The intersection is the **empty set** $\emptyset$; the plane does not meet the sphere.

## 5. Why Each Step Is Valid
1. **System of equations**: Points on the intersection curve must satisfy both the equation of the sphere and the equation of the plane simultaneously. Substituting $z = c$ reduces the 3D system to a single 2D relation.
2. **Pythagorean theorem**: In the right triangle formed by the sphere's center $(0,0,0)$, the circle's center $(0,0,c)$, and any point on the intersection circle, the hypotenuse is the sphere's radius $R = 5$, the height is $|c|$, and the base is the circle's radius $r$. Thus $r^2 + c^2 = R^2 \implies r = \sqrt{R^2 - c^2}$.
3. **Exhaustive trichotomy**: The real number $25 - c^2$ can only be strictly positive, zero, or strictly negative, covering all geometric cases completely.

## 6. Final Answer in Words
For the plane $z=3$, the intersection is a circle in the plane $z=3$ given by $x^2+y^2=16$ with center $(0, 0, 3)$ and radius $r = 4$. For a general plane $z=c$: if $|c|<5$, the intersection is a circle of radius $r=\sqrt{25-c^2}$; if $|c|=5$, the plane is tangent to the sphere at a single point $(0, 0, \pm 5)$; and if $|c|>5$, the plane misses the sphere and the intersection is empty.

## 7. Quick Verification
- Using the Pythagorean theorem: distance from origin to plane is $d = 3$. Sphere radius is $R = 5$.
- Radius of intersection: $r = \sqrt{R^2 - d^2} = \sqrt{5^2 - 3^2} = \sqrt{25 - 9} = \sqrt{16} = 4$.
- Test the point $(4, 0, 3)$:
  $$4^2 + 0^2 + 3^2 = 16 + 0 + 9 = 25.$$
  It lies on both the sphere and the plane $z = 3$.

## 8. Common Mistakes
- **Forgetting to state the plane**: Writing only $x^2 + y^2 = 16$ without noting that this curve lies in the plane $z = 3$ (in 3D, $x^2 + y^2 = 16$ alone describes a cylinder!).
- **Incorrect radius formula**: Writing $r = 25 - 9 = 16$ instead of taking the square root to get $r = 4$.
- **Ignoring negative values of $c$**: Writing the condition as $c < 5$ instead of $|c| < 5$, forgetting that planes below $z = -5$ also do not intersect the sphere.

## 9. Short In-Class Explanation (3 Sentences)
Substituting $z=3$ into the sphere equation yields $x^2+y^2=16$, which describes a circle of radius $4$ centered at $(0, 0, 3)$. By the Pythagorean theorem, slicing the sphere at any distance $|c|$ from the center produces a circle of radius $\sqrt{25-c^2}$. As a result, the intersection is a circle when $|c|<5$, a single tangent point when $|c|=5$, and empty when $|c|>5$.
