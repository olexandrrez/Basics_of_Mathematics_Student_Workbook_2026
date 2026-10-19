# Problem 12: Symmetry, Sign, and Absolute Value

## 1. Original Problem
Compare $\int_{-2}^2x dx$ and $\int_{-2}^2|x|dx$. Predict from symmetry, calculate, and explain the difference.

## 2. What We Are Trying to Find
We compare signed accumulation for an odd function with positive area for its absolute value.

## 3. Key Idea or Theorem Needed Before the Calculation
The integral of an odd function over symmetric bounds is zero. An even function's integral over $[-a,a]$ is twice its integral over $[0,a]$.

## 4. Step-by-Step Solution
The function $x$ is odd, so its negative and positive halves cancel. Directly,
$$\int_{-2}^2x dx=\left[\frac{x^2}{2}\right]_{-2}^2=2-2=0.$$
The absolute value $|x|$ is even and nonnegative. Therefore
$$\int_{-2}^2|x|dx=2\int_0^2x dx=2\left[\frac{x^2}{2}\right]_0^2=4.$$
Each half forms a triangle of area 2; after absolute value both count positively.

## 5. Why Each Step Is Valid
Symmetry lets us pair opposite inputs. Absolute value reflects the negative half above the axis, changing cancellation into addition.

## 6. Final Answer in Words
The first integral is 0; the second is 4.

## 7. Quick Verification
The graph of $|x|$ has two congruent triangles, each area 2, giving total 4.

## 8. Common Mistakes
- Saying both integrals vanish because the interval is symmetric.
- Confusing signed integral with total area.

## 9. Short In-Class Explanation
The odd function $x$ cancels on symmetric bounds, so its integral is zero. The absolute value makes both sides nonnegative, and the two triangular areas add to 4.
