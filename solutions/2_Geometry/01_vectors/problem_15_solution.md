# Problem 15: Comparing Directions Using the Cosine of the Angle

## 1. Original Problem
Given
$$a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).$$
For each pair, compute
$$\frac{u\cdot v}{\|u\|\, \|v\|}.$$
Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

## 2. What We Are Trying to Find
We must compute the normalized directional cosine $\cos\theta = \frac{u \cdot v}{\|u\| \|v\|}$ for all three pairs of vectors, rank the pairs in order of increasing angle between them, and explain why two vectors of different lengths can have a directional cosine of exactly $1$.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Cosine of the Angle Between Vectors**: For non-zero vectors $u$ and $v$,
  $$\cos\theta = \frac{u \cdot v}{\|u\| \|v\|}.$$
- **Monotonicity**: The function $\theta = \arccos(\cos\theta)$ is strictly decreasing: a larger cosine corresponds to a **smaller angle** ($0 \le \theta \le \pi$).
  - $\cos\theta = 1 \iff \theta = 0^\circ$ (vectors point in the exact same direction).
- **Collinearity**: If $v = k u$ with $k > 0$, the vectors point in the identical direction regardless of their magnitudes.

## 4. Step-by-Step Solution

### Step 1: Compute Vector Norms
For $a = (1, 2, 1)$, $b = (2, 4, 2)$, and $c = (2, 0, 3)$:
- $\|a\| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{1 + 4 + 1} = \sqrt{6}$.
- $\|b\| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6}$.
- $\|c\| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 0 + 9} = \sqrt{13}$.

### Step 2: Compute Dot Products and Cosines for Each Pair
1. **Pair $(a, b)$**:
   $$a \cdot b = (1)(2) + (2)(4) + (1)(2) = 2 + 8 + 2 = 12.$$
   $$\cos\theta_{ab} = \frac{a \cdot b}{\|a\| \|b\|} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1.$$
   Angle: $\theta_{ab} = \arccos(1) = 0^\circ$.

2. **Pair $(a, c)$**:
   $$a \cdot c = (1)(2) + (2)(0) + (1)(3) = 2 + 0 + 3 = 5.$$
   $$\cos\theta_{ac} = \frac{a \cdot c}{\|a\| \|c\|} = \frac{5}{\sqrt{6} \cdot \sqrt{13}} = \frac{5}{\sqrt{78}} \approx \frac{5}{8.8318} \approx 0.5661.$$
   Angle: $\theta_{ac} = \arccos(0.5661) \approx 55.52^\circ$.

3. **Pair $(b, c)$**:
   $$b \cdot c = (2)(2) + (4)(0) + (2)(3) = 4 + 0 + 6 = 10.$$
   $$\cos\theta_{bc} = \frac{b \cdot c}{\|b\| \|c\|} = \frac{10}{2\sqrt{6} \cdot \sqrt{13}} = \frac{10}{2\sqrt{78}} = \frac{5}{\sqrt{78}} \approx 0.5661.$$
   Angle: $\theta_{bc} = \arccos(0.5661) \approx 55.52^\circ$.

### Step 3: Order Pairs by Increasing Angle
The angles are:
$$\theta_{ab} = 0^\circ < \theta_{ac} = \theta_{bc} \approx 55.52^\circ.$$
In order of increasing angle:
$$\text{Pair } (a, b) \quad < \quad \text{Pair } (a, c) \;=\; \text{Pair } (b, c).$$

### Step 4: Explain Why $\cos\theta_{ab} = 1$ Despite Different Lengths
Notice that $b = (2, 4, 2) = 2(1, 2, 1) = 2a$.
Vector $b$ is a positive scalar multiple of $a$ ($k = 2 > 0$).
In the cosine formula:
$$\frac{a \cdot b}{\|a\| \|b\|} = \frac{a \cdot (2a)}{\|a\| \|2a\|} = \frac{2(a \cdot a)}{2 \|a\| \|a\|} = \frac{2 \|a\|^2}{2 \|a\|^2} = 1.$$
The scalar factor $2$ represents the length ratio and appears in both the numerator (dot product) and denominator (product of lengths), canceling out completely.
The cosine formula compares only the **directions** of the vectors, not their lengths. Since $a$ and $b$ point along the exact same ray, the angle between them is $0^\circ$, giving $\cos\theta = 1$.

## 5. Why Each Step Is Valid
- Cauchy-Schwarz inequality guarantees $-1 \le \frac{u \cdot v}{\|u\| \|v\|} \le 1$ with equality to $1$ if and only if $v = k u$ for $k > 0$.
- Because $b = 2a$, the vectors $a$ and $b$ share the identical unit vector $e_a = e_b = a/\|a\|$, so the angle formed with any third vector $c$ must be identical ($	heta_{ac} = \theta_{bc}$).

## 6. Final Answer in Words
The values are $\cos\theta_{ab} = 1$, $\cos\theta_{ac} = \frac{5}{\sqrt{78}} \approx 0.566$, and $\cos\theta_{bc} = \frac{5}{\sqrt{78}} \approx 0.566$. Ordered by increasing angle: pair $(a, b)$ has angle $0^\circ$, followed by pairs $(a, c)$ and $(b, c)$ which both have equal angles of approximately $55.52^\circ$. The cosine for $a$ and $b$ is $1$ because $b = 2a$ points in the exact same direction as $a$, and dividing by vector lengths normalizes the expression, canceling the length difference.

## 7. Quick Verification
- Compute unit vectors:
  $e_a = \frac{1}{\sqrt{6}}(1, 2, 1)$, $e_b = \frac{1}{2\sqrt{6}}(2, 4, 2) = \frac{1}{\sqrt{6}}(1, 2, 1) = e_a$.
  Since $e_a = e_b$, their dot product is $e_a \cdot e_a = 1$, and their dot products with $e_c$ must be identical: $e_a \cdot e_c = e_b \cdot e_c = 5/\sqrt{78}$.

## 8. Common Mistakes
- Reversing the order: thinking smaller cosine means smaller angle (cosine is decreasing, so larger cosine means smaller angle).
- Overlooking that $b = 2a$, which immediately implies $\theta_{ab} = 0^\circ$ and $\theta_{ac} = \theta_{bc}$.

## 9. Short In-Class Explanation (3 Sentences)
We compute the normalized dot products to find $\cos\theta = 1$ for $(a, b)$, and $\cos\theta = 5/\sqrt{78} \approx 0.566$ for both $(a, c)$ and $(b, c)$. In order of increasing angle, $(a, b)$ comes first with $0^\circ$, followed by $(a, c)$ and $(b, c)$ which share an angle of about $55.5^\circ$. The value for $a$ and $b$ is 1 because $b = 2a$ points in the exact same direction, and the formula normalizes lengths so that magnitude has no effect on the angle.
