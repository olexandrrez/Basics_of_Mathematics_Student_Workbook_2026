# Problem 2: Maximum Area of a Rectangle

## 1. Original Problem
A rectangle has perimeter 40. Express area using one side, find the geometric domain, and determine and justify the maximum.

## 2. What We Are Trying to Find
We model the constraint to express the second side in terms of the first, then optimize area on the physically possible interval.

## 3. Key Idea or Theorem Needed Before the Calculation
The perimeter condition is $2x+2y=40$. For an interior maximum, solve $A'=0$ and verify with concavity or endpoint behavior.

## 4. Step-by-Step Solution
Let side lengths be $x,y>0$. The constraint gives $y=20-x$, so $0<x<20$. Area is
$$A(x)=xy=x(20-x)=20x-x^2.$$
Differentiate: $A'=20-2x$, which is zero at $x=10$. The second derivative $A''=-2$ is negative, so the parabola is concave down. The corresponding other side is $y=10$.

## 5. Why Each Step Is Valid
The domain follows from both side lengths being positive. Concavity down makes the stationary point a maximum; also the limiting areas at $x=0$ and $x=20$ are zero.

## 6. Final Answer in Words
The maximum area is 100 square units, achieved by a $10$ by $10$ square.

## 7. Quick Verification
The perimeter is $2(10)+2(10)=40$ and area is $10\cdot10=100$.

## 8. Common Mistakes
- Using $y=40-x$ instead of accounting for two pairs of sides.
- Including zero-length sides as rectangles with positive area.

## 9. Short In-Class Explanation
The perimeter gives $y=20-x$, so area is a downward quadratic. Its vertex is at $x=10$, yielding equal sides and area 100.
