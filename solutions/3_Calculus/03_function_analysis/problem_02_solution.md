# Problem 2: A Parabola from the Perspective of the Derivative

## 1. Original Problem
For $f(x)=x^2-4x+1$, find its minimum using the derivative and compare with vertex form.

## 2. What We Are Trying to Find
We locate the stationary point, determine whether it is a minimum, and verify the same result by completing the square.

## 3. Key Idea or Theorem Needed Before the Calculation
A sign change of $f'$ from negative to positive identifies a minimum. Completing the square writes a quadratic as a square plus a constant.

## 4. Step-by-Step Solution
Differentiate: $f'(x)=2x-4$. Solving $f'=0$ gives $x=2$. For $x<2$, $f'<0$; for $x>2$, $f'>0$, so the function decreases and then increases. Its value there is $f(2)=4-8+1=-3$.

Now complete the square:
$$x^2-4x+1=(x-2)^2-3.$$
Since $(x-2)^2\ge0$, the smallest possible value is $-3$, attained at $x=2$.

## 5. Why Each Step Is Valid
The derivative sign proves the turning direction; the square representation proves global minimality because a square cannot be negative.

## 6. Final Answer in Words
The minimum occurs at $(2,-3)$, as both methods show.

## 7. Quick Verification
Substituting $x=2$ into the original formula and vertex form gives $-3$ in both cases.

## 8. Common Mistakes
- Solving $f(x)=0$ instead of $f'(x)=0$ when seeking an extremum.
- Calling the critical point a minimum without a sign check or concavity argument.

## 9. Short In-Class Explanation
The derivative vanishes at 2 and changes from negative to positive, giving a minimum of $-3$. Completing the square gives $(x-2)^2-3$, which confirms the same vertex.
