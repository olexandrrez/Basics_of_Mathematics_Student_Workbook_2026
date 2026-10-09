# Problem 12: Recognizing a Surface from Cross-Sections

## 1. Original Problem
A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\text{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

## 2. What We Are Trying to Find
We are given geometric descriptions of planar cross-sections of an unknown 3D surface:
1. At height $z = 0$, the horizontal cross-section is a single point.
2. For any height $z > 0$, the horizontal cross-sections are circles whose radii increase as $z$ increases.
3. Every vertical slice containing the vertical $z$-axis ($Oz$) is a parabola.

We must formulate the simplest algebraic equation in $x, y, z$ satisfying all three conditions and provide a rigorous geometric justification.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Surfaces of Revolution**:
  If every horizontal cross-section $z = c$ is a circle centered on the $z$-axis, the surface possesses rotational symmetry about the $z$-axis and its equation depends on $x$ and $y$ only through the squared radial distance:
  $$r^2 = x^2 + y^2.$$
- **Profile Curve in Vertical Planes**:
  A vertical plane passing through the $Oz$ axis can be described in cylindrical coordinates by fixing the angle $\theta = \theta_0$. In this plane, the horizontal coordinate is the distance $r = \sqrt{x^2+y^2}$.
  If the profile curve is a parabola with its vertex at the origin opening upward, its equation must be:
  $$z = k r^2 \quad (k > 0).$$

## 4. Step-by-Step Solution

### Step 1: Propose the candidate equation
Choosing the simplest positive proportionality constant $k = 1$, we propose:
$$z = x^2 + y^2.$$

### Step 2: Verify Property 1 (cross-section at $z = 0$)
Substitute $z = 0$ into $z = x^2 + y^2$:
$$x^2 + y^2 = 0.$$
- Since $x^2 \ge 0$ and $y^2 \ge 0$ for all real numbers, the sum of two squares is zero if and only if both $x = 0$ and $y = 0$.
- In the three-dimensional space, the only point satisfying this is $(0, 0, 0)$.
- **Conclusion**: The cross-section at $z = 0$ is indeed the single point $(0, 0, 0)$, satisfying the first condition.

### Step 3: Verify Property 2 (cross-sections for $z > 0$)
Substitute a constant height $z = c$ where $c > 0$:
$$x^2 + y^2 = c.$$
- In the plane $z = c$, this equation defines a **circle** centered at $(0, 0, c)$ with radius:
  $$R(c) = \sqrt{c}.$$
- As $c$ increases, the derivative $\frac{dR}{dc} = \frac{1}{2\sqrt{c}} > 0$, meaning the radius $R(c)$ is strictly increasing.
- **Conclusion**: For every $z > 0$, the horizontal slices are circles with strictly increasing radius, satisfying the second condition.

### Step 4: Verify Property 3 (vertical cross-sections through $Oz$)
Any vertical plane passing through the $z$-axis ($Oz$) has the equation:
$$y = (\tan\theta) x \quad \text{or} \quad x = 0.$$
Let $\theta$ be the angle of the plane with the positive $x$-axis. We can parametrize any point in this plane by its signed distance $r$ from the $z$-axis:
$$x = r \cos\theta, \quad y = r \sin\theta.$$
Substitute these parametrizations into the proposed surface equation:
$$z = (r \cos\theta)^2 + (r \sin\theta)^2 = r^2 (\cos^2\theta + \sin^2\theta) = r^2.$$
- The equation relating height $z$ to radial distance $r$ in this vertical plane is:
  $$z = r^2.$$
- This is the standard equation of a **parabola** with vertex at $r = 0, z = 0$ opening upward.
- Because this holds for *every* choice of $\theta$, every vertical cross-section through the $Oz$ axis is an upward-opening parabola.
- **Conclusion**: The third condition is completely satisfied.

## 5. Why Each Step Is Valid
1. **Circular symmetry**: The term $x^2 + y^2$ guarantees that at any fixed $z$, the distance to the $z$-axis is constant, which is the definition of a circle.
2. **Pythagorean identity**: The identity $\cos^2\theta + \sin^2\theta = 1$ ensures that the vertical cross-section equation $z = r^2$ is independent of the rotation angle $\theta$, so every vertical profile through the axis is an identical parabola.
3. **Uniqueness of minimum**: Since $x^2 + y^2 \ge 0$, no real points exist for $z < 0$, making $z = 0$ the unique global vertex.

## 6. Final Answer in Words
The simplest equation for this surface is $z = x^2 + y^2$ (a circular paraboloid). At $z = 0$, the equation reduces to $x^2 + y^2 = 0$, giving the single point $(0, 0, 0)$. For any constant height $z = c > 0$, the horizontal cross-section is a circle $x^2 + y^2 = c$ with radius $R = \sqrt{c}$, which strictly increases with $z$. Finally, intersecting the surface with any vertical plane passing through the $z$-axis yields the upward-opening parabola $z = r^2$, fulfilling all required conditions.

## 7. Quick Verification
- Slicing with the $yz$-plane ($x = 0$): $z = y^2$ (a parabola).
- Slicing with the $xz$-plane ($y = 0$): $z = x^2$ (a parabola).
- Slicing with the diagonal plane $y = x$: $z = x^2 + x^2 = 2x^2$. Since radial distance is $r = x\sqrt{2}$, we have $z = (r/\sqrt{2})^2 \times 2 = r^2$ (the exact same parabola).
All cross-sections agree with the problem requirements.

## 8. Common Mistakes
- **Proposing a cone instead ($z = \sqrt{x^2+y^2}$)**: A cone also has point cross-section at $z=0$ and circles for $z>0$, but its vertical cross-sections are straight lines ($z = |r|$), not parabolas!
- **Proposing $z^2 = x^2 + y^2$**: This is a double cone, whose vertical cross-sections are straight lines, failing condition 3.
- **Forgetting that the radius must grow**: Proposing a cylinder $x^2 + y^2 = 1$, which does not have a single point at $z=0$ and whose radius does not increase.

## 9. Short In-Class Explanation (3 Sentences)
Because all horizontal slices are circles centered on the $z$-axis, the equation must involve the radial term $x^2+y^2$. Slicing by any vertical plane through the vertical axis gives a parabola with vertex at the origin, which establishes the quadratic relation $z = r^2 = x^2+y^2$. Therefore, the simplest equation matching all properties is the circular paraboloid $z = x^2+y^2$.
