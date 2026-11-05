# Problem 1: Matrix Product and Sum Dimensions

## Problem

Let $A$ be $2\times3$, $B$ be $3\times2$, and $C$ be $2\times2$. State which of $AB$, $BA$, $A+C$, and $AB+C$ are defined and give their dimensions.

## Worked Solution

For a matrix product, the number of columns in the first matrix must equal the number of rows in the second. The product then has the outer dimensions. A sum is defined only for matrices of the same dimensions.

- $AB$ is defined because the inner dimensions are both $3$. Its size is the outer dimensions, $2\times2$.
- $BA$ is defined because the inner dimensions are both $2$. Its size is $3\times3$.
- $A+C$ is undefined: $A$ is $2\times3$ while $C$ is $2\times2$.
- $AB+C$ is defined because $AB$ is $2\times2$, matching the size of $C$. The sum is $2\times2$.

**Check.** Each product's inner dimensions match, and each proposed sum has matching row and column counts.
