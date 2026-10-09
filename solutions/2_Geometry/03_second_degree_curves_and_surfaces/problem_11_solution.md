# Problem 11: Two Similar Surfaces

## 1. Original Problem
Compare
$$x^2+y^2-z^2=1$$
and
$$x^2+y^2-z^2=-1.$$
For several values $z=c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

## 2. What We Are Trying to Find
We must compare two fundamental quadric surfaces:
1. $x^2 + y^2 - z^2 = 1$ (hyperboloid of one sheet).
2. $x^2 + y^2 - z^2 = -1$ (hyperboloid of two sheets).

Specifically, we will:
- Squeeze each surface with horizontal planes $z = c$ for test values of $c$ (such as $c = 0, \pm 1, \pm 2$).
- Determine whether a real cross-section exists and compute its radius.
- Explain the topological and geometric distinction between a single connected sheet versus two separated sheets.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Horizontal Cross-Sections ($z = c$)**:
  Rearranging each equation gives $x^2 + y^2$ as a function of the height $c$:
  - For $x^2 + y^2 - z^2 = 1$:
    $$x^2 + y^2 = 1 + c^2.$$
    Since $1 + c^2 \ge 1 > 0$ for all real $c$, every horizontal cross-section is a circle with radius $R(c) = \sqrt{1 + c^2}$.
  - For $x^2 + y^2 - z^2 = -1$:
    $$x^2 + y^2 = c^2 - 1.$$
    The existence of a real cross-section depends strictly on the sign of $c^2 - 1$:
    - If $|c| < 1$, then $c^2 - 1 < 0$, so no real points exist.
    - If $|c| = 1$, then $c^2 - 1 = 0$, giving a single point $(0, 0, \pm 1)$.
    - If $|c| > 1$, then $c^2 - 1 > 0$, giving a circle with radius $R(c) = \sqrt{c^2 - 1}$.

## 4. Step-by-Step Solution

### Surface 1: $x^2 + y^2 - z^2 = 1$

#### Step 1: Analyze cross-sections $z = c$
Rewrite the equation as $x^2 + y^2 = 1 + c^2$.
- **At $c = 0$ (the $xy$-plane)**:
  $$x^2 + y^2 = 1 + 0^2 = 1.$$
  This is a circle with minimum radius $R(0) = 1$. This circle is the "throat" or "waist" of the surface.
- **At $c = \pm 1$**:
  $$x^2 + y^2 = 1 + 1^2 = 2.$$
  This is a circle with radius $R(\pm 1) = \sqrt{2} \approx 1.414$.
- **At $c = \pm 2$**:
  $$x^2 + y^2 = 1 + 2^2 = 5.$$
  This is a circle with radius $R(\pm 2) = \sqrt{5} \approx 2.236$.
- **General behavior**: For every real value of $c \in (-\infty, \infty)$, a circle exists. Its radius increases smoothly and without bound as $|c| \to \infty$.

#### Step 2: Qualitative description
- The surface is unbroken, seamless, and connected. It resembles an hourglass or an upright cooling tower.
- Name: **Hyperboloid of one sheet** (single connected component).

---

### Surface 2: $x^2 + y^2 - z^2 = -1$

#### Step 1: Analyze cross-sections $z = c$
Rewrite the equation as $x^2 + y^2 = c^2 - 1$.
- **At $c = 0$ (the $xy$-plane)**:
  $$x^2 + y^2 = 0^2 - 1 = -1.$$
  Since squares of real numbers cannot sum to a negative number, **no real points exist** in this plane.
- **For $|c| < 1$ (e.g., $c = 0.5$)**:
  $$x^2 + y^2 = 0.25 - 1 = -0.75 < 0.$$
  There are **no real points** on the surface in the entire vertical slab $-1 < z < 1$.
- **At $c = \pm 1$**:
  $$x^2 + y^2 = 1^2 - 1 = 0.$$
  This yields the single isolated points $(0, 0, 1)$ and $(0, 0, -1)$, which are the two apexes (vertices) of the surface.
- **At $c = \pm 2$**:
  $$x^2 + y^2 = 2^2 - 1 = 3.$$
  This is a circle with radius $R(\pm 2) = \sqrt{3} \approx 1.732$.
- **General behavior**: Slices exist only when $|c| \ge 1$. For $|c| > 1$, the cross-sections are circles whose radii grow as $\sqrt{c^2 - 1}$.

#### Step 2: Qualitative description
- The surface is split into two completely separate, mirror-symmetric pieces: an upper bowl opening upward from $z = 1$ and a lower bowl opening downward from $z = -1$, separated by a completely empty gap of height $2$.
- Name: **Hyperboloid of two sheets** (two disconnected components).

## 5. Why Each Step Is Valid
1. **Level-set slicing**: Setting $z = c$ restricts the surface equation to a horizontal 2D plane, where the form $x^2 + y^2 = r$ can be evaluated by standard circle properties.
2. **Positivity of sum of squares**: For any real coordinates $(x, y)$, $x^2 + y^2 \ge 0$. Hence, a cross-section is non-empty if and only if the right-hand constant is non-negative.
3. **Topological distinction**: Because $1+c^2 > 0$ for all $c$, the first surface is connected across $z = 0$. Because $c^2-1 < 0$ for $|c|<1$, the second surface has a void, proving it has two disconnected sheets.

## 6. Final Answer in Words
For $x^2+y^2-z^2=1$, horizontal slices $z=c$ exist for every real number $c$ as circles of radius $\sqrt{1+c^2}$, with a minimum waist of radius $1$ at $z=0$, making it a connected **hyperboloid of one sheet**. For $x^2+y^2-z^2=-1$, horizontal slices do not exist for $|c|<1$, collapse to single points at $z=\pm 1$, and become circles of radius $\sqrt{c^2-1}$ only for $|c|>1$, creating two disconnected bowls known as a **hyperboloid of two sheets**.

## 7. Quick Verification
- For $x^2+y^2-z^2=1$: point $(1, 0, 0)$ satisfies $1^2 + 0^2 - 0^2 = 1$. The equator is non-empty.
- For $x^2+y^2-z^2=-1$: point $(0, 0, 1)$ satisfies $0^2 + 0^2 - 1^2 = -1$.
- Any attempt to find a point with $z = 0$ on the second surface yields $x^2 + y^2 = -1$, which has no real solutions.

## 8. Common Mistakes
- **Confusing the two names**: Forgetting whether $+1$ or $-1$ on the right side corresponds to one sheet or two sheets.
- **Assuming the throat of the one-sheet hyperboloid can close to zero**: Overlooking that $1 + c^2 \ge 1$, so the radius never drops below $1$.
- **Thinking the two-sheet hyperboloid is a cone**: Forgetting that its vertical cross-sections are hyperbolas, not straight lines, and that there is a finite gap between $z=-1$ and $z=1$.

## 9. Short In-Class Explanation (3 Sentences)
By rewriting the equations as $x^2+y^2=1+z^2$ and $x^2+y^2=z^2-1$, we see how their circular horizontal cross-sections behave. The first surface has circles for every height $z$, with a narrow waist of radius $1$ at $z=0$, forming a single connected hyperboloid of one sheet. The second surface has no real points between $z=-1$ and $z=1$, splitting into two separate upward and downward opening bowls called a hyperboloid of two sheets.
