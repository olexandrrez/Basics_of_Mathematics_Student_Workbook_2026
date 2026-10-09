# Problem 01: Recognizing Curves from Canonical Form

## 1. Original Problem
Recognize the curves
$$x^2+y^2=9,$$
$$\frac{x^2}{16}+\frac{y^2}{9}=1,$$
$$y^2=8x,$$
$$\frac{x^2}{9}-\frac{y^2}{4}=1.$$
For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

## 2. What We Are Trying to Find
We must classify each of the four second-degree conic sections in canonical form (circle, ellipse, parabola, hyperbola), determine their geometric characteristics (center, vertices, radii, semiaxes, axes of symmetry), describe their shapes, and explain how algebraic structural features reveal the curve type.

## 3. Key Idea or Theorem Needed Before the Calculation
- **General Conic Classification in Canonical Form**:
  1. $x^2 + y^2 = R^2$: **Circle** (both variables squared with equal positive coefficients).
  2. $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$: **Ellipse** (both variables squared with unequal positive coefficients).
  3. $y^2 = 2px$ or $x^2 = 2py$: **Parabola** (one variable squared, one linear).
  4. $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$: **Hyperbola** (both variables squared with opposite signs).

## 4. Step-by-Step Solution

### Curve 1: $x^2 + y^2 = 9$
- **Classification**: **Circle**.
- **Recognition**: Both $x$ and $y$ are squared, have identical positive coefficients ($1$), and sum to a positive constant.
- **Key Features**:
  - Center: $(0, 0)$.
  - Radius: $R = \sqrt{9} = 3$.
  - Intercepts: $(\pm 3, 0)$ and $(0, \pm 3)$.
- **Shape**: A perfectly round, symmetric closed loop of radius 3 centered at the origin.

### Curve 2: $\frac{x^2}{16} + \frac{y^2}{9} = 1$
- **Classification**: **Ellipse**.
- **Recognition**: Both $x$ and $y$ are squared, have positive but unequal denominators ($a^2 = 16 \neq 9 = b^2$), and sum to $1$.
- **Key Features**:
  - Center: $(0, 0)$.
  - Horizontal semi-major axis: $a = \sqrt{16} = 4$.
  - Vertical semi-minor axis: $b = \sqrt{9} = 3$.
  - Vertices on axes: $(\pm 4, 0)$ and $(0, \pm 3)$.
- **Shape**: A smooth, horizontally elongated oval, stretched further along the $x$-axis than the $y$-axis.

### Curve 3: $y^2 = 8x$
- **Classification**: **Parabola**.
- **Recognition**: One variable ($y$) is squared while the other ($x$) appears only to the first power (linearly).
- **Key Features**:
  - Vertex: $(0, 0)$.
  - Axis of symmetry: the $x$-axis ($y = 0$).
  - Opening direction: opens towards positive $x$ ($x \ge 0$ since $8x = y^2 \ge 0$).
  - Focal parameter: $2p = 8 \implies p = 4$, focus at $(p/2, 0) = (2, 0)$.
  - Test points: for $x = 2$, $y^2 = 16 \implies y = \pm 4$, so points $(2, 4)$ and $(2, -4)$ lie on the curve.
- **Shape**: An open, symmetric U-shaped curve lying entirely in the right half-plane ($x \ge 0$).

### Curve 4: $\frac{x^2}{9} - \frac{y^2}{4} = 1$
- **Classification**: **Hyperbola**.
- **Recognition**: Both $x$ and $y$ are squared, but their terms have opposite signs ($+$ for $x^2$, $-$ for $y^2$).
- **Key Features**:
  - Center: $(0, 0)$.
  - Transverse axis: the $x$-axis (since the positive term is $x^2$).
  - Vertices: $(\pm \sqrt{9}, 0) = (\pm 3, 0)$.
  - Asymptotes: $y = \pm \frac{b}{a} x = \pm \frac{2}{3} x$.
  - Semiaxis lengths: $a = 3, b = 2$.
- **Shape**: Two disconnected open branches opening left and right away from vertices $(-3, 0)$ and $(3, 0)$, approaching the lines $y = \pm \frac{2}{3}x$ as $|x| \to \infty$.

## 5. Why Each Step Is Valid
- The signs and degrees of the variables in second-degree Cartesian equations uniquely determine the affine and Euclidean equivalence classes of conic sections.
- Setting coordinates to zero isolates the exact axis intercepts and vertices.

## 6. Final Answer in Words
1. $x^2 + y^2 = 9$ is a circle of radius 3 centered at $(0, 0)$.
2. $\frac{x^2}{16} + \frac{y^2}{9} = 1$ is a horizontal ellipse centered at $(0, 0)$ with horizontal semi-axis 4 and vertical semi-axis 3.
3. $y^2 = 8x$ is a parabola opening to the right with vertex at $(0, 0)$ and axis $y = 0$.
4. $\frac{x^2}{9} - \frac{y^2}{4} = 1$ is a horizontal hyperbola with vertices at $(\pm 3, 0)$ and asymptotes $y = \pm \frac{2}{3}x$.
The curve type is recognized by checking whether both variables are squared (and if their signs are identical or opposite) or if only one variable is squared.

## 7. Quick Verification
- Check points:
  - $(0, 3)$ satisfies $0^2 + 3^2 = 9$.
  - $(4, 0)$ satisfies $16/16 + 0 = 1$.
  - $(2, 4)$ satisfies $4^2 = 8(2) = 16$.
  - $(3, 0)$ satisfies $9/9 - 0 = 1$.
  All test points satisfy their respective equations.

## 8. Common Mistakes
- Confusing which axis the hyperbola opens along: positive $x^2$ means it opens horizontally; positive $y^2$ means vertically.
- Misidentifying the parabola's opening direction (it opens towards $x > 0$, not upward along $y$).

## 9. Short In-Class Explanation (3 Sentences)
We recognize the curve type by inspecting the degrees and signs of the variables in each equation. The first two equations have both variables squared with positive coefficients, giving a circle when the coefficients are equal and an ellipse when they are unequal. The third equation is a parabola because only $y$ is squared, and the fourth is a hyperbola because the squared terms have opposite signs.
