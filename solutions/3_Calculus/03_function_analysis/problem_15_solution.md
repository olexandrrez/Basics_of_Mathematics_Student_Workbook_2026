# Problem 15: Find the Error in the Monotonicity Analysis

## 1. Original Problem
For $f(x)=x^3-3x$, the derivative is $f'(x)=3(x-1)(x+1)$. Explain why the student's sign chart is unsupported, correct it with test points, and classify extrema.

## 2. What We Are Trying to Find
We identify the sign of the derivative on all intervals determined by its zeros and then translate that sign chart into monotonicity and extrema.

## 3. Key Idea or Theorem Needed Before the Calculation
Zeros divide the real line into intervals, but the roots alone do not tell whether the derivative is positive or negative there. Factor signs or test values are needed.

## 4. Step-by-Step Solution
The critical values are $-1$ and 1. Test one point in each interval:
- At $x=-2$, $f'(-2)=3(-3)(-1)=9>0$.
- At $x=0$, $f'(0)=3(-1)(1)=-3<0$.
- At $x=2$, $f'(2)=3(1)(3)=9>0$.
Thus the correct sign pattern is $+,-,+$, not $-,+,-$ as the student claimed. Therefore $f$ increases on $(-\infty,-1)$, decreases on $(-1,1)$, and increases on $(1,\infty)$. At $-1$ it has a local maximum $f(-1)=2$; at 1 a local minimum $f(1)=-2$.

## 5. Why Each Step Is Valid
Each interval contains no root of the derivative, so its sign is constant there. One test point determines that sign throughout the interval. The derivative changes $+\to-$ at $-1$ and $-\to+$ at 1.

## 6. Final Answer in Words
The student's sign chart and extrema are reversed. The correct signs are positive, negative, positive, with local maximum $(−1,2)$ and local minimum $(1,−2)$.

## 7. Quick Verification
Directly evaluate the original function: $f(-1)=-1+3=2$ and $f(1)=1-3=-2$.

## 8. Common Mistakes
- Assuming a quadratic factored derivative is always positive between roots.
- Using the derivative zeros without checking the sign on intervals.

## 9. Short In-Class Explanation
Test $-2,0,2$ in the derivative. The signs are plus, minus, plus. So the function rises, falls, rises, giving a maximum at $-1$ and minimum at 1.
