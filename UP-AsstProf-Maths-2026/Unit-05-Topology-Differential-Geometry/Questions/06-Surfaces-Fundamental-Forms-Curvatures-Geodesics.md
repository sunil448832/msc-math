# Unit 5 · Topic 06 — Surfaces: Fundamental Forms, Gaussian Curvature, Principal Curvatures, Geodesics
> Syllabus coverage: First and Second fundamental forms, Gaussian curvatures, Principal directions and principal curvatures, Geodesics
> Cheatsheet: [../Cheatsheets/06-Surfaces-Fundamental-Forms-Curvatures-Geodesics.md](../Cheatsheets/06-Surfaces-Fundamental-Forms-Curvatures-Geodesics.md)

*Notation: $I=E\,du^2+2F\,du\,dv+G\,dv^2$, $II=L\,du^2+2M\,du\,dv+N\,dv^2$, $K$ = Gaussian curvature, $H$ = mean curvature, $\kappa_1,\kappa_2$ = principal curvatures.*

**Q1.** `[Numerical]` ★ The Gaussian curvature of a sphere of radius $a$ is

(A) $\dfrac1a$

(B) $\dfrac2a$

(C) $\dfrac1{a^2}$

(D) $a^2$

**Q2.** `[Numerical]` ★★ The Gaussian curvature of the surface $z=x^2+3xy+5y^2$ at the origin is

(A) $11$

(B) $20$

(C) $-11$

(D) $1$

**Q3.** `[Concept]` ★ A connected surface every point of which is an umbilic is contained in

(A) a cylinder or a cone

(B) a plane or a sphere

(C) a surface of revolution

(D) a minimal surface

**Q4.** `[Match]` ★★ Match the surface (List-I) with its curvature description (List-II).

| List-I | List-II |
|---|---|
| A. Sphere | 1. $K=0,\ H=0$ |
| B. Circular cylinder | 2. $K<0,\ H=0$ |
| C. Plane | 3. $K>0$, every point umbilic |
| D. Catenoid | 4. $K=0,\ H\ne0$ |

(A) A-3, B-1, C-4, D-2

(B) A-3, B-4, C-1, D-2

(C) A-2, B-4, C-1, D-3

(D) A-3, B-4, C-2, D-1

**Q5.** `[Numerical]` ★★ For the torus $\mathbf r(u,v)=\big((3+\cos u)\cos v,\ (3+\cos u)\sin v,\ \sin u\big)$, the Gaussian curvature at points of the inner equator ($u=\pi$) is

(A) $-\tfrac12$

(B) $\tfrac14$

(C) $-\tfrac14$

(D) $\tfrac12$

**Q6.** `[Multi-Statement]` ★★ Consider:

I. The principal curvatures at a point are the eigenvalues of the shape operator (Weingarten map).

II. $K=\dfrac{LN-M^2}{EG-F^2}$.

III. $H=\dfrac{EN+GL-2FM}{EG-F^2}$.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q7.** `[Assertion-Reason]` ★★

**Assertion (A):** No region of a sphere can be mapped isometrically onto a region of the plane.

**Reason (R):** Gaussian curvature is invariant under local isometries (Theorema Egregium), and the sphere has $K=1/a^2\ne0$ while the plane has $K=0$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[NOT-true / Counterexample]` ★★ Which of the following curves on the right circular cylinder $x^2+y^2=a^2$ is NOT a geodesic?

(A) A ruling (generator) $x=x_0,\ y=y_0$

(B) A horizontal circle $z=c$

(C) A circular helix $(a\cos t, a\sin t, bt)$

(D) The ellipse cut out by the plane $z=x$

**Q9.** `[Application]` ★★★ A geodesic on a surface of revolution crosses a parallel of radius $2$ at an angle of $30^\circ$ with the meridian. By Clairaut's relation, the smallest possible distance of this geodesic from the axis of revolution is

(A) $\sqrt3$

(B) $1$

(C) $\tfrac12$

(D) $2$

**Q10.** `[Numerical]` ★ For the cone $\mathbf r(u,v)=(u\cos v,\ u\sin v,\ u)$, the coefficients $(E,F,G)$ of the first fundamental form are

(A) $(1,0,u^2)$

(B) $(2,0,2u^2)$

(C) $(2,0,u^2)$

(D) $(2,u,u^2)$

**Q11.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) $K=\kappa_1\kappa_2$

(B) $H=\tfrac12(\kappa_1+\kappa_2)$

(C) At a non-umbilic point the two principal directions are orthogonal.

(D) A minimal surface has $K\ge0$ at every point.

**Q12.** `[Numerical]` ★★★ For the helicoid $\mathbf r(u,v)=(u\cos v,\ u\sin v,\ v)$, the Gaussian curvature at the points with $u=1$ is

(A) $\tfrac14$

(B) $-\tfrac12$

(C) $-\tfrac14$

(D) $0$

**Q13.** `[Numerical]` ★★ At a point of a surface the principal curvatures are $\kappa_1=3$ and $\kappa_2=1$. The normal curvature in a direction making an angle of $60^\circ$ with the first principal direction is

(A) $\tfrac32$

(B) $\tfrac52$

(C) $2$

(D) $\tfrac{3+\sqrt3}{2}$

**Q14.** `[Concept]` ★ A unit-speed curve with non-vanishing curvature on a surface is a geodesic if and only if

(A) its principal normal is everywhere tangent to the surface

(B) its principal normal is everywhere parallel to the surface normal

(C) its normal curvature is identically zero

(D) its torsion is identically zero

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Numerical |
| 2 | A | Numerical |
| 3 | B | Concept |
| 4 | B | Match |
| 5 | A | Numerical |
| 6 | D | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | D | NOT-true |
| 9 | B | Application |
| 10 | C | Numerical |
| 11 | D | NOT-true |
| 12 | C | Numerical |
| 13 | A | Numerical |
| 14 | B | Concept |

## Solutions
**Q1 — (C).** $\kappa_1=\kappa_2=1/a$, so $K=1/a^2$. $1/a$ is the mean curvature (up to sign), and $2/a$ is $\kappa_1+\kappa_2$.

**Q2 — (A).** For a Monge patch $z=f(x,y)$, $K=\dfrac{f_{xx}f_{yy}-f_{xy}^2}{(1+f_x^2+f_y^2)^2}$. At the origin $f_x=f_y=0$, so $K=2\cdot10-3^2=11$ (checked with sympy). Option (B) forgets the $f_{xy}^2$ term.

**Q3 — (B).** If $\kappa_1=\kappa_2$ everywhere, then $dN=-\kappa\,d\mathbf r$ with $\kappa$ constant. If $\kappa=0$ the surface is a plane; otherwise it is a sphere of radius $1/|\kappa|$. A cylinder is not umbilic: its principal curvatures are $0$ and $1/a$.

**Q4 — (B).** Sphere: $\kappa_1=\kappa_2=1/a$. Cylinder: $\kappa_1=1/a$, $\kappa_2=0$, so $K=0$ and $H\ne0$. Plane: both principal curvatures are $0$. Catenoid: minimal ($H=0$) with $K=-\operatorname{sech}^4u<0$.

**Q5 — (A).** For the torus with radii $R,r$: $K=\dfrac{\cos u}{r(R+r\cos u)}$. With $R=3$, $r=1$, $u=\pi$: $K=\dfrac{-1}{1\cdot2}=-\tfrac12$ (saddle-like inner side). The outer equator gives $\tfrac14$, which is option (B).

**Q6 — (D).** I and II are standard. III is missing the factor 2: $H=\dfrac{EN-2FM+GL}{2(EG-F^2)}$.

**Q7 — (A).** An isometry preserves $E,F,G$, and $K$ depends only on these (Gauss). Since the two curvatures differ, no local isometry exists. This is exactly the reason why every flat map of the Earth distorts distances.

**Q8 — (D).** On the cylinder (locally isometric to the plane by unrolling), geodesics are the images of straight lines: rulings, parallels and helices. The ellipse $z=x$ unrolls to a sinusoid, not a line. Equivalently, its principal normal is not along the surface normal except at isolated points.

**Q9 — (B).** Clairaut: $\rho\sin\psi$ is constant, where $\rho$ is the distance from the axis and $\psi$ the angle with the meridian. Here $\rho\sin\psi=2\cdot\tfrac12=1$. Since $\sin\psi\le1$, $\rho\ge1$ along the geodesic, and $\rho=1$ when the geodesic runs tangent to a parallel. Option (A) uses $\cos30^\circ$.

**Q10 — (C).** $\mathbf r_u=(\cos v,\sin v,1)$, so $E=2$. $\mathbf r_v=(-u\sin v,u\cos v,0)$, so $G=u^2$. $F=\mathbf r_u\cdot\mathbf r_v=0$.

**Q11 — (D).** A minimal surface has $H=0$, so $\kappa_2=-\kappa_1$ and $K=-\kappa_1^2\le0$. (C) holds because the shape operator is self-adjoint.

**Q12 — (C).** For the helicoid $(u\cos v,u\sin v,cv)$, $K=-\dfrac{c^2}{(c^2+u^2)^2}$. With $c=1$, $u=1$: $K=-\tfrac14$ (sympy). The helicoid is a minimal surface, so $K<0$ everywhere, with $K=-1/c^2$ on the axis $u=0$. Option (B) forgets to square $c^2+u^2$.

**Q13 — (A).** Euler's theorem: $\kappa_n=\kappa_1\cos^2\theta+\kappa_2\sin^2\theta=3\cdot\tfrac14+1\cdot\tfrac34=\tfrac32$. Option (B) swaps $\cos^2$ and $\sin^2$.

**Q14 — (B).** A geodesic has zero geodesic curvature, so its acceleration $\mathbf r''=\kappa N_{\text{curve}}$ is normal to the surface. (C) describes **asymptotic** curves, and (D) describes planar curves.
