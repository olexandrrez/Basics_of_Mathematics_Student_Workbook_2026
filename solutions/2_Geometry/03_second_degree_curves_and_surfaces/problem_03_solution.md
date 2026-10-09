# Problem 03: Ellipse

## 1. Original Problem
For
$$\frac{x^2}{25}+\frac{y^2}{9}=1,$$
find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

## 2. What We Are Trying to Find
We must determine the semi-major and semi-minor axis lengths of the given canonical ellipse, find all four intercept points where the ellipse crosses the Cartesian axes, describe the shape of the graph, and explain why the ellipse is stretched more along the $x$-axis by referencing the denominators in the equation.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Canonical Equation of an Ellipse**:
  $$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1.$$
  - $a > 0$ is the horizontal semi-axis length along the $x$-axis.
  - $b > 0$ is the vertical semi-axis length along the $y$-axis.
- **Axis Intercepts**:
  - Setting $y = 0 \implies x^2/a^2 = 1 \implies x = \pm a$ (intercepts at $(\pm a, 0)$).
  - Setting $x = 0 \implies y^2/b^2 = 1 \implies y = \pm b$ (intercepts at $(0, \pm b)$).
- **Geometric Stretch Criterion**: The ellipse extends from $-a$ to $a$ horizontally (total width $2a$) and from $-b$ to $b$ vertically (total height $2b$). Whichever variable has the larger denominator corresponds to the axis along which the ellipse is more stretched.

## 4. Step-by-Step Solution

### Step 1: Identify Semiaxis Lengths
Compare $\frac{x^2}{25} + \frac{y^2}{9} = 1$ with $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$:
- $a^2 = 25 \implies a = \sqrt{25} = 5$.
- $b^2 = 9 \implies b = \sqrt{9} = 3$.
The horizontal semi-axis has length $a = 5$, and the vertical semi-axis has length $b = 3$.

### Step 2: Find the Coordinate Intercepts
1. **Intercepts with the $x$-axis (set $y = 0$)**:
   $$\frac{x^2}{25} + 0 = 1 \implies x^2 = 25 \implies x = \pm 5.$$
   The $x$-intercepts are $(-5, 0)$ and $(5, 0)$.
2. **Intercepts with the $y$-axis (set $x = 0$)**:
   $$0 + \frac{y^2}{9} = 1 \implies y^2 = 9 \implies y = \pm 3.$$
   The $y$-intercepts are $(0, -3)$ and $(0, 3)$.

### Step 3: Explain the Stretch Direction from the Equation
Notice that:
$$a = 5 > 3 = b.$$
The total horizontal width of the ellipse is $2a = 10$, while the total vertical height is $2b = 6$.
Because $10 > 6$, the ellipse is **more stretched along the $x$-axis** (horizontal elongation).

**How this is visible in the equation**:
In the equation $\frac{x^2}{25} + \frac{y^2}{9} = 1$, the denominator under $x^2$ is $25$, which is significantly larger than the denominator under $y^2$, which is $9$.
For each fraction to stay $\le 1$:
- The variable $x$ can range between $-5$ and $+5$ (since $x^2 \le 25$).
- The variable $y$ can only range between $-3$ and $+3$ (since $y^2 \le 9$).
The larger denominator directly grants the corresponding variable a wider range of allowed coordinates, stretching the ellipse along that axis.

## 5. Why Each Step Is Valid
- Setting a coordinate to zero isolates the intersection of the conic section with that coordinate axis.
- Taking the square root of positive denominators yields the exact boundary extents of the real locus.

## 6. Final Answer in Words
The horizontal semi-axis is $a = 5$ and the vertical semi-axis is $b = 3$. The four axis intercepts are $(\pm 5, 0)$ and $(0, \pm 3)$. The ellipse is stretched more along the $x$-axis because the denominator under $x^2$ ($25$) is larger than the denominator under $y^2$ ($9$), allowing $x$ to reach $\pm 5$ while restricting $y$ to $\pm 3$.

## 7. Quick Verification
- Check foci: $c = \sqrt{a^2 - b^2} = \sqrt{25 - 9} = \sqrt{16} = 4$. Foci are at $(\pm 4, 0)$ on the $x$-axis, confirming the major axis is horizontal.
- Check sum of focal distances for top vertex $(0, 3)$:
  $d_1 = \| (0, 3) - (-4, 0) \| = \sqrt{16 + 9} = 5$.
  $d_2 = \| (0, 3) - (4, 0) \| = \sqrt{16 + 9} = 5$.
  Sum: $d_1 + d_2 = 5 + 5 = 10 = 2a$.
  String definition of ellipse verified!

## 8. Common Mistakes
- Swapping the semiaxes with full axis lengths (reporting $a=25$ instead of $a=5$).
- Thinking the ellipse is centered away from $(0, 0)$ when there are no linear shift terms.

## 9. Short In-Class Explanation (3 Sentences)
Comparing the equation to canonical form gives horizontal semi-axis $a = 5$ and vertical semi-axis $b = 3$, leading to intercepts at $(\pm 5, 0)$ and $(0, \pm 3)$. The ellipse is stretched more along the $x$-axis because the denominator under $x^2$ is 25, which is larger than the denominator of 9 under $y^2$. This larger denominator allows $x$ to reach $\pm 5$ while $y$ can only reach $\pm 3$, producing a horizontally elongated oval.
