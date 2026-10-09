# Problem 06: Projection and Perpendicular Component

## 1. Original Problem
Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute
$$r=u-\operatorname{proj}_v u$$
and verify that $r\cdot v=0$. Explain this result geometrically.

## 2. What We Are Trying to Find
We must compute the orthogonal vector projection of $u$ onto $v$, find the residual difference vector $r = u - \operatorname{proj}_v u$, verify that $r$ is orthogonal to $v$ by computing their dot product, and interpret the resulting decomposition geometrically.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Vector Projection Formula**: The orthogonal projection of vector $u$ onto non-zero vector $v$ is:
  $$\operatorname{proj}_v u = \left(\frac{u \cdot v}{v \cdot v}\right) v = \left(\frac{u \cdot v}{\|v\|^2}\right) v.$$
- **Orthogonal Decomposition Theorem**: Any vector $u$ can be uniquely decomposed into a component parallel to $v$ and a component perpendicular to $v$:
  $$u = u_{\parallel} + u_{\perp}, \quad \text{where } u_{\parallel} = \operatorname{proj}_v u \text{ and } u_{\perp} = r = u - \operatorname{proj}_v u.$$
  By construction, $r \cdot v = 0$.

## 4. Step-by-Step Solution

### Step 1: Compute Dot Products
For $u = (4, 2)$ and $v = (1, 1)$:
- $u \cdot v = (4)(1) + (2)(1) = 4 + 2 = 6$.
- $v \cdot v = (1)^2 + (1)^2 = 1 + 1 = 2$.

### Step 2: Compute $\operatorname{proj}_v u$
Apply the projection formula:
$$\operatorname{proj}_v u = \left(\frac{u \cdot v}{v \cdot v}\right) v = \left(\frac{6}{2}\right) (1, 1) = 3(1, 1) = (3, 3).$$

### Step 3: Compute the Residual Vector $r$
$$r = u - \operatorname{proj}_v u = (4, 2) - (3, 3) = (4 - 3, 2 - 3) = (1, -1).$$

### Step 4: Verify That $r \cdot v = 0$
Compute the dot product of $r = (1, -1)$ and $v = (1, 1)$:
$$r \cdot v = (1)(1) + (-1)(1) = 1 - 1 = 0.$$
Because the dot product is $0$, vector $r$ is strictly perpendicular to vector $v$.

### Step 5: Geometric Explanation
Geometrically, imagine shining a light perpendicular to the line through $v$:
- $\operatorname{proj}_v u = (3, 3)$ is the **orthogonal shadow** (parallel component) cast by $u$ onto the line of $v$.
- $r = (1, -1)$ is the **perpendicular altitude vector** connecting the tip of the shadow on the line to the tip of $u$.
Together, they form a right-angled triangle with hypotenuse $u = (3, 3) + (1, -1) = (4, 2)$. The condition $r \cdot v = 0$ confirms that the residual vector is perpendicular to the direction of projection.

## 5. Why Each Step Is Valid
- The scalar $\frac{u \cdot v}{\|v\|^2}$ minimizes the distance $\|u - c v\|$ over all scalars $c \in \mathbb{R}$.
- The dot product $(u - c v) \cdot v = u \cdot v - c(v \cdot v) = u \cdot v - \frac{u \cdot v}{v \cdot v}(v \cdot v) = 0$ proves orthogonality algebraically.

## 6. Final Answer in Words
The projection of $u$ onto $v$ is $\operatorname{proj}_v u = (3, 3)$, and the perpendicular residual vector is $r = (1, -1)$. The dot product is $r \cdot v = 1 - 1 = 0$, confirming orthogonality. Geometrically, this decomposes vector $u$ into a component $(3, 3)$ parallel to $v$ and an altitude vector $(1, -1)$ perpendicular to $v$.

## 7. Quick Verification
- Check reconstruction: $\operatorname{proj}_v u + r = (3, 3) + (1, -1) = (4, 2) = u$. (True)
- Pythagorean theorem check: $\|u\|^2 = 4^2 + 2^2 = 20$.
  $\|\operatorname{proj}_v u\|^2 + \|r\|^2 = (3^2 + 3^2) + (1^2 + (-1)^2) = 18 + 2 = 20$.
  Pythagorean identity $\|u\|^2 = \|u_\parallel\|^2 + \|u_\perp\|^2$ holds exactly.

## 8. Common Mistakes
- Dividing by $\|v\| = \sqrt{2}$ instead of $\|v\|^2 = 2$ in the vector projection formula.
- Confusing scalar projection $\frac{u \cdot v}{\|v\|} = \frac{6}{\sqrt{2}} = 3\sqrt{2}$ with vector projection $(3, 3)$.

## 9. Short In-Class Explanation (3 Sentences)
We project $u = (4, 2)$ onto $v = (1, 1)$ using the formula $\frac{u \cdot v}{\|v\|^2} v = \frac{6}{2}(1, 1)$, which yields $(3, 3)$. Subtracting this projection from $u$ gives the perpendicular component $r = (1, -1)$. Computing the dot product $r \cdot v = 1 - 1 = 0$ confirms that $r$ is perpendicular to $v$, completing the orthogonal decomposition of $u$.
