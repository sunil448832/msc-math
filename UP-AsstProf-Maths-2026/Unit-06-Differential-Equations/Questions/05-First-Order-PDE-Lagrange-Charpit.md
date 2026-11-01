# Unit 6 · Topic 05 — First Order PDEs: Lagrange and Charpit Methods
> Syllabus coverage: Lagrange and Charpit methods for solving first order partial differential equations
> Cheatsheet: [../Cheatsheets/05-First-Order-PDE-Lagrange-Charpit.md](../Cheatsheets/05-First-Order-PDE-Lagrange-Charpit.md)

Notation: $z=z(x,y)$, $p=z_x$, $q=z_y$.

**Q1.** `[Concept]` ★ If $u(x,y,z)=c_1$ and $v(x,y,z)=c_2$ are two independent solutions of $\dfrac{dx}{P}=\dfrac{dy}{Q}=\dfrac{dz}{R}$, then the general solution of $Pp+Qq=R$ is

(A) $u+v=0$

(B) $z=au+bv$ for arbitrary constants $a,b$

(C) $\phi(u,v)=0$ for an arbitrary function $\phi$

(D) $uv=c$ for an arbitrary constant $c$

**Q2.** `[Numerical]` ★ The general solution of $xp+yq=z$ is

(A) $z=\phi(x^2+y^2)$

(B) $\phi(xy,\ xz)=0$

(C) $\phi(x+y,\ z)=0$

(D) $\phi\negthinspace \left(\dfrac{y}{x},\dfrac{z}{x}\right)=0$

**Q3.** `[Numerical]` ★★ The general solution of $(y-z)p+(z-x)q=x-y$ is

(A) $\phi(xyz,\ x+y+z)=0$

(B) $\phi(x-y,\ y-z)=0$

(C) $\phi(x+y+z,\ x^2+y^2+z^2)=0$

(D) $\phi(x^2+y^2,\ z)=0$

**Q4.** `[Match]` ★★ Match each PDE in List-I with its classification in List-II.

| List-I | List-II |
|---|---|
| (a) $xp+yq=z$ | 1. quasilinear (not semilinear) |
| (b) $p+q=z^2$ | 2. linear |
| (c) $zp+q=0$ | 3. fully nonlinear |
| (d) $p^2+q^2=1$ | 4. semilinear (not linear) |

(A) a-2, b-4, c-1, d-3

(B) a-2, b-1, c-4, d-3

(C) a-4, b-2, c-1, d-3

(D) a-2, b-4, c-3, d-1

**Q5.** `[Numerical]` ★ A complete integral of $z=px+qy+pq$ is

(A) $z=ax+by+ab$

(B) $z=ax+by+a+b$

(C) $z=(x+a)(y+b)$

(D) $z=ax+by-xy$

**Q6.** `[Numerical]` ★★ A complete integral of $pq=z$ is

(A) $z=(x+ay+b)^2$

(B) $4az=(x+ay+b)^2$

(C) $z=ae^{x+ay}+b$

(D) $az=(x+ay+b)^2$

**Q7.** `[Numerical]` ★★★ A complete integral of $p^2+q^2=x+y$ is

(A) $z=\tfrac32(x+a)^{2/3}+\tfrac32(y-a)^{2/3}+b$

(B) $z=\tfrac23(x+y)^{3/2}+b$

(C) $z=(x+a)^{1/2}+(y-a)^{1/2}+b$

(D) $z=\tfrac23(x+a)^{3/2}+\tfrac23(y-a)^{3/2}+b$

**Q8.** `[Multi-Statement]` ★★ Consider the following statements about a first-order PDE $f(x,y,z,p,q)=0$.

I. A complete integral contains two arbitrary constants.

II. The general integral is obtained by putting $b=\phi(a)$ in the complete integral and taking the envelope with respect to $a$.

III. Every first-order PDE possesses a singular integral.

IV. The singular integral, when it exists, is obtained by eliminating $a,b$ from $z=F(x,y,a,b)$, $F_a=0$, $F_b=0$.

Which are correct?

(A) I and II only

(B) I, II and IV only

(C) II, III and IV only

(D) I, II, III and IV

**Q9.** `[Assertion-Reason]` ★★
**Assertion (A):** $z=ax+by+a^2+b^2$ is a complete integral of $z=px+qy+p^2+q^2$.
**Reason (R):** The singular integral of $z=px+qy+p^2+q^2$ is $4z=x^2+y^2$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) Eliminating $\phi$ from $z=\phi(x^2+y^2)$ gives $yp-xq=0$.

(B) Eliminating $a,b$ from $z=(x+a)(y+b)$ gives $z=p+q$.

(C) Eliminating $a,b$ from $z=ax+by$ gives $z=px+qy$.

(D) Eliminating $\phi$ from $u=\phi(x-ct)$ (with $`u=u(x,t)`$) gives $u_t+cu_x=0$.

**Q11.** `[Application]` ★★★ The integral surface of $xp+yq=z$ passing through the curve $x=1$, $z=y^2$ is

(A) $z=y^2/x$

(B) $z=xy^2$

(C) $z=y^2$

(D) $z=y^2/x^2$

**Q12.** `[Concept]` ★★ In Charpit's method for $f(x,y,z,p,q)=0$, the auxiliary equations are $\dfrac{dp}{\alpha}=\dfrac{dq}{\beta}=\dfrac{dz}{\gamma}=\dfrac{dx}{-f_p}=\dfrac{dy}{-f_q}$, where

(A) $\alpha=f_x,\ \beta=f_y,\ \gamma=f_z$

(B) $\alpha=f_x-pf_z,\ \beta=f_y-qf_z,\ \gamma=pf_p+qf_q$

(C) $\alpha=f_p+xf_z,\ \beta=f_q+yf_z,\ \gamma=-xf_x-yf_y$

(D) $\alpha=f_x+pf_z,\ \beta=f_y+qf_z,\ \gamma=-pf_p-qf_q$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | D | Numerical |
| 3 | C | Numerical |
| 4 | A | Match |
| 5 | A | Numerical |
| 6 | B | Numerical |
| 7 | D | Numerical |
| 8 | B | Multi-Statement |
| 9 | C | Assertion-Reason |
| 10 | B | NOT-true / Counterexample |
| 11 | A | Application |
| 12 | D | Concept |

## Solutions
**Q1 — (C).** Lagrange's theorem: $\phi(u,v)=0$ (equivalently, $`v=\psi(u)`$) with $\phi$ an arbitrary function. Arbitrary constants (B) would give only a complete-type family, not the general solution.

**Q2 — (D).** From $\frac{dx}{x}=\frac{dy}{y}$ we get $y/x=c_1$, and from $\frac{dx}{x}=\frac{dz}{z}$ we get $z/x=c_2$. So $\phi(y/x,z/x)=0$, i.e. $z=x\thinspace f(y/x)$: $z$ is homogeneous of degree 1 (Euler).

**Q3 — (C).** With multipliers $1,1,1$, we get $P+Q+R=0$, so $x+y+z=c_1$. With multipliers $x,y,z$, we get $xP+yQ+zR=0$, so $x^2+y^2+z^2=c_2$.

**Q4 — (A).** (a) Linear in $z,p,q$ with coefficients in $x,y$. (b) Linear in $p,q$ with coefficients in $x,y$, but the term $z^2$ is nonlinear, so it is semilinear. (c) The coefficient of $p$ involves $z$, so it is quasilinear but not semilinear. (d) $p,q$ enter nonlinearly, so it is fully nonlinear.

**Q5 — (A).** This is Clairaut form $z=px+qy+f(p,q)$, so the complete integral is $z=ax+by+f(a,b)=ax+by+ab$. Option (C) satisfies $pq=z$, not this equation.

**Q6 — (B).** For the type $f(z,p,q)=0$, put $u=x+ay$, so $q=ap$ and $p=dz/du$. Then $a p^2=z$, so $p=\sqrt{z/a}$, and $2\sqrt{az}=u+b$, i.e. $4az=(x+ay+b)^2$. Check: $p=\frac{x+ay+b}{2a}$ and $q=\frac{x+ay+b}{2}$, so $pq=z$. Option (D) misses the factor $4$.

**Q7 — (D).** The equation is separable: $p^2-x=y-q^2=a$. So $p=\sqrt{x+a}$ and $q=\sqrt{y-a}$, and $z=\int p\thinspace dx+\int q\thinspace dy$ gives (D). Option (B) has only one constant, so it is not complete.

**Q8 — (B).** III is false: not every PDE has a singular integral. For example, the eliminants of $p^2+q^2=1$ give no surface. I, II and IV are the standard definitions.

**Q9 — (C).** A is true because this is Clairaut form. For R: $F_a=x+2a=0$ and $F_b=y+2b=0$ give $z=-\frac{x^2}{2}-\frac{y^2}{2}+\frac{x^2+y^2}{4}=-\frac{x^2+y^2}{4}$. So the singular integral is $4z+x^2+y^2=0$, and R (with the wrong sign) is false.

**Q10 — (B).** For $z=(x+a)(y+b)$, $p=y+b$ and $q=x+a$, so $z=pq$, not $p+q$. Checks: (A) $p=2x\phi'$ and $q=2y\phi'$, so $yp-xq=0$. (C) $p=a$, $q=b$. (D) $u_t=-c\phi'$ and $u_x=\phi'$.

**Q11 — (A).** The general solution is $z=x\thinspace F(y/x)$. On $x=1$ this gives $F(y)=y^2$, so $z=x(y/x)^2=y^2/x$. Check: $xp+yq=-y^2/x+2y^2/x=y^2/x=z$. Option (C) satisfies the data but not the PDE, since $xp+yq=2y^2\ne z$.

**Q12 — (D).** These are the standard Charpit equations: $\frac{dp}{f_x+pf_z}=\frac{dq}{f_y+qf_z}=\frac{dz}{-pf_p-qf_q}=\frac{dx}{-f_p}=\frac{dy}{-f_q}$. Option (B) has the signs flipped.
