# Unit 7 · Topic 01 — Calculus of Variations
> Syllabus coverage: Calculus of variations – Linear functionals, Necessary and sufficient conditions for extrema, Euler–Lagrange equation
> Cheatsheet: [../Cheatsheets/01-Calculus-of-Variations.md](../Cheatsheets/01-Calculus-of-Variations.md)

**Q1.** `[Concept]` ★ A necessary condition for $y(x)$ to extremize $J[y]=\int_a^b F(x,y,y')\,dx$ with fixed end points is

(A) $\dfrac{\partial F}{\partial y}+\dfrac{d}{dx}\left(\dfrac{\partial F}{\partial y'}\right)=0$

(B) $\dfrac{\partial F}{\partial x}-\dfrac{d}{dx}\left(\dfrac{\partial F}{\partial y'}\right)=0$

(C) $\dfrac{\partial F}{\partial y'}-\dfrac{d}{dx}\left(\dfrac{\partial F}{\partial y}\right)=0$

(D) $\dfrac{\partial F}{\partial y}-\dfrac{d}{dx}\left(\dfrac{\partial F}{\partial y'}\right)=0$

**Q2.** `[Numerical]` ★ The extremal of $J[y]=\displaystyle\int_0^1\left(y'^2+12xy\right)dx$, $y(0)=0,\ y(1)=1$, is

(A) $y=x^2$

(B) $y=x$

(C) $y=x^3$

(D) $y=\dfrac{x^3+x}{2}$

**Q3.** `[Numerical]` ★★ The extremal of $J[y]=\displaystyle\int_0^{\pi/2}\left(y'^2-y^2+2xy\right)dx$, $y(0)=0,\ y(\pi/2)=0$, is

(A) $y=x-\dfrac{\pi}{2}\sin x$

(B) $y=x+\dfrac{\pi}{2}\sin x$

(C) $y=x-\dfrac{\pi}{2}\cos x$

(D) $y=\sin x-\dfrac{2x}{\pi}$

**Q4.** `[Concept]` ★ If the integrand $F(y,y')$ does not contain $x$ explicitly, the Euler–Lagrange equation has the first integral

(A) $F_{y'}=\text{const}$

(B) $F+y'F_{y'}=\text{const}$

(C) $F-y'F_{y'}=\text{const}$

(D) $F-yF_{y}=\text{const}$

**Q5.** `[Match]` ★★ Match the variational problem (List-I) with its extremal curve (List-II).

| List-I | List-II |
|---|---|
| (a) Brachistochrone (curve of fastest descent) | 1. Circle |
| (b) Surface of revolution of minimum area | 2. Helix |
| (c) Closed curve of given length enclosing maximum area | 3. Cycloid |
| (d) Geodesic on a right circular cylinder (generic) | 4. Catenary |

(A) a-3, b-4, c-1, d-2

(B) a-4, b-3, c-1, d-2

(C) a-3, b-1, c-4, d-2

(D) a-3, b-4, c-2, d-1

**Q6.** `[Multi-Statement]` ★★ For $J[y]=\int_a^b F(x,y,y')\,dx$ with fixed ends, consider an extremal $y_0$.

I. $F_{y'y'}\ge 0$ along $y_0$ is necessary for $y_0$ to give a weak minimum (Legendre).

II. $F_{y'y'}>0$ along $y_0$ is, by itself, sufficient for a weak minimum.

III. If $F_{y'y'}>0$ along $y_0$ and the interval $(a,b]$ contains no point conjugate to $a$, then $y_0$ gives a weak minimum (Jacobi).

Which are correct?

(A) I only

(B) I and II only

(C) I, II and III

(D) I and III only

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** The extremal of $\int_0^1 y'^2\,dx$ with $y(0)=0$ and $y(1)$ free is $y\equiv 0$.
**Reason (R):** At a free end point the natural boundary condition $\partial F/\partial y'=0$ must hold.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[NOT-true / Counterexample]` ★ Which of the following is NOT a linear functional on $C^1[0,1]$?

(A) $J[y]=\int_0^1 x\,y'(x)\,dx$

(B) $J[y]=y(0)+2y'(1)$

(C) $J[y]=\int_0^1 y(x)^2\,dx$

(D) $J[y]=\int_0^1 \left(e^x y+\sin x\,y'\right)dx$

**Q9.** `[Numerical]` ★★★ Among all $y\in C^2[0,1]$ with $y(0)=y(1)=0$ and $\int_0^1 y\,dx=1$, the minimum value of $\int_0^1 y'^2\,dx$ is

(A) $6$

(B) $12$

(C) $36$

(D) $4$

**Q10.** `[Concept]` ★ The Euler–Poisson equation for $J[y]=\int_a^b F(x,y,y',y'')\,dx$ is

(A) $F_y-\dfrac{d}{dx}F_{y'}-\dfrac{d^2}{dx^2}F_{y''}=0$

(B) $F_y+\dfrac{d}{dx}F_{y'}+\dfrac{d^2}{dx^2}F_{y''}=0$

(C) $F_y-\dfrac{d^2}{dx^2}F_{y''}=0$

(D) $F_y-\dfrac{d}{dx}F_{y'}+\dfrac{d^2}{dx^2}F_{y''}=0$

**Q11.** `[Application]` ★★★ For $J[y]=\displaystyle\int_0^1\left(y^2+2xyy'\right)dx$ with $y(0)=0,\ y(1)=2$, which statement is true?

(A) The unique extremal is $y=2x$

(B) The Euler–Lagrange equation holds identically and $J[y]=4$ for every admissible $y$

(C) No admissible curve satisfies the Euler–Lagrange equation

(D) The Euler–Lagrange equation holds identically and $J[y]=2$ for every admissible $y$

**Q12.** `[Numerical]` ★★ For $J[y,z]=\displaystyle\int_a^b\left(y'^2+z'^2+2yz\right)dx$, the extremals satisfy

(A) $y''-y=0$

(B) $y^{(4)}+y=0$

(C) $y^{(4)}-y=0$

(D) $y''+y=0$

**Q13.** `[Numerical]` ★★★ For $J[y]=\int_0^a\left(y'^2-y^2\right)dx$, $y(0)=0,\ y(a)=0$, the point conjugate to $x=0$ (along the extremal $y\equiv0$) is

(A) $\pi/2$

(B) $\pi$

(C) $2\pi$

(D) there is no conjugate point

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | C | Numerical |
| 3 | A | Numerical |
| 4 | C | Concept |
| 5 | A | Match |
| 6 | D | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | C | NOT-true / Counterexample |
| 9 | B | Numerical |
| 10 | D | Concept |
| 11 | B | Application |
| 12 | C | Numerical |
| 13 | B | Numerical |

## Solutions
**Q1 — (D).** Euler–Lagrange: $F_y-\frac{d}{dx}F_{y'}=0$. (A) has the wrong sign; (C) swaps the roles of $y$ and $y'$.

**Q2 — (C).** $F_y=12x$, $F_{y'}=2y'$ ⇒ $12x-2y''=0$ ⇒ $y''=6x$ ⇒ $y=x^3+c_1x+c_2$. $y(0)=0\Rightarrow c_2=0$; $y(1)=1\Rightarrow c_1=0$. (D) satisfies the BCs but not $y''=6x$.

**Q3 — (A).** $F_y=-2y+2x$, $F_{y'}=2y'$ ⇒ $y''+y=x$ ⇒ $y=x+A\cos x+B\sin x$. $y(0)=0\Rightarrow A=0$; $y(\pi/2)=0\Rightarrow \pi/2+B=0$. A sign slip in the particular integral gives (B).

**Q4 — (C).** Beltrami identity: $\frac{d}{dx}(F-y'F_{y'})=F_x=0$. (A) is the first integral when $y$ (not $x$) is absent.

**Q5 — (A).** Brachistochrone → cycloid; minimal surface of revolution → catenary (catenoid); isoperimetric → circle; geodesics on a cylinder → helices (special cases: generators and circles).

**Q6 — (D).** Legendre's condition is necessary only. Strengthened Legendre alone is not sufficient (e.g. $\int_0^a(y'^2-y^2)dx$ with $a>\pi$: $F_{y'y'}=2>0$ but $y\equiv0$ is not a minimum). Strengthened Legendre + Jacobi (no conjugate point in $(a,b]$) is sufficient for a weak minimum.

**Q7 — (A).** EL: $y''=0$ ⇒ $y=cx$. Natural BC at $x=1$: $F_{y'}=2y'(1)=2c=0$ ⇒ $y\equiv0$. R is exactly the condition used.

**Q8 — (C).** $J[2y]=4J[y]\ne 2J[y]$. The others are of the form $\int(py+qy')dx$ or point evaluations – all linear.

**Q9 — (B).** Isoperimetric: $H=y'^2-\lambda y$ ⇒ $2y''=-\lambda$ ⇒ $y$ is a parabola; with the BCs $y=kx(1-x)$. $\int_0^1 y=k/6=1\Rightarrow k=6$. $\int_0^1 36(1-2x)^2dx=36\cdot\frac13=12$. (C) forgets the factor $\int(1-2x)^2=1/3$.

**Q10 — (D).** Signs alternate: $F_y-(F_{y'})'+(F_{y''})''=0$. (A) is the common sign slip.

**Q11 — (B).** $y^2+2xyy'=\frac{d}{dx}(xy^2)$. Here $F_y=2y+2xy'$ and $\frac{d}{dx}F_{y'}=\frac{d}{dx}(2xy)=2y+2xy'$, so EL is an identity. $J=[xy^2]_0^1=1\cdot4=4$ (path-independent). (D) forgets to square $y(1)$.

**Q12 — (C).** $F_y=2z$, $F_{y'}=2y'$ ⇒ $y''=z$; similarly $z''=y$. Hence $y^{(4)}=z''=y$.

**Q13 — (B).** Jacobi equation: $\frac{d}{dx}(Ph')-Qh=0$ with $P=\frac12F_{y'y'}=1$, $Q=\frac12(F_{yy}-\frac{d}{dx}F_{yy'})=-1$ ⇒ $h''+h=0$, $h(0)=0$ ⇒ $h=\sin x$, next zero at $\pi$. So $y\equiv0$ is a minimum iff $a<\pi$.
