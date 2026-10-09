# Problem 04: Dot Product and Perpendicularity

## 1. Original Problem
For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

## 2. What We Are Trying to Find
We must evaluate the dot product $u \cdot v$, use it to determine if $u$ and $v$ are perpendicular, solve for the unknown coordinate $a$ such that vector $w = (2, -1, a)$ is perpendicular to $u$, and verify the perpendicularity of $w$ and $u$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Dot Product Definition**: For vectors in $\mathbb{R}^3$,
  $$u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3.$$
- **Orthogonality (Perpendicularity) Criterion**: Two non-zero vectors $u$ and $v$ are perpendicular (orthogonal, $u \perp v$) if and only if their dot product is zero:
  $$u \perp v \iff u \cdot v = 0.$$
- **Why this holds**: Geometrically, $u \cdot v = \|u\| \|v\| \cos\theta$. For non-zero vectors, $u \cdot v = 0 \iff \cos\theta = 0 \iff \theta = 90^\circ$.

## 4. Step-by-Step Solution

### Step 1: Compute $u \cdot v$
For $u = (1, 2, -1)$ and $v = (2, -1, 3)$:
$$u \cdot v = (1)(2) + (2)(-1) + (-1)(3) = 2 - 2 - 3 = -3.$$

### Step 2: Determine Whether $u$ and $v$ Are Perpendicular
Since $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**.
(Since the dot product is negative, the angle between them is obtuse).

### Step 3: Find $a$ Such That $w \perp u$
We are given $w = (2, -1, a)$ and require $u \cdot w = 0$.
Write the dot product:
$$u \cdot w = (1)(2) + (2)(-1) + (-1)(a) = 2 - 2 - a = -a.$$
Set the dot product equal to zero:
$$-a = 0 \implies a = 0.$$

### Step 4: Check the Result
With $a = 0$, the vector is $w = (2, -1, 0)$.
Compute $u \cdot w$:
$$u \cdot w = (1)(2) + (2)(-1) + (-1)(0) = 2 - 2 + 0 = 0.$$
Since $u \cdot w = 0$, vector $w = (2, -1, 0)$ is strictly perpendicular to $u$.

## 5. Why Each Step Is Valid
- The dot product formula is an algebraic bilinear form that strictly reflects Euclidean geometry.
- Setting $u \cdot w = 0$ creates a linear algebraic equation in the single variable $a$, which has the unique solution $a = 0$.

## 6. Final Answer in Words
The dot product is $u \cdot v = -3$, so vectors $u$ and $v$ are not perpendicular. Vector $w = (2, -1, a)$ is perpendicular to $u$ when $a = 0$. Substituting $a = 0$ gives $w = (2, -1, 0)$, and computing $u \cdot w = 2 - 2 + 0 = 0$ confirms perpendicularity.

## 7. Quick Verification
- Angle between $u$ and $w$:
  $\|u\| = \sqrt{1 + 4 + 1} = \sqrt{6}$, $\|w\| = \sqrt{4 + 1 + 0} = \sqrt{5}$.
  $\cos\theta = \frac{u \cdot w}{\|u\|\|w\|} = \frac{0}{\sqrt{30}} = 0 \implies \theta = 90^\circ = \pi/2$.
  Verified.

## 8. Common Mistakes
- Arithmetic errors in summing negative products: $2 - 2 - 3 = -3$, not $+3$.
- Thinking that $u \cdot v = 0$ means the vectors are parallel instead of perpendicular.

## 9. Short In-Class Explanation (3 Sentences)
The dot product of $u$ and $v$ is $2 - 2 - 3 = -3$, which is non-zero, so the vectors are not perpendicular. Setting the dot product $u \cdot w$ equal to zero gives the equation $2 - 2 - a = 0$, which solves to $a = 0$. Substituting $a = 0$ into $w$ gives the vector $(2, -1, 0)$, whose dot product with $u$ is zero, confirming that it is perpendicular to $u$.
