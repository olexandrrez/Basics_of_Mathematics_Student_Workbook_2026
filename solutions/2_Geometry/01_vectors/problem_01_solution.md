# Problem 01: Vector Operations and Their Meaning

## 1. Original Problem
For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute
$$u+v,\qquad u-v,\qquad 3u-2v.$$
Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

## 2. What We Are Trying to Find
We must compute componentwise vector addition, subtraction, and a linear combination of two 3D vectors $u$ and $v$, verify the algebraic identity $(u+v)-v = u$, and explain the geometric meaning of vector addition in space.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Componentwise Operations**: For vectors $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$ in $\mathbb{R}^3$,
  $$u \pm v = (u_1 \pm v_1, u_2 \pm v_2, u_3 \pm v_3),\qquad c u = (c u_1, c u_2, c u_3).$$
- **Geometric Meaning of Addition**: Adding vector $v$ to vector $u$ represents successive displacements (the triangle rule / tip-to-tail method): place the tail of $v$ at the tip of $u$; the sum $u+v$ is the resultant displacement from the tail of $u$ to the tip of $v$ (or the diagonal of the parallelogram they span).

## 4. Step-by-Step Solution

### Step 1: Compute $u + v$
Add corresponding components:
$$u+v = (2 + (-1), -1 + 4, 3 + 2) = (1, 3, 5).$$

### Step 2: Compute $u - v$
Subtract corresponding components:
$$u-v = (2 - (-1), -1 - 4, 3 - 2) = (2 + 1, -5, 1) = (3, -5, 1).$$

### Step 3: Compute $3u - 2v$
Scale each vector:
$$3u = 3(2, -1, 3) = (6, -3, 9),$$
$$2v = 2(-1, 4, 2) = (-2, 8, 4).$$
Now subtract:
$$3u - 2v = (6 - (-2), -3 - 8, 9 - 4) = (6 + 2, -11, 5) = (8, -11, 5).$$

### Step 4: Verify $(u+v) - v = u$
Take our computed sum $u+v = (1, 3, 5)$ and subtract $v = (-1, 4, 2)$:
$$(u+v)-v = (1 - (-1), 3 - 4, 5 - 2) = (1 + 1, -1, 3) = (2, -1, 3) = u.$$
The result identically matches the original vector $u$.

### Step 5: Geometric Explanation of Vector Addition
Geometrically, a vector represents a translation (displacement) in space with a specific magnitude and direction. Adding $u+v$ corresponds to applying translation $u$ first, and then from that new position applying translation $v$. Subtracting $v$ undoes the second displacement, returning you precisely to the endpoint of $u$. In the parallelogram formed by $u$ and $v$, $u+v$ is the main diagonal.

## 5. Why Each Step Is Valid
- Vectors in $\mathbb{R}^3$ form a real vector space where addition and scalar multiplication operate independently on Cartesian components.
- The group axiom $(u+v)-v = u+(v-v) = u+0 = u$ guarantees that subtraction is the inverse operation of addition.

## 6. Final Answer in Words
The results are $u+v = (1, 3, 5)$, $u-v = (3, -5, 1)$, and $3u-2v = (8, -11, 5)$. Subtracting $v$ from $u+v$ yields $(2, -1, 3) = u$. Geometrically, adding two vectors chains two displacements tip-to-tail, and subtracting $v$ reverses the second step to restore the original displacement $u$.

## 7. Quick Verification
- Check $(u - v) + v = (3, -5, 1) + (-1, 4, 2) = (2, -1, 3) = u$. Verified!
- Check $3u - 2v = u + 2(u - v) = (2, -1, 3) + 2(3, -5, 1) = (2+6, -1-10, 3+2) = (8, -11, 5)$. Verified!

## 8. Common Mistakes
- Sign errors when subtracting negative numbers: $2 - (-1) = 3$, not $1$.
- Multiplying the vector components together instead of taking linear combinations.

## 9. Short In-Class Explanation (3 Sentences)
We compute the operations componentwise, yielding $u+v = (1, 3, 5)$, $u-v = (3, -5, 1)$, and $3u-2v = (8, -11, 5)$. Subtracting $v$ from $u+v$ cancels $v$ and reproduces $u = (2, -1, 3)$ exactly. Geometrically, vector addition represents following one displacement after another tip-to-tail, so subtracting $v$ simply walks back the second displacement to return to the tip of $u$.
