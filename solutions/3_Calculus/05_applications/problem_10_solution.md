# Problem 10: A Cable Through Water and Land

## 1. Original Problem
A river is 100 m wide; point B is 500 m along the opposite bank from the point opposite A. Underwater cable costs twice as much per metre as land cable. Build and minimize a cost model.

## 2. What We Are Trying to Find
We choose the cable's exit point along the far bank, express underwater and land lengths using that variable, then minimize total cost.

## 3. Key Idea or Theorem Needed Before the Calculation
Use the Pythagorean theorem for the underwater diagonal. Convert different per-metre prices into a single cost function and optimize on the allowed interval.

## 4. Step-by-Step Solution
Let $x$ be the distance along the far bank from the point opposite A to the exit, toward B. Then $0\le x\le500$. Underwater distance is $\sqrt{100^2+x^2}$; land distance is $500-x$. Measure cost in units of land price per metre, making underwater unit cost 2. Thus
$$C(x)=2\sqrt{10000+x^2}+500-x.$$
Differentiate:
$$C'(x)=\frac{2x}{\sqrt{10000+x^2}}-1.$$
Set to zero: $2x=\sqrt{10000+x^2}$. Squaring (both sides nonnegative) gives $4x^2=10000+x^2$, so $3x^2=10000$ and $x=100/\sqrt3\approx57.7$ m. The derivative is negative at zero and positive by 500; there is only this critical point, so it minimizes cost.

## 5. Why Each Step Is Valid
The variable's interval follows from placing the exit between the opposite point and B. The derivative balances the marginal extra underwater cost against the saved land cost.

## 6. Final Answer in Words
The cable should emerge about 57.7 m along the far bank from the point directly across from A.

## 7. Quick Verification
The critical point is inside $[0,500]$. $C'(0)=-1$ and $C'(500)>0$, confirming the cost first decreases then increases.

## 8. Common Mistakes
- Charging the same rate for both route segments.
- Using $x$ for the remaining land distance while also using it for the exit offset.
- Squaring without confirming nonnegative sides (here both are nonnegative).

## 9. Short In-Class Explanation
Let $x$ be the exit offset. The underwater diagonal is $\sqrt{10000+x^2}$ and remaining land is $500-x$. Weight water twice as much, differentiate, and the minimum occurs at $x=100/\sqrt3$ m.
