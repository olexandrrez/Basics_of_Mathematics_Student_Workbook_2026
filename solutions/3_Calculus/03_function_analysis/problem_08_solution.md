# Problem 8: The Second Derivative

## 1. Original Problem
For $f(x)=x^4-4x^2$, find local extrema, convexity/concavity, inflection points, and sketch with labels.

## 2. What We Are Trying to Find
The first derivative locates and classifies turning points. The second derivative describes curvature and identifies inflection points where curvature changes.

## 3. Key Idea or Theorem Needed Before the Calculation
Critical points satisfy $f'=0$. The sign of $f'$ gives increase/decrease; the sign of $f''$ gives concavity. An inflection point requires a change in concavity, not merely $f''=0$.

## 4. Step-by-Step Solution
$$f'=4x(x^2-2),$$
so critical points are $x=-\sqrt2,0,\sqrt2$. The sign pattern is $-,+,-,+$, giving minima at $\pm\sqrt2$ and a maximum at 0. Values are $f(\pm\sqrt2)=-4$, $f(0)=0$.

Next,
$$f''=12x^2-8=4(3x^2-2).$$
It is zero at $x=\pm\sqrt{2/3}$, negative between them and positive outside. Thus the graph is concave down on $(-\sqrt{2/3},\sqrt{2/3})$ and concave up on the two outer intervals. At each candidate the sign changes, so both are inflection points. Their height is $4/9-8/3=-20/9$.

## 5. Why Each Step Is Valid
Derivative sign changes classify the extrema. The second derivative changes sign at each inflection candidate, so curvature actually changes there.

## 6. Final Answer in Words
Local maximum $(0,0)$; minima $(\pm\sqrt2,-4)$. Inflections $(\pm\sqrt{2/3},-20/9)$. The graph is an even W-shaped quartic.

## 7. Quick Verification
The function is even, so extrema and inflection points occur symmetrically. As $|x|\to\infty$, the positive $x^4$ term makes both ends rise.

## 8. Common Mistakes
- Calling every root of $f''$ an inflection point without checking a sign change.
- Reversing the second-derivative sign when stating concavity.

## 9. Short In-Class Explanation
Use $f'$ for the three turning points, then $f''$ for curvature. The second derivative changes sign at plus and minus $\sqrt{2/3}$, giving two inflections and a symmetric W-shaped sketch.

```text
y       ╲                 ╱
↑        ╲               ╱
|         ╲             ╱
|          •           •   minima (±√2,−4)
|            ╲       ╱
|              • (0,0)
+-------------------------------→ x
```
