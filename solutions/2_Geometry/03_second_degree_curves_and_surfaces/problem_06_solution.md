# Problem 06: Shifted Ellipse

## 1. Original Problem
Reduce
$$4x^2+9y^2-16x+18y-11=0$$
to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

## 2. What We Are Trying to Find
We need to:
1. Complete the square in both $x$ and $y$ to rewrite the general quadratic equation into canonical ellipse form $\frac{(x-x_0)^2}{a^2} + \frac{(y-y_0)^2}{b^2} = 1$.
2. State the center $(x_0, y_0)$ and the lengths of the horizontal and vertical semiaxes $a$ and $b$.
3. Substitute the center $(x_0, y_0)$ into the original left-hand expression to verify algebraic consistency with the completed-square form.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Completing the Square**:
  For an expression $A x^2 + B x$, factor out the leading coefficient $A$:
  $$A(x^2 + \frac{B}{A}x) = A\left[\left(x + \frac{B}{2A}\right)^2 - \left(\frac{B}{2A}\right)^2\right].$$
- **Canonical Form of a Translated Ellipse**:
  $$\frac{(x-x_0)^2}{a^2} + \frac{(y-y_0)^2}{b^2} = 1,$$
  where $(x_0, y_0)$ is the geometric center of symmetry, $a$ is the horizontal semiaxis, and $b$ is the vertical semiaxis.

## 4. Step-by-Step Solution

### Step 1: Group variables and factor out coefficients
Group the quadratic and linear terms for $x$ and $y$, moving the constant term to the right-hand side:
$$(4x^2 - 16x) + (9y^2 + 18y) = 11.$$
Factor out the leading coefficients of each variable:
$$4(x^2 - 4x) + 9(y^2 + 2y) = 11.$$

### Step 2: Complete the square inside each bracket
- For the $x$-terms: $x^2 - 4x = (x - 2)^2 - 4$.
- For the $y$-terms: $y^2 + 2y = (y + 1)^2 - 1$.

Substitute these into the equation:
$$4\left[(x - 2)^2 - 4\right] + 9\left[(y + 1)^2 - 1\right] = 11.$$

### Step 3: Expand the constants and isolate the squared binomials
Distribute the factors $4$ and $9$:
$$4(x - 2)^2 - 16 + 9(y + 1)^2 - 9 = 11.$$
Combine the numerical constants on the left:
$$-16 - 9 = -25.$$
Add $25$ to both sides of the equation:
$$4(x - 2)^2 + 9(y + 1)^2 = 11 + 25 = 36.$$

### Step 4: Divide by the right-hand side to obtain canonical form
Divide both sides of $4(x - 2)^2 + 9(y + 1)^2 = 36$ by $36$:
$$\frac{4(x - 2)^2}{36} + \frac{9(y + 1)^2}{36} = 1,$$
which simplifies to:
$$\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1.$$
Or, writing denominators as explicit squares:
$$\frac{(x - 2)^2}{3^2} + \frac{(y + 1)^2}{2^2} = 1.$$

### Step 5: Read off the geometric characteristics
- **Center**: $(x_0, y_0) = (2, -1)$.
- **Horizontal semiaxis**: $a = \sqrt{9} = 3$.
- **Vertical semiaxis**: $b = \sqrt{4} = 2$.

### Step 6: Verify by substituting the center into the original left-hand side
Let $L(x, y) = 4x^2 + 9y^2 - 16x + 18y - 11$.
Substitute $x = 2$ and $y = -1$:
$$L(2, -1) = 4(2)^2 + 9(-1)^2 - 16(2) + 18(-1) - 11.$$
Calculate each term:
- $4(4) = 16$
- $9(1) = 9$
- $-16(2) = -32$
- $18(-1) = -18$
- $-11$

Summing these up:
$$L(2, -1) = 16 + 9 - 32 - 18 - 11 = 25 - 61 = -36.$$

Notice that from our completed-square form:
$$L(x, y) = 4(x - 2)^2 + 9(y + 1)^2 - 36.$$
When $(x, y) = (2, -1)$, the squared terms vanish:
$$4(0)^2 + 9(0)^2 - 36 = -36.$$
The values match perfectly, confirming that the center is indeed $(2, -1)$ and the total constant offset is $-36$.

## 5. Why Each Step Is Valid
1. **Grouping and factoring**: Regrouping terms is allowed by associativity and commutativity of addition; factoring common scalar coefficients isolates monic quadratics.
2. **Completing the square**: The identity $(u - c)^2 = u^2 - 2cu + c^2$ allows replacing $u^2 - 2cu$ with $(u - c)^2 - c^2$ without changing values.
3. **Balancing equations**: Adding identical constants to both sides of an equality preserves the solution set.
4. **Dividing by 36**: Since $36 \neq 0$, division produces an equivalent equation with $1$ on the right side.
5. **Center substitution**: At the center of an ellipse, the deviations $(x-x_0)$ and $(y-y_0)$ are both zero, so the entire quadratic part vanishes, leaving solely the constant remainder $-36$.

## 6. Final Answer in Words
The canonical form of the equation is $\frac{(x - 2)^2}{9} + \frac{(y + 1)^2}{4} = 1$. It represents an ellipse centered at $(2, -1)$ with horizontal semi-major axis $a = 3$ and vertical semi-minor axis $b = 2$. Evaluating the original polynomial at the center yields $-36$, which precisely equals the negative of the constant $36$ required to balance the canonical form.

## 7. Quick Verification
- **Vertices along axes**:
  - Horizontal vertices: $(2 \pm 3, -1) = (5, -1)$ and $(-1, -1)$.
  - Test $(5, -1)$ in the original equation:
    $4(25) + 9(1) - 16(5) + 18(-1) - 11 = 100 + 9 - 80 - 18 - 11 = 109 - 109 = 0$.
  - Vertical vertices: $(2, -1 \pm 2) = (2, 1)$ and $(2, -3)$.
  - Test $(2, 1)$ in the original equation:
    $4(4) + 9(1) - 16(2) + 18(1) - 11 = 16 + 9 - 32 + 18 - 11 = 43 - 43 = 0$.
Both vertices satisfy the original equation, proving the center and semiaxes are accurate.

## 8. Common Mistakes
- **Forgetting to multiply the added square by the factored-out coefficient**: Writing $4(x-2)^2$ and only subtracting $4$ instead of $4 \times 4 = 16$.
- **Sign confusion in the center coordinates**: Thinking $(x - 2)^2$ means center coordinate $-2$, whereas $(x - x_0)^2$ means $x_0 = +2$, and $(y + 1)^2 = (y - (-1))^2$ means $y_0 = -1$.
- **Confusing semiaxes with diameters**: Taking $a=3$ to be the entire width instead of half the width.

## 9. Short In-Class Explanation (3 Sentences)
To find the canonical form, we factor out the leading coefficients and complete the square separately in $x$ and $y$. This translates the equation into $\frac{(x-2)^2}{9} + \frac{(y+1)^2}{4} = 1$, revealing an ellipse with center $(2, -1)$ and semiaxes $3$ and $2$. Substituting the center into the left-hand side makes the squared terms vanish, returning $-36$, which confirms our algebraic completion.
