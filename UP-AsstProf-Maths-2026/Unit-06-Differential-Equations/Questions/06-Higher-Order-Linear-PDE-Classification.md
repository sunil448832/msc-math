# Unit 6 · Topic 06 — Higher Order Linear PDEs and Classification
> Syllabus coverage: General solution of higher order partial differential equations with constant coefficients, classification of second order partial differential equations
> Cheatsheet: [../Cheatsheets/06-Higher-Order-Linear-PDE-Classification.md](../Cheatsheets/06-Higher-Order-Linear-PDE-Classification.md)

Notation: $D=\partial/\partial x$, $D'=\partial/\partial y$. Second-order PDE: $Au_{xx}+Bu_{xy}+Cu_{yy}+(\text{lower order})=0$.

**Q1.** `[Concept]` ★ The equation $Au_{xx}+Bu_{xy}+Cu_{yy}+Du_x+Eu_y+Fu=G$ (with real coefficients) is hyperbolic at a point if

(A) $B^2-4AC<0$

(B) $B^2-4AC=0$

(C) $B^2-4AC>0$

(D) $B^2-AC>0$

**Q2.** `[Numerical]` ★ The PDE $x^2u_{xx}-y^2u_{yy}=0$ is

(A) elliptic in the region $xy\neq0$

(B) hyperbolic in the region $xy\neq0$

(C) parabolic everywhere

(D) hyperbolic only in the first quadrant

**Q3.** `[Numerical]` ★★ The Tricomi equation $yu_{xx}+u_{yy}=0$ is

(A) elliptic for $y<0$ and hyperbolic for $y>0$

(B) parabolic for $y\ne0$

(C) hyperbolic everywhere

(D) hyperbolic for $y<0$ and elliptic for $y>0$

**Q4.** `[Numerical]` ★★ The general solution of $(D^2-3DD'+2D'^2)z=0$ is

(A) $z=f_1(y+x)+f_2(y+2x)$

(B) $z=f_1(y-x)+f_2(y-2x)$

(C) $z=f_1(x+y)+f_2(2x-y)$

(D) $z=f_1(y+x)+xf_2(y+x)$

**Q5.** `[Application]` ★★ The general solution of $u_{xx}+4u_{xy}+4u_{yy}=0$ is

(A) $f(y+2x)+g(y-2x)$

(B) $f(y-2x)+x\,g(y-2x)$

(C) $f(y+2x)+x\,g(y+2x)$

(D) $f(x-2y)+y\,g(x-2y)$

**Q6.** `[Numerical]` ★★★ A particular integral of $(D^2-D'^2)z=e^{x+y}$ is

(A) $\tfrac12e^{x+y}$

(B) $xe^{x+y}$

(C) $\tfrac12xe^{x+y}$

(D) $-\tfrac12xe^{x+y}$

**Q7.** `[Numerical]` ★★ A particular integral of $(D^2-D'^2)z=\cos(x+2y)$ is

(A) $-\tfrac13\cos(x+2y)$

(B) $\tfrac13\cos(x+2y)$

(C) $-\tfrac15\cos(x+2y)$

(D) $\tfrac15\cos(x+2y)$

**Q8.** `[Multi-Statement]` ★★ Consider:

I. Laplace's equation $u_{xx}+u_{yy}=0$ is elliptic everywhere.

II. The heat equation $u_t=ku_{xx}$ ($k>0$) is parabolic.

III. The wave equation $u_{tt}=c^2u_{xx}$ is hyperbolic.

IV. The equation $u_{xx}+xu_{yy}=0$ is of the same type at every point of $\mathbb{R}^2$.

Which are correct?

(A) I, II and III only

(B) I and III only

(C) II and IV only

(D) I, II, III and IV

**Q9.** `[Assertion-Reason]` ★★★
**Assertion (A):** The type (elliptic/parabolic/hyperbolic) of a second-order linear PDE in two variables at a point is unchanged by a smooth change of variables $\xi=\xi(x,y)$, $\eta=\eta(x,y)$ with non-zero Jacobian.
**Reason (R):** Under such a change, the discriminant transforms as $B'^2-4A'C'=J^2\,(B^2-4AC)$, where $J=\dfrac{\partial(\xi,\eta)}{\partial(x,y)}$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[Match]` ★★ Match each PDE in List-I with its real characteristic curves in List-II.

| List-I | List-II |
|---|---|
| (a) $u_{xx}-u_{yy}=0$ | 1. $x=$ const and $y=$ const |
| (b) $u_{xx}+2u_{xy}+u_{yy}=0$ | 2. no real characteristics |
| (c) $u_{xx}+u_{yy}=0$ | 3. $x+y=$ const and $x-y=$ const |
| (d) $u_{xy}=0$ | 4. the single family $y-x=$ const |

(A) a-3, b-4, c-1, d-2

(B) a-4, b-3, c-2, d-1

(C) a-3, b-4, c-2, d-1

(D) a-3, b-2, c-4, d-1

**Q11.** `[NOT-true / Counterexample]` ★★ Which of the following statements is **NOT** true?

(A) $u_{xx}+u_{yy}+u_x=0$ is elliptic.

(B) The type of a second-order linear PDE depends only on its principal (second-order) part.

(C) A second-order linear PDE with constant coefficients has the same type at every point.

(D) $u_{xx}-x^2u_{yy}=0$ is hyperbolic at every point of $\mathbb{R}^2$.

**Q12.** `[Concept]` ★★ For the irreducible equation $(D-D'^2)z=0$, the trial solution $z=e^{hx+ky}$ works provided

(A) $h=-k^2$

(B) $h=k$

(C) $k=h^2$

(D) $h=k^2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | B | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | B | Application |
| 6 | C | Numerical |
| 7 | B | Numerical |
| 8 | A | Multi-Statement |
| 9 | A | Assertion-Reason |
| 10 | C | Match |
| 11 | D | NOT-true / Counterexample |
| 12 | D | Concept |

## Solutions
**Q1 — (C).** In the convention $Au_{xx}+Bu_{xy}+Cu_{yy}$, the equation is hyperbolic if $B^2-4AC>0$. Option (D) is the test for the convention $Au_{xx}+2Bu_{xy}+Cu_{yy}$, which is a different form from the one given.

**Q2 — (B).** $B^2-4AC=0-4(x^2)(-y^2)=4x^2y^2>0$ when $xy\ne0$. On the axes it is parabolic.

**Q3 — (D).** $B^2-4AC=-4y$, which is positive (hyperbolic) for $y<0$, negative (elliptic) for $y>0$, and zero (parabolic) on $y=0$.

**Q4 — (A).** The auxiliary equation is $m^2-3m+2=0$, so $m=1,2$. Each factor $(D-mD')$ contributes $f(y+mx)$. Option (B) uses the wrong sign convention.

**Q5 — (B).** $D^2+4DD'+4D'^2=(D+2D')^2$, so $m=-2$ is a repeated root. The solution is $f(y-2x)+x\,g(y-2x)$. Equivalently, $\xi=y-2x$, $\eta=x$ gives the canonical form $u_{\eta\eta}=0$.

**Q6 — (C).** $F(D,D')=(D-D')(D+D')$ vanishes at $(1,1)$ through the factor $D-D'$, so this is the failure case. Then $\frac{1}{D-D'}\cdot\frac{1}{D+D'}e^{x+y}=\frac{1}{D-D'}\frac{e^{x+y}}{2}=\frac{x}{2}e^{x+y}$. Check: $z_{xx}-z_{yy}=\frac{(2+x)-x}{2}e^{x+y}=e^{x+y}$. Option (B) forgets the factor $\frac{1}{2}$ from $D+D'$.

**Q7 — (B).** Replace $D^2\to-1$ and $D'^2\to-4$: $F=-1-(-4)=3$, so the particular integral is $\frac13\cos(x+2y)$. This was checked by direct substitution. Option (A) comes from dropping both minus signs ($D^2\to1$, $D'^2\to4$, which gives $-3$). Option (C) comes from writing $D'^2\to+4$, which gives $-5$.

**Q8 — (A).** IV is false: $B^2-4AC=-4x$, so the equation is hyperbolic for $x<0$, parabolic on $x=0$ and elliptic for $x>0$.

**Q9 — (A).** Since $J^2>0$, the sign of the discriminant is preserved, which is exactly why the type is invariant.

**Q10 — (C).** The characteristic equation is $A\,dy^2-B\,dx\,dy+C\,dx^2=0$. (a) $dy^2=dx^2$ gives $x\pm y=c$. (b) $(dy-dx)^2=0$ gives $y-x=c$ (one family, parabolic). (c) $dy^2+dx^2=0$ has no real solutions. (d) $-dx\,dy=0$ gives $x=c$ and $y=c$.

**Q11 — (D).** At $x=0$, $B^2-4AC=4x^2=0$, so the equation is parabolic on the $y$-axis and hyperbolic only for $x\ne0$. (A) is true because lower-order terms do not affect the type.

**Q12 — (D).** $(D-D'^2)e^{hx+ky}=(h-k^2)e^{hx+ky}$, so we need $h=k^2$. This gives $z=\sum A\,e^{k^2x+ky}$. For example, with $k=i\alpha$ we get $e^{-\alpha^2x}\cos\alpha y$, a heat-equation-type solution.
