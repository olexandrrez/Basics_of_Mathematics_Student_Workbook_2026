# Problem 3: A Box Made from Cardboard

## 1. Original Problem
Cut squares of side $x$ from a $30\text{ cm}\times40\text{ cm}$ sheet, fold up the sides, and find the cut size maximizing open-box volume.

## 2. What We Are Trying to Find
We must construct the volume model from the resulting dimensions, restrict it to physically possible cuts, and optimize it there.

## 3. Key Idea or Theorem Needed Before the Calculation
The box height equals the cut size; each base dimension loses two cut widths. Differentiate the volume function and discard critical values outside its physical domain.

## 4. Step-by-Step Solution
Dimensions are height $x$, length $40-2x$, width $30-2x$. Positivity requires $0<x<15$. The volume is
$$V(x)=x(30-2x)(40-2x)=1200x-140x^2+4x^3.$$
Then
$$V'(x)=1200-280x+12x^2=4(3x^2-70x+300).$$
Solving gives $x=(35\pm5\sqrt{13})/3$. The larger root is about 17.68, outside $0<x<15$. The valid root is $x_*=(35-5\sqrt{13})/3\approx5.657$ cm. It is the only critical point in the domain; volume tends to zero at both boundary limits and is positive inside, so this point maximizes it. The other dimensions are about 18.685 cm and 28.685 cm, giving volume approximately $3032.3\text{ cm}^3$.

## 5. Why Each Step Is Valid
The model multiplies the three perpendicular dimensions. The domain enforces positive height and base dimensions. The excluded stationary point cannot describe a physical box.

## 6. Final Answer in Words
Cut squares of side approximately 5.657 cm. This gives the maximum volume, approximately $3032.3\text{ cm}^3$.

## 7. Quick Verification
At the admissible root, all dimensions are positive. At either limiting cut size, at least one dimension collapses and volume tends to zero.

## 8. Common Mistakes
- Subtracting only $x$ rather than $2x$ from each base dimension.
- Keeping the derivative root outside the domain.

## 9. Short In-Class Explanation
The folded box has dimensions $x$, $30-2x$, and $40-2x$. Differentiate their product, keep only the critical cut size below 15 cm, and compare with zero volume at the domain ends.
