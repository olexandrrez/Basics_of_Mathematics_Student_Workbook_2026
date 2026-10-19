# Problem 05: Angle Between Vectors

## 1. Original Problem
Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

## 2. What We Are Trying to Find
We must determine the qualitative type of the angle between vectors $u$ and $v$ (acute, right, or obtuse) from the sign of their dot product, calculate the exact angle using the cosine formula, and compare the exact value with our qualitative prediction.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Dot Product Angle Formula**: For non-zero vectors $u$ and $v$,
  $$\cos\theta = \frac{u \cdot v}{\|u\| \|v\|}, \quad \theta \in [0, \pi].$$
- **Sign Interpretation of $u \cdot v$**: Since vector norms $\|u\|$ and $\|v\|$ are strictly positive:
  - $u \cdot v > 0 \implies \cos\theta > 0 \implies 0^\circ \le \theta < 90^\circ$. This includes $0^\circ$ when the vectors point in the same direction; an **acute** angle has $0^\circ < \theta < 90^\circ$.
  - $u \cdot v = 0 \implies \cos\theta = 0 \implies \theta = 90^\circ$ (**right angle**).
  - $u \cdot v < 0 \implies \cos\theta < 0 \implies 90^\circ < \theta \le 180^\circ$. This includes $180^\circ$ for opposite directions; an **obtuse** angle has $90^\circ < \theta < 180^\circ$.

## 4. Step-by-Step Solution

### Step 1: Compute the Dot Product and Predict Angle Type
For $u = (1, 1, 0)$ and $v = (1, 0, 1)$:
$$u \cdot v = (1)(1) + (1)(0) + (0)(1) = 1 + 0 + 0 = 1.$$
Since $u \cdot v = 1 > 0$, the cosine of the angle must be positive:
$$\cos\theta > 0.$$
**Prediction**: Since these vectors are not parallel, their positive dot product gives an **acute** angle ($0 < \theta < 90^\circ$).

### Step 2: Compute Vector Lengths
- Length of $u$:
  $$\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{1 + 1 + 0} = \sqrt{2}.$$
- Length of $v$:
  $$\|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{1 + 0 + 1} = \sqrt{2}.$$

### Step 3: Compute $\cos\theta$ and the Angle $\theta$
Apply the angle formula:
$$\cos\theta = \frac{u \cdot v}{\|u\| \|v\|} = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}.$$
Since $\cos\theta = \frac{1}{2}$ on the interval $[0, \pi]$:
$$\theta = \arccos\left(\frac{1}{2}\right) = \frac{\pi}{3} \quad (60^\circ).$$

### Step 4: Compare Result with Prediction
The calculated angle is $\theta = 60^\circ$.
Because $0^\circ < 60^\circ < 90^\circ$, this is an **acute angle**.
This matches our prediction that a positive dot product indicates an acute angle.

## 5. Why Each Step Is Valid
- The cosine function is strictly decreasing on $[0, \pi]$; $\cos\theta > 0$ strictly maps to the acute interval $(0, \pi/2)$.
- The value $\arccos(1/2) = \pi/3$ is a standard exact trigonometric value.

## 6. Final Answer in Words
The dot product is $u \cdot v = 1 > 0$, predicting an acute angle. Computing the lengths $\|u\| = \sqrt{2}$ and $\|v\| = \sqrt{2}$ yields $\cos\theta = 1/2$, which corresponds to an exact angle of $\theta = \pi/3$ radians ($60^\circ$). This confirms that the angle is acute.

## 7. Quick Verification
- Geometric perspective: $u = (1,1,0)$, $v = (1,0,1)$, and $w = (0,1,-1)$ form an equilateral triangle with vertices at $(0,0,0)$, $(1,1,0)$, $(1,0,1)$.
  Side lengths: $\|u\| = \sqrt{2}$, $\|v\| = \sqrt{2}$, $\|u - v\| = \|(0, 1, -1)\| = \sqrt{0 + 1 + 1} = \sqrt{2}$.
  All three sides have equal length $\sqrt{2}$, meaning the triangle formed by $u$ and $v$ from the origin is equilateral, so each interior angle is exactly $60^\circ$.

## 8. Common Mistakes
- Miscalculating the product of the norms: $\sqrt{2} \cdot \sqrt{2} = 2$, not $4$ or $\sqrt{2}$.
- Giving $\cos\theta = 1/2$ as the final answer without finding the angle $\theta = 60^\circ$.

## 9. Short In-Class Explanation (3 Sentences)
For nonzero vectors, a positive dot product gives an angle in $[0^\circ,90^\circ)$, with $0^\circ$ possible when the vectors point in the same direction. These particular vectors are not parallel, so their angle is strictly acute. Their lengths give $\cos\theta=1/2$, hence $\theta=60^\circ$.
