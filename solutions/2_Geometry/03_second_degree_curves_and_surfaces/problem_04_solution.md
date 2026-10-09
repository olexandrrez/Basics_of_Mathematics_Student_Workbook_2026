# Problem 04: Parabola

## 1. Original Problem
For
$$y^2=12x,$$
identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x=3$ and use them to make a sketch.

## 2. What We Are Trying to Find
We must extract the geometric properties of the canonical parabola $y^2 = 12x$ (vertex, axis of symmetry, opening direction, focal parameter), calculate the corresponding $y$-values when $x = 3$, and describe the resulting parabolic curve.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Canonical Parabola Equation**:
  $$y^2 = 2px \quad (p > 0).$$
  - **Vertex**: At the origin $(0, 0)$.
  - **Axis of Symmetry**: The line $y = 0$ ($x$-axis), because substituting $-y$ gives $(-y)^2 = y^2$, leaving the equation unchanged.
  - **Opening Direction**: Since $y^2 \ge 0$ for all real $y$, $12x \ge 0 \implies x \ge 0$. The parabola exists only for non-negative $x$, meaning it opens towards the **positive $x$-axis** (to the right).
  - **Focal Parameter $p$**: $2p = 12 \implies p = 6$. The focus is at $(p/2, 0) = (3, 0)$, and the directrix line is $x = -p/2 = -3$.

## 4. Step-by-Step Solution

### Step 1: Identify Vertex, Axis, and Opening Direction
1. **Vertex**:
   Setting $x = 0$ gives $y^2 = 0 \implies y = 0$. The vertex is at the origin:
   $$V = (0, 0).$$
2. **Axis of Symmetry**:
   Replacing $y$ with $-y$ gives $(-y)^2 = 12x \implies y^2 = 12x$.
   Because the equation is symmetric with respect to sign changes in $y$, the axis of symmetry is the horizontal line:
   $$y = 0 \quad (\text{the } x\text{-axis}).$$
3. **Opening Direction**:
   Since $y^2 \ge 0$ for all real numbers $y$, we have $12x \ge 0 \implies x \ge 0$.
   The curve has no points in the left half-plane ($x < 0$); it opens to the **right** (towards positive $x$).

### Step 2: Find Points on the Parabola for $x = 3$
Substitute $x = 3$ into $y^2 = 12x$:
$$y^2 = 12(3) = 36.$$
Take the square root of both sides:
$$y = \pm \sqrt{36} = \pm 6.$$
The two corresponding points on the parabola are:
$$P_1 = (3, 6) \quad \text{and} \quad P_2 = (3, -6).$$

### Step 3: Geometric Description (Sketch Information)
- The vertex is at $(0, 0)$.
- The curve passes through $(3, 6)$ and $(3, -6)$, meaning that at distance $x = 3$ units from the vertex, the width of the parabola is $6 - (-6) = 12$ units.
- Notice that the focus is located at $(p/2, 0) = (3, 0)$. The segment connecting $(3, -6)$ to $(3, 6)$ is the **latus rectum** (focal chord perpendicular to the axis of symmetry), whose length is exactly $2p = 12$.
- The curve curves smoothly around the focus $(3, 0)$ and opens wider as $x \to \infty$.

## 5. Why Each Step Is Valid
- Solving $y^2 = 36$ yields the two symmetric real roots $\pm 6$.
- Parabolic focus-directrix property ensures that every point $(x, y)$ on the curve is equidistant from the focus $(3, 0)$ and the directrix line $x = -3$.

## 6. Final Answer in Words
The parabola has its vertex at $(0, 0)$, its axis of symmetry along the $x$-axis ($y = 0$), and opens to the right (positive $x$ direction). For $x = 3$, the points on the parabola are $(3, 6)$ and $(3, -6)$. These two points form the endpoints of the focal chord of length 12 through the focus $(3, 0)$.

## 7. Quick Verification
- Check focus-directrix distance definition for point $(3, 6)$:
  Distance to focus $(3, 0)$: $d_F = \sqrt{(3 - 3)^2 + (6 - 0)^2} = \sqrt{0 + 36} = 6$.
  Distance to directrix line $x = -3$: $d_D = |3 - (-3)| = 6$.
  Since $d_F = d_D = 6$, point $(3, 6)$ strictly satisfies the definition of the parabola.
- By symmetry, point $(3, -6)$ has distance $6$ to focus and directrix.

## 8. Common Mistakes
- Claiming the parabola opens upward (confusing $y^2 = 12x$ with $y = 12x^2$).
- Forgetting the negative root and reporting only the point $(3, 6)$ instead of both $(3, \pm 6)$.

## 9. Short In-Class Explanation (3 Sentences)
Because $y$ is squared and $x$ is linear with a positive coefficient, the parabola has its vertex at $(0, 0)$, axis of symmetry $y = 0$, and opens to the right. Substituting $x = 3$ gives $y^2 = 36$, yielding the symmetric points $(3, 6)$ and $(3, -6)$. These two points lie on the focal chord perpendicular to the axis, demonstrating that the curve expands outward around the focus $(3, 0)$.
