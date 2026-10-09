# Problem 09: Ellipsoid and Its Cross-Sections

## 1. Original Problem
Consider
$$\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.$$
Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

## 2. What We Are Trying to Find
We must:
1. Determine the three semiaxis lengths $a, b, c$ along the $x$, $y$, and $z$ axes.
2. Characterize the curve formed by intersecting the ellipsoid with the plane $z = 0$ (the $xy$-equatorial plane).
3. Analyze algebraically and geometrically the family of horizontal planar slices $z = c$ as $c$ varies within $(-4, 4)$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Canonical Ellipsoid**:
  $$\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1,$$
  where $a, b, c > 0$ are the lengths of the principal semiaxes.
- **Cross-Section by $z = \text{const}$**:
  Substituting $z = c$ into the 3D equation produces a 2D equation in $x$ and $y$:
  $$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 - \frac{c^2}{c_z^2}.$$
  Depending on the sign of the right-hand side:
  - If $1 - \frac{c^2}{c_z^2} > 0$, it is an ellipse scaled by $\sqrt{1 - c^2/c_z^2}$.
  - If $1 - \frac{c^2}{c_z^2} = 0$, it is a single point (the pole).
  - If $1 - \frac{c^2}{c_z^2} < 0$, the cross-section has no real points.

## 4. Step-by-Step Solution

### Step 1: Identify the semiaxis lengths
Write each denominator as an explicit square:
$$\frac{x^2}{3^2} + \frac{y^2}{2^2} + \frac{z^2}{4^2} = 1.$$
- Semiaxis along the $x$-axis: $a = \sqrt{9} = 3$.
- Semiaxis along the $y$-axis: $b = \sqrt{4} = 2$.
- Semiaxis along the $z$-axis: $c_z = \sqrt{16} = 4$.

### Step 2: Describe the cross-section $z = 0$
Set $z = 0$ in the equation:
$$\frac{x^2}{9} + \frac{y^2}{4} + \frac{0^2}{16} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1.$$
- In the plane $z = 0$, this is an **ellipse** centered at the origin $(0, 0, 0)$.
- Its semiaxes are $a = 3$ along the $x$-direction and $b = 2$ along the $y$-direction.
- This represents the maximum cross-section (the "equator") of the ellipsoid parallel to the $xy$-plane.

### Step 3: Analyze the general cross-sections $z = c$ for $|c| < 4$
Substitute an arbitrary constant height $z = c$ with $-4 < c < 4$:
$$\frac{x^2}{9} + \frac{y^2}{4} + \frac{c^2}{16} = 1.$$
Subtract $\frac{c^2}{16}$ from both sides:
$$\frac{x^2}{9} + \frac{y^2}{4} = 1 - \frac{c^2}{16}.$$
Since $|c| < 4$, we have $c^2 < 16$, which guarantees that:
$$k(c) = 1 - \frac{c^2}{16} > 0.$$
Divide both sides by $k(c)$:
$$\frac{x^2}{9 k(c)} + \frac{y^2}{4 k(c)} = 1.$$
This is an ellipse in the plane $z = c$ with:
- Center at $(0, 0, c)$.
- Horizontal semiaxis: $a(c) = 3\sqrt{1 - \frac{c^2}{16}}$.
- Vertical semiaxis: $b(c) = 2\sqrt{1 - \frac{c^2}{16}}$.

### Step 4: Geometric evolution as $c$ varies
1. **At $c = 0$**: The scaling factor $\sqrt{1 - c^2/16} = 1$, giving the largest ellipse with semiaxes $3$ and $2$.
2. **As $|c|$ increases toward $4$**: The factor $\sqrt{1 - c^2/16}$ strictly decreases toward $0$. The cross-sectional ellipses maintain the exact same aspect ratio ($a(c)/b(c) = 3/2$), shrinking homothetically.
3. **At the boundaries $c = \pm 4$**: The factor reaches $0$, so $x^2/9 + y^2/4 = 0$, shrinking the ellipse to the single points $(0, 0, 4)$ and $(0, 0, -4)$ (the north and south poles).
4. **For $|c| > 4$**: $1 - c^2/16 < 0$, meaning no real points exist, showing the ellipsoid is entirely bounded between $z = -4$ and $z = 4$.

## 5. Why Each Step Is Valid
1. **Reading canonical constants**: In canonical form $\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c_z^2}=1$, the denominators are directly the squares of the intercepts along the coordinate axes.
2. **Planar intersection**: Setting $z = c$ geometrically models the intersection of the surface with the horizontal plane $z = c$.
3. **Positivity of the RHS**: When $|c| < 4$, $c^2/16 < 1$, so $1 - c^2/16$ is strictly positive, ensuring the 2D locus is a non-degenerate ellipse.

## 6. Final Answer in Words
The ellipsoid has semiaxis lengths $3$ along the $x$-axis, $2$ along the $y$-axis, and $4$ along the $z$-axis. The cross-section with the plane $z=0$ is an ellipse $\frac{x^2}{9}+\frac{y^2}{4}=1$ with semiaxes $3$ and $2$. For any height $|c|<4$, each horizontal slice $z=c$ is a similar ellipse with scaled semiaxes $3\sqrt{1-c^2/16}$ and $2\sqrt{1-c^2/16}$, which smoothly shrink from their maximal size at $c=0$ down to single points at $c=\pm 4$.

## 7. Quick Verification
- At $c = 0$: semiaxes are $3\sqrt{1-0} = 3$ and $2\sqrt{1-0} = 2$.
- At $c = 2\sqrt{3}$ (where $c^2 = 12$): $1 - 12/16 = 1/4$, so $\sqrt{1 - c^2/16} = 1/2$. Semiaxes are $1.5$ and $1.0$.
- Test the point $(1.5, 0, 2\sqrt{3})$:
  $$\frac{(1.5)^2}{9} + 0 + \frac{12}{16} = \frac{2.25}{9} + \frac{3}{4} = \frac{1}{4} + \frac{3}{4} = 1.$$
The point lies precisely on the surface.

## 8. Common Mistakes
- **Confusing the semiaxis notation**: Denoting the vertical semiaxis as $c$ while also using $c$ as the slice plane $z = c$.
- **Believing the cross-sections are circles**: Overlooking that the denominators $9$ and $4$ are unequal, which makes all horizontal cross-sections genuine ellipses with ratio $3:2$, not circles.
- **Forgetting that the surface terminates at $|c| = 4$**: Not explaining that beyond $|c| = 4$ there are no real intersection points.

## 9. Short In-Class Explanation (3 Sentences)
The denominators immediately reveal that the ellipsoid has semiaxis lengths $3$, $2$, and $4$ along the $x$, $y$, and $z$ axes respectively. Slicing with the plane $z=0$ gives the equatorial ellipse $\frac{x^2}{9}+\frac{y^2}{4}=1$. For any plane $z=c$ with $|c|<4$, the cross-section is an ellipse with semiaxes scaled by $\sqrt{1-c^2/16}$, smoothly contracting to points at the poles $z=\pm 4$.
