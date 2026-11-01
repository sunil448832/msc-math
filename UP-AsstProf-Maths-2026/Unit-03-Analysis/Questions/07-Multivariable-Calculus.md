# Unit 3 · Topic 07 — Multivariable Calculus
> Syllabus coverage: Multivariable calculus — functions of several variables, directional derivative, partial derivative and total derivative, maxima and minima (also: limits, continuity, Jacobian, implicit function theorem, Lagrange multipliers)
> Cheatsheet: [../Cheatsheets/07-Multivariable-Calculus.md](../Cheatsheets/07-Multivariable-Calculus.md)

**Q1.** `[Concept]` ★ Let $f(x,y)=\dfrac{xy}{x^2+y^2}$ for $(x,y)\ne(0,0)$ and $f(0,0)=0$. At the origin,

(A) $f$ is continuous and differentiable

(B) both partial derivatives exist, but $f$ is not continuous

(C) the partial derivatives do not exist

(D) $f$ is continuous, but the partial derivatives do not exist

**Q2.** `[Numerical]` ★ The directional derivative of $f(x,y,z)=x^2y+2yz$ at $(1,2,1)$ in the direction of the vector $2\mathbf i+\mathbf j+2\mathbf k$ is

(A) $19$

(B) $\dfrac{19}{3}$

(C) $\sqrt{41}$

(D) $\dfrac{11}{3}$

**Q3.** `[Numerical]` ★★ For $u=x^2-y^2$, $v=2xy$, the Jacobian $\dfrac{\partial(u,v)}{\partial(x,y)}$ at $(1,1)$ is

(A) $0$

(B) $4$

(C) $8$

(D) $-8$

**Q4.** `[Multi-Statement]` ★★★ Let $f(x,y)=\dfrac{x^2y}{x^4+y^2}$ for $(x,y)\ne(0,0)$ and $f(0,0)=0$. Consider the following statements.

I. The directional derivative $D_{\mathbf u}f(0,0)$ exists for every unit vector $\mathbf u$.

II. $f$ is continuous at $(0,0)$.

III. The map $\mathbf u\mapsto D_{\mathbf u}f(0,0)$ is linear.

Which is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** $f(x,y)=\sqrt{|xy|}$ is not differentiable at $(0,0)$.
**Reason (R):** $f_x(0,0)=f_y(0,0)=0$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Each function in List-I has a critical point at the origin, and $r=f_{xx}, s=f_{xy}, t=f_{yy}$ are evaluated there. Match the function with the nature of the origin.

| List-I | List-II |
|---|---|
| (a) $x^2+y^2$ | 1. $rt-s^2=0$ (test inconclusive), yet a local minimum |
| (b) $x^2-y^2$ | 2. saddle point |
| (c) $-x^2-y^2$ | 3. local maximum |
| (d) $x^4+y^4$ | 4. local minimum with $rt-s^2>0$ |

(A) a-4, b-2, c-3, d-1

(B) a-1, b-2, c-3, d-4

(C) a-4, b-3, c-2, d-1

(D) a-4, b-1, c-3, d-2

**Q7.** `[NOT-true / Counterexample]` ★ For $f:\mathbb R^2\to\mathbb R$ and a point $p$, which of the following is **NOT** true in general?

(A) If $f$ is differentiable at $p$, then $f$ is continuous at $p$.

(B) If $f$ is differentiable at $p$, then both partial derivatives exist at $p$.

(C) If $f_x,f_y$ exist in a neighbourhood of $p$ and are continuous at $p$, then $f$ is differentiable at $p$.

(D) If both partial derivatives exist at $p$, then $f$ is continuous at $p$.

**Q8.** `[Numerical]` ★★ The minimum value of $x^2+y^2+z^2$ subject to $x+2y+2z=9$ is

(A) $3$

(B) $9$

(C) $\dfrac{81}{5}$

(D) $27$

**Q9.** `[Numerical]` ★★ For $f(x,y)=x^3+y^3-3xy$, the local minimum value of $f$ is

(A) $0$

(B) $1$

(C) $f$ has no local minimum

(D) $-1$

**Q10.** `[Application]` ★★ The equation $xyz+x^2+z^3=3$ defines $z$ as a differentiable function of $(x,y)$ near $(1,1,1)$. Then $\dfrac{\partial z}{\partial x}(1,1)$ equals

(A) $-\dfrac34$

(B) $-\dfrac43$

(C) $\dfrac34$

(D) $-1$

**Q11.** `[Concept]` ★★★ Let $f(x,y)=\dfrac{xy(x^2-y^2)}{x^2+y^2}$ for $(x,y)\ne(0,0)$ and $f(0,0)=0$. At the origin, the mixed partial derivatives $\frac{\partial^2 f}{\partial x\partial y}$ and $\frac{\partial^2 f}{\partial y\partial x}$

(A) both exist and are equal to $0$

(B) both exist and are equal to $1$

(C) both exist, and one is $1$ while the other is $-1$

(D) do not exist

**Q12.** `[Application]` ★★★ Let $F:\mathbb R^2\to\mathbb R^2$, $F(x,y)=(e^x\cos y,\ e^x\sin y)$. Which of the following is true?

(A) $F$ is injective on $\mathbb R^2$.

(B) $\det JF$ vanishes on the line $x=0$.

(C) $F$ is onto $\mathbb R^2$.

(D) $\det JF$ never vanishes, so $F$ is locally invertible at every point, but $F$ is not injective.

**Q13.** `[Concept]` ★ Let $(a,b)$ be a critical point of a $C^2$ function $f(x,y)$, with $r=f_{xx}, s=f_{xy}, t=f_{yy}$ evaluated at $(a,b)$. Then $(a,b)$ is a saddle point if

(A) $rt-s^2>0$ and $r>0$

(B) $rt-s^2>0$ and $r<0$

(C) $rt-s^2<0$

(D) $rt-s^2=0$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | B | Numerical |
| 3 | C | Numerical |
| 4 | A | Multi-Statement |
| 5 | B | Assertion-Reason |
| 6 | A | Match |
| 7 | D | NOT-true / Counterexample |
| 8 | B | Numerical |
| 9 | D | Numerical |
| 10 | A | Application |
| 11 | C | Concept |
| 12 | D | Application |
| 13 | C | Concept |

## Solutions
**Q1 — (B).** $f(x,0)=f(0,y)=0$, so $f_x(0,0)=f_y(0,0)=0$. Along $y=mx$, $f=\frac{m}{1+m^2}$ depends on $m$, so the limit at the origin does not exist and $f$ is not continuous (hence not differentiable).

**Q2 — (B).** $\nabla f=(2xy,\ x^2+2z,\ 2y)=(4,3,4)$ at $(1,2,1)$. The unit vector is $\frac13(2,1,2)$, so $D_{\mathbf u}f=\frac{8+3+8}{3}=\frac{19}{3}$. Option (A) forgets to normalise the direction vector.

**Q3 — (C).** $J=\begin{vmatrix}2x&-2y\\2y&2x\end{vmatrix}=4(x^2+y^2)=8$ at $(1,1)$. This is $|f'(z)|^2$ for $f(z)=z^2$.

**Q4 — (A).** For $\mathbf u=(a,b)$ with $b\ne0$: $\frac{f(ta,tb)}{t}=\frac{a^2b}{t^2a^4+b^2}\to\frac{a^2}{b}$. For $b=0$, $f=0$ and the derivative is $0$. So I holds. Along $y=x^2$, $f=\frac12$, so $f$ is not continuous and II fails. $a^2/b$ is not linear in $(a,b)$, so III fails. (If $f$ were differentiable, the map in III would be $\nabla f\cdot\mathbf u$, which is linear.)

**Q5 — (B).** $f(x,0)=0$ and $f(0,y)=0$, so both partials are $0$ (R is true). If $f$ were differentiable, $\frac{f(h,k)}{\sqrt{h^2+k^2}}\to0$. Along $h=k$ this quotient is $\frac{|h|}{\sqrt2|h|}=\frac1{\sqrt2}$, so A is true. R does not explain A: existence of the partials is consistent with both differentiability and non-differentiability.

**Q6 — (A).** $x^2+y^2$: $r=t=2$, $s=0$, $rt-s^2=4>0$, $r>0$, so a minimum (4). $x^2-y^2$: $rt-s^2=-4<0$, a saddle (2). $-x^2-y^2$: a maximum (3). $x^4+y^4$: all second derivatives vanish, so the test fails, but $f\ge0=f(0,0)$ shows it is a minimum (1).

**Q7 — (D).** $\frac{xy}{x^2+y^2}$ (Q1) has both partials at $0$ but is discontinuous there. (A), (B) and (C) are standard. (C) is the usual sufficient condition for differentiability, and it even suffices that one partial is continuous.

**Q8 — (B).** The minimum is the squared distance from the origin to the plane: $\left(\frac{9}{\sqrt{1+4+4}}\right)^2=9$, attained at $(1,2,2)$. Lagrange: $(2x,2y,2z)=\lambda(1,2,2)$. Option (A) is the distance, not its square.

**Q9 — (D).** The critical points are $(0,0)$ and $(1,1)$. At $(0,0)$: $rt-s^2=0\cdot0-9<0$, a saddle. At $(1,1)$: $r=6,t=6,s=-3$, $rt-s^2=27>0$, $r>0$, a local minimum with value $1+1-3=-1$. (Globally $f$ is unbounded below, but the question asks for the local minimum.)

**Q10 — (A).** With $F=xyz+x^2+z^3-3$: $F_x=yz+2x=3$ and $F_z=xy+3z^2=4$ at $(1,1,1)$. So $z_x=-F_x/F_z=-\frac34$. Option (B) inverts the ratio.

**Q11 — (C).** $f_x(0,y)=-y$, so $\partial_y(f_x)(0,0)=-1$. $f_y(x,0)=x$, so $\partial_x(f_y)(0,0)=1$. The mixed partials exist and are unequal, because they are not continuous at the origin (the hypothesis of Schwarz/Clairaut fails). Whichever notation convention is used, one value is $1$ and the other is $-1$.

**Q12 — (D).** $JF=\begin{pmatrix}e^x\cos y&-e^x\sin y\\e^x\sin y&e^x\cos y\end{pmatrix}$, $\det=e^{2x}>0$. By the inverse function theorem $F$ is a local diffeomorphism. But $F(x,y)=F(x,y+2\pi)$, so $F$ is not injective, and $F$ never takes the value $(0,0)$, so it is not onto. ($F$ is $z\mapsto e^z$.)

**Q13 — (C).** $rt-s^2<0$ means the Hessian is indefinite, which gives a saddle. (A) gives a minimum, (B) a maximum, and (D) is inconclusive.
