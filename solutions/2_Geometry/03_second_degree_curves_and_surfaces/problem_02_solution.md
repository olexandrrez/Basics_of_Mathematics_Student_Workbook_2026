# Problem 02: Circle by Completing the Square

## 1. Original Problem
Reduce
$$x^2+y^2-6x+4y-3=0$$
to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

## 2. What We Are Trying to Find
We must convert the general second-degree equation of a circle into standard canonical form $(x - x_0)^2 + (y - y_0)^2 = R^2$ by completing the square for $x$ and $y$, extract the coordinates of the center $(x_0, y_0)$ and radius $R$, identify two concrete points on the circle, and verify them in both equations.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Completing the Square Identity**:
  $$x^2 - 2hx = (x - h)^2 - h^2,\qquad y^2 + 2ky = (y + k)^2 - k^2.$$
- **Canonical Equation of a Circle**:
  $$(x - x_0)^2 + (y - y_0)^2 = R^2,$$
  where $(x_0, y_0)$ is the center and $R > 0$ is the radius.

## 4. Step-by-Step Solution

### Step 1: Group Variables and Complete the Square
Start with:
$$x^2 + y^2 - 6x + 4y - 3 = 0.$$
Group $x$ and $y$ terms together:
$$(x^2 - 6x) + (y^2 + 4y) - 3 = 0.$$
1. Complete the square for $x$:
   $$x^2 - 6x = (x - 3)^2 - 3^2 = (x - 3)^2 - 9.$$
2. Complete the square for $y$:
   $$y^2 + 4y = (y + 2)^2 - 2^2 = (y + 2)^2 - 4.$$

### Step 2: Assemble the Canonical Form
Substitute the completed squares back into the equation:
$$\left[(x - 3)^2 - 9\right] + \left[(y + 2)^2 - 4\right] - 3 = 0.$$
Combine the constant terms:
$$(x - 3)^2 + (y + 2)^2 - (9 + 4 + 3) = 0 \implies (x - 3)^2 + (y + 2)^2 - 16 = 0.$$
Move the constant to the right-hand side:
$$(x - 3)^2 + (y + 2)^2 = 16 = 4^2.$$
This is the **canonical form** of the circle.

### Step 3: Identify Center and Radius
Comparing with $(x - x_0)^2 + (y - y_0)^2 = R^2$:
- **Center**: $(x_0, y_0) = (3, -2)$.
- **Radius**: $R = \sqrt{16} = 4$.

### Step 4: Choose Two Simple Points and Verify in Both Forms
To find simple points on the circle, move distance $R = 4$ along the horizontal or vertical direction from the center $(3, -2)$:
1. **Point 1 (Top point, move $+4$ in $y$)**:
   $$P_1 = (3, -2 + 4) = (3, 2).$$
   - Check in canonical form:
     $$(3 - 3)^2 + (2 - (-2))^2 = 0^2 + (4)^2 = 16. \quad (\text{Matches})$$
   - Check in general form:
     $$3^2 + 2^2 - 6(3) + 4(2) - 3 = 9 + 4 - 18 + 8 - 3 = (13 - 18) + (8 - 3) = -5 + 5 = 0. \quad (\text{Matches})$$

2. **Point 2 (Rightmost point, move $+4$ in $x$)**:
   $$P_2 = (3 + 4, -2) = (7, -2).$$
   - Check in canonical form:
     $$(7 - 3)^2 + (-2 - (-2))^2 = 4^2 + 0^2 = 16. \quad (\text{Matches})$$
   - Check in general form:
     $$7^2 + (-2)^2 - 6(7) + 4(-2) - 3 = 49 + 4 - 42 - 8 - 3 = 53 - 53 = 0. \quad (\text{Matches})$$

Both points satisfy both forms of the equation.

## 5. Why Each Step Is Valid
- Completing the square is an exact algebraic identity: $(x - h)^2 - h^2 = x^2 - 2hx + h^2 - h^2 = x^2 - 2hx$.
- Adding and subtracting the same constants preserves numerical equality while revealing the geometric center.

## 6. Final Answer in Words
The canonical form of the circle is $(x - 3)^2 + (y + 2)^2 = 16$. The center of the circle is $(3, -2)$ and its radius is $4$. Two simple points on the circle are the top point $(3, 2)$ and the rightmost point $(7, -2)$. Substituting either point into both the canonical form and the original general equation yields valid equalities ($16 = 16$ and $0 = 0$).

## 7. Quick Verification
- Leftmost point $(3 - 4, -2) = (-1, -2)$:
  $(-1 - 3)^2 + 0 = 16$. General: $(-1)^2 + (-2)^2 - 6(-1) + 4(-2) - 3 = 1 + 4 + 6 - 8 - 3 = 11 - 11 = 0$.
- Bottom point $(3, -2 - 4) = (3, -6)$:
  $0 + (-6 + 2)^2 = 16$. General: $9 + 36 - 18 - 24 - 3 = 45 - 45 = 0$.
  All four cardinal points verify the circle.

## 8. Common Mistakes
- Sign errors for the center: writing $(x_0, y_0) = (-3, 2)$ instead of $(3, -2)$ (remember: $(x - x_0)$ means the coordinate is $+x_0$).
- Adding the completed constants instead of subtracting: writing $+9$ and $+4$ on the left side.

## 9. Short In-Class Explanation (3 Sentences)
We complete the square for $x$ and $y$ to rewrite the equation as $(x - 3)^2 + (y + 2)^2 = 16$. From this canonical form, we immediately read off the center $(3, -2)$ and radius $R = \sqrt{16} = 4$. Testing the top point $(3, 2)$ and rightmost point $(7, -2)$ confirms that both points satisfy both the canonical and original equations.
