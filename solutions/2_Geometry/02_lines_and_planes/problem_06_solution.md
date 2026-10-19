# Problem 06: Angle Between Planes

## 1. Original Problem
Given
$$\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.$$
First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

## 2. What We Are Trying to Find
We must determine if planes $\Pi_1$ and $\Pi_2$ are parallel by comparing their normal vectors, compute the dihedral angle $\theta$ between the planes, and explain the geometric theorem that the angle between two planes equals the angle between their normal vectors.

## 3. Key Idea or Theorem Needed Before the Calculation
- **Normal Vectors of Planes**: From Cartesian equations $A x + B y + C z + D = 0$, the normal vector is $n = (A, B, C)$.
- **Parallelism Criterion**: Two planes are parallel if and only if their normal vectors are proportional: $n_1 = c n_2$.
- **Dihedral Angle Between Planes**: The acute angle $\theta \in [0, \pi/2]$ between two planes equals the acute angle between their normal lines:
  $$\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\| \|n_2\|}.$$
- **Why normals suffice**: A rigid rotation cannot turn a plane into a line. Instead, take a cross-section perpendicular to the planes' intersection line. Each plane meets it in a line, and rotating those trace lines by $90^\circ$ gives directions parallel to the planes' normals while preserving their angle.

## 4. Step-by-Step Solution

### Step 1: Extract the Normal Vectors
From the plane equations:
- For $\Pi_1: 1x + 1y + 1z = 1$: normal vector is $n_1 = (1, 1, 1)$.
- For $\Pi_2: 1x - 1y + 0z = 2$: normal vector is $n_2 = (1, -1, 0)$.

### Step 2: Check for Parallelism
Check if $n_1 = c n_2$:
$$(1, 1, 1) = c(1, -1, 0) \implies c = 1, \text{ but } 1 = -c = -1, \text{ and } 1 = c(0) = 0.$$
This is contradictory. Because $n_1$ and $n_2$ are not scalar multiples, the planes are **not parallel**; they intersect along a line.

### Step 3: Compute the Angle Between the Planes
1. Compute the dot product:
   $$n_1 \cdot n_2 = (1)(1) + (1)(-1) + (1)(0) = 1 - 1 + 0 = 0.$$
2. Compute the norms:
   $$\|n_1\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3},$$
   $$\|n_2\| = \sqrt{1^2 + (-1)^2 + 0^2} = \sqrt{1 + 1} = \sqrt{2}.$$
3. Apply the cosine formula:
   $$\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\| \|n_2\|} = \frac{|0|}{\sqrt{3} \sqrt{2}} = 0.$$
4. Determine the angle $\theta$:
   $$\theta = \arccos(0) = \frac{\pi}{2} \quad (90^\circ).$$
The two planes are **perpendicular (orthogonal)**.

### Step 4: Explain Why Normal Vectors Alone Are Enough
Take a cross-section perpendicular to the intersection line. Each plane meets this cross-section in a line, called its trace. Rotating each trace line by $90^\circ$ in the cross-section gives a direction parallel to that plane's normal. A rotation preserves the angle between the two trace lines, so the angle between the normals equals the dihedral angle between the planes. The planes themselves remain two-dimensional throughout; only their cross-sectional traces are rotated.

## 5. Why Each Step Is Valid
- Normal vectors extract the gradient of the defining linear forms.
- The dot product evaluate to $0$, which by Cauchy-Schwarz and trigonometry uniquely implies an angle of $90^\circ$.

## 6. Final Answer in Words
The planes are not parallel because their normal vectors $n_1 = (1, 1, 1)$ and $n_2 = (1, -1, 0)$ are not proportional. The angle between them is $90^\circ$ ($\pi/2$ radians), meaning the planes are perpendicular. In a cross-section perpendicular to their intersection line, the planes become trace lines; rotating those lines by $90^\circ$ preserves their angle and gives directions parallel to the normals.

## 7. Quick Verification
- Let $v$ be the intersection line direction: $v = n_1 \times n_2 = (1, 1, -2)$.
  Check $v \cdot n_1 = 1 + 1 - 2 = 0$, $v \cdot n_2 = 1 - 1 + 0 = 0$.
  In the cross-section perpendicular to $v$, $n_1$ and $n_2$ are perpendicular ($n_1 \cdot n_2 = 0$), confirming that the dihedral angle is $90^\circ$.

## 8. Common Mistakes
- Omitting the absolute value $|n_1 \cdot n_2|$, which could incorrectly yield an obtuse angle (the angle between planes is conventionally defined as acute, $\le 90^\circ$).
- Reading $n_2$ as $(1, -1, 2)$ instead of $(1, -1, 0)$, forgetting that $z$ has coefficient 0.

## 9. Short In-Class Explanation (3 Sentences)
We extract the normal vectors $n_1=(1,1,1)$ and $n_2=(1,-1,0)$, whose dot product is zero, so the plane angle is $90^\circ$. To justify using normals, take a cross-section perpendicular to the planes' intersection line: each plane gives a trace line there. Rotating those trace lines by $90^\circ$ preserves their angle and makes their directions parallel to the normals.
