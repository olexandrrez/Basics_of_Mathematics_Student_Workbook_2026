# Problem 11: Decomposition into Parallel and Perpendicular Components

## 1. Original Problem
Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check
$$u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.$$
Explain why these are two independent checks of correctness.

## 2. What We Are Trying to Find
We must find the orthogonal decomposition of $u = (3, 4)$ with respect to $v = (1, 2)$ by finding $u_\parallel$ (parallel to $v$) and $u_\perp$ (perpendicular to $v$), verify the reconstruction identity $u = u_\parallel + u_\perp$, verify the orthogonality condition $u_\perp \cdot v = 0$, and explain why both checks are mathematically necessary.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Parallel Component (Vector Projection)**:
  $$u_\parallel = \operatorname{proj}_v u = \left(\frac{u \cdot v}{\|v\|^2}\right) v = \left(\frac{u \cdot v}{v \cdot v}\right) v.$$
- **Perpendicular Component (Orthogonal Complement)**:
  $$u_\perp = u - u_\parallel.$$
- **Two Independent Criteria**:
  1. **Reconstruction**: Verifies that the parts sum to the whole vector.
  2. **Orthogonality**: Verifies that $u_\perp$ is genuinely at a $90^\circ$ angle to $v$.

## 4. Step-by-Step Solution

### Step 1: Compute Dot Products
For $u = (3, 4)$ and $v = (1, 2)$:
- $u \cdot v = (3)(1) + (4)(2) = 3 + 8 = 11$.
- $v \cdot v = 1^2 + 2^2 = 1 + 4 = 5$.

### Step 2: Compute $u_\parallel$
Using the projection formula:
$$u_\parallel = \left(\frac{u \cdot v}{v \cdot v}\right) v = \frac{11}{5} (1, 2) = \left(\frac{11}{5}, \frac{22}{5}\right) = (2.2, 4.4).$$

### Step 3: Compute $u_\perp$
Subtract $u_\parallel$ from $u$:
$$u_\perp = u - u_\parallel = (3, 4) - \left(\frac{11}{5}, \frac{22}{5}\right) = \left(\frac{15 - 11}{5}, \frac{20 - 22}{5}\right) = \left(\frac{4}{5}, -\frac{2}{5}\right) = (0.8, -0.4).$$

### Step 4: Check 1 — Reconstruction
$$u_\parallel + u_\perp = \left(\frac{11}{5}, \frac{22}{5}\right) + \left(\frac{4}{5}, -\frac{2}{5}\right) = \left(\frac{11 + 4}{5}, \frac{22 - 2}{5}\right) = \left(\frac{15}{5}, \frac{20}{5}\right) = (3, 4) = u.$$
Check 1 passes: the components sum to $u$.

### Step 5: Check 2 — Orthogonality
Compute $u_\perp \cdot v$:
$$u_\perp \cdot v = \left(\frac{4}{5}\right)(1) + \left(-\frac{2}{5}\right)(2) = \frac{4}{5} - \frac{4}{5} = 0.$$
Check 2 passes: $u_\perp$ is orthogonal to $v$.

### Step 6: Why These Are Two Independent Checks
These two checks test two completely distinct mathematical requirements:
1. **The sum check ($u_\parallel + u_\perp = u$)** ensures that we have properly decomposed the original vector without losing or miscalculating components. However, this check alone does not guarantee that the components are perpendicular (e.g., choosing $u_\parallel = (1, 0)$ and $u_\perp = (2, 4)$ sums to $(3, 4)$, but $(2, 4)$ is not perpendicular to $v$).
2. **The orthogonality check ($u_\perp \cdot v = 0$)** ensures that $u_\perp$ is truly at $90^\circ$ to the direction of $v$. However, this check alone does not guarantee that the vectors sum to $u$ (e.g., choosing $u_\perp = (2, -1)$ satisfies $(2, -1) \cdot (1, 2) = 0$, but it does not sum to $u$).
Only when **both** conditions are verified simultaneously can we be certain that the decomposition is correct.

## 5. Why Each Step Is Valid
- Projection minimizes distance in Hilbert space, uniquely defining the parallel component.
- The orthogonality identity $(u - \frac{u \cdot v}{v \cdot v} v) \cdot v = u \cdot v - u \cdot v = 0$ holds identically.

## 6. Final Answer in Words
The components are $u_\parallel = (11/5, 22/5) = (2.2, 4.4)$ and $u_\perp = (4/5, -2/5) = (0.8, -0.4)$. Adding the two vectors reproduces $u = (3, 4)$, and computing the dot product $u_\perp \cdot v$ gives zero, verifying orthogonality. These checks are independent because the first confirms that the components add up to $u$, while the second confirms that the two directions are strictly perpendicular.

## 7. Quick Verification
- Check parallelism of $u_\parallel$: $(11/5, 22/5) = 2.2(1, 2) = 2.2 v$, which is parallel to $v$.
- Norm check: $\|u\|^2 = 3^2 + 4^2 = 25$.
  $\|u_\parallel\|^2 + \|u_\perp\|^2 = (121 + 484)/25 + (16 + 4)/25 = 605/25 + 20/25 = 625/25 = 25$.
  Pythagorean theorem confirmed.

## 8. Common Mistakes
- Miscomputing $u_\perp$ as $u_\parallel - u$ (giving the wrong sign).
- Checking only one condition and assuming the other follows automatically.

## 9. Short In-Class Explanation (3 Sentences)
We project $u = (3, 4)$ onto $v = (1, 2)$ to find the parallel component $u_\parallel = (11/5, 22/5)$, and subtract it from $u$ to obtain the perpendicular component $u_\perp = (4/5, -2/5)$. The first check confirms that their sum reconstructs the original vector $u = (3, 4)$. The second check confirms that the dot product $u_\perp \cdot v = 0$ is zero, guaranteeing that the two components are perpendicular.
