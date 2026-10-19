# Problem 12: Complete Model and Computer Verification

## 1. Original Problem
A rectangular room uses an existing wall for one side. The two perpendicular sides cost 300 PLN/m each, the opposite parallel side costs 500 PLN/m, and the budget is 30,000 PLN. Build and optimize the area model, state its domain, verify numerically, and describe the graph.

## 2. What We Are Trying to Find
We translate the physical layout and unequal side costs into a constraint, reduce area to one variable, and maximize it subject to positive dimensions.

## 3. Key Idea or Theorem Needed Before the Calculation
Two equal perpendicular sides of length $x$ cost $600x$ total; the side parallel to the wall, length $y$, costs $500y$. The budget constrains these lengths. The derivative and concavity then determine the optimum.

## 4. Step-by-Step Solution
Let $x>0$ be each side perpendicular to the wall, and $y>0$ be the third constructed side parallel to the wall. The budget equation is
$$600x+500y=30000.$$
Solve for $y$: $y=60-1.2x$. Positivity of $y$ gives $0<x<50$. The floor area is
$$A(x)=xy=x(60-1.2x)=60x-1.2x^2.$$
Differentiate: $A'=60-2.4x$, so the only critical point is $x=25$. Then $y=60-1.2(25)=30$. Area is 750 m$^2$. Since $A''=-2.4<0$, the graph is concave down, and area tends to zero at both domain boundaries, so this is the global maximum.

## 5. Why Each Step Is Valid
The constraint accounts for all three built sides and their stated prices. The domain enforces positive dimensions. Concavity and endpoint behavior verify the critical point is a maximum.

## 6. Final Answer in Words
Build perpendicular sides of length 25 m and the parallel side of length 30 m. The largest area is 750 m$^2$.

## 7. Quick Verification
Budget use is $600(25)+500(30)=15000+15000=30000$ PLN. Nearby areas are $A(24)=748.8$, $A(25)=750$, and $A(26)=748.8$ m$^2$.

## 8. Common Mistakes
- Charging for the wall side, which the problem says already exists.
- Using 300 PLN/m for the parallel side instead of 500 PLN/m.
- Treating the numerical checks as proof; the derivative and concavity establish optimality.

## 9. Short In-Class Explanation
The budget gives $y=60-1.2x$, so area is a downward parabola $60x-1.2x^2$. Its vertex is at $x=25$, giving $y=30$ and maximum area 750 m$^2$. The model comes from the geometry and prices; calculus optimizes it.

```text
A (m²)
750 |                 ● (25,750)
    |             ／       ＼
    |          ／             ＼
    |       ／                   ＼
  0 +●─────────────────────────────●→ x (m)
    0             25              50
```
