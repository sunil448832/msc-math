# Cheatsheet · Unit 6 · Topic 02 — Singular Solutions of First Order ODEs
> Questions: [../Questions/02-Singular-Solutions-First-Order.md](../Questions/02-Singular-Solutions-First-Order.md)

Notation: $p=y'$. We consider equations of degree $\gt 1$ in $p$: $F(x,y,p)=0$.

## 1. Definitions
- **General solution:** a one-parameter family $\phi(x,y,c)=0$.
- **Particular solution:** a member of the family for a specific $c$.
- **Singular solution:** a solution that is **not** obtainable from the general solution for any $c$. Typically it is the **envelope** of the family.
- A singular solution is possible only where **uniqueness fails**. If $f$ and $f_y$ are continuous, then $y'=f(x,y)$ has **no** singular solution.

## 2. Discriminants
| | How to get it | Contains |
|---|---|---|
| $p$-discriminant | eliminate $p$ from $F=0,\ \partial F/\partial p=0$ | $E\cdot T^{2}\cdot C$ |
| $c$-discriminant | eliminate $c$ from $\phi=0,\ \partial\phi/\partial c=0$ | $E\cdot N^{2}\cdot C^{3}$ |

Here $E$ is the envelope (**a singular solution**), $T$ the tac-locus, $N$ the nodal locus and $C$ the cusp-locus.
- **Singular solution test:** take a factor that appears in **both** discriminants to the **first power**, then **check that it satisfies the ODE**.
- The tac-, nodal and cusp-loci are generally **not** solutions. The cusp-locus can occasionally satisfy the ODE, so always check.
- For a quadratic $Ap^2+Bp+C=0$, the $p$-discriminant is $B^2-4AC=0$. The same applies to $c$ in the family.

## 3. Clairaut's equation $y=px+f(p)$
- Differentiating gives $(x+f'(p))\thinspace p'=0$.
- **General solution:** $y=cx+f(c)$, a family of straight lines.
- **Singular solution:** eliminate $p$ from $y=px+f(p)$ and $x+f'(p)=0$. This is the envelope of the lines.

| Equation | Singular solution |
|---|---|
| $y=px+p^2$ | $x^2+4y=0$ |
| $y=px+a/p$ | $y^2=4ax$ |
| $y=px+a\sqrt{1+p^2}$ | $x^2+y^2=a^2$ |
| $y=px+\sqrt{a^2p^2+b^2}$ | $x^2/a^2+y^2/b^2=1$ |
| $y=px+\sqrt{a^2p^2-b^2}$ | $x^2/a^2-y^2/b^2=1$ |
| $y=px-p^3$ | $27y^2=4x^3$ |
| $y=px-e^p$ | $y=x\ln x-x$ |

**Reducible to Clairaut form:**
| Equation type | Substitution |
|---|---|
| contains $(px-y)$ with $x^2,y^2$, e.g. $(px-y)(py+x)=a^2p$ | $X=x^2,\ Y=y^2$. This example gives $Y=PX-\frac{a^2P}{P+1}$ |
| $e^{3x}(p-1)+p^3e^{2y}=0$ | $X=e^x,\ Y=e^y$ |
| $y=2px+y^2p^3$ | $Y=y^2$, which gives $Y=PX+P^3/8$ |

## 4. Other first-order, higher-degree equations
- **Solvable for $p$:** factor into $(p-f_1)(p-f_2)\cdots=0$ and solve each factor.
- **Solvable for $y$:** $y=f(x,p)$. Differentiate w.r.t. $x$ to get an equation in $x,p$.
- **Solvable for $x$:** $x=f(y,p)$. Differentiate w.r.t. $y$, using $\frac{dx}{dy}=\frac1p$.
- **Lagrange (d'Alembert) equation** $y=x\thinspace g(p)+f(p)$: this is linear in $x$ as a function of $p$.
- **Standard examples:**
  - $p^2=4y$: general solution $y=(x+c)^2$, singular solution $y=0$.
  - $y'=3y^{2/3}$: general solution $y=(x-c)^3$, singular solution $y=0$ (the envelope at the inflection points).
  - $y^2(1+p^2)=1$ (unit circles centred on the $x$-axis): singular solutions $y=\pm1$.

## 5. Exact equations and integrating factors (brief)
$M\thinspace dx+N\thinspace dy=0$ is **exact** iff $M_y=N_x$ (on a simply connected domain).

| Condition | Integrating factor |
|---|---|
| $\frac{M_y-N_x}{N}=f(x)$ | $e^{\int f(x)dx}$ |
| $\frac{N_x-M_y}{M}=g(y)$ | $e^{\int g(y)dy}$ |
| homogeneous, $Mx+Ny\ne0$ | $\frac{1}{Mx+Ny}$ |
| $M=yf(xy)$, $N=xg(xy)$, $Mx-Ny\neq0$ | $\frac{1}{Mx-Ny}$ |
| $x^ay^b(my\thinspace dx+nx\thinspace dy)+x^cy^d(m'y\thinspace dx+n'x\thinspace dy)=0$ | $x^hy^k$ |
| linear $y'+Py=Q$ | $e^{\int P}$ |

Useful exact differentials: $d(xy)=x\thinspace dy+y\thinspace dx$; $d\big(\tfrac{x}{y}\big)=\tfrac{y\thinspace dx-x\thinspace dy}{y^2}$; $d\big(\tan^{-1}\tfrac{y}{x}\big)=\tfrac{x\thinspace dy-y\thinspace dx}{x^2+y^2}$; $d\ln(x^2+y^2)=\tfrac{2(x\thinspace dx+y\thinspace dy)}{x^2+y^2}$.

## Exam traps
- A factor of the $p$-discriminant is **not automatically** a singular solution. Check that it satisfies the ODE and that it appears in the $c$-discriminant too.
- The tac-locus appears **squared** in the $p$-discriminant and **not at all** in the $c$-discriminant. The nodal locus appears **squared** in the $c$-discriminant only. The cusp-locus appears **once** in the $p$-discriminant and **cubed** in the $c$-discriminant.
- In Clairaut's equation, the condition for the singular solution is $x+f'(p)=0$. Watch the sign when solving, e.g. $y=px+p^2$ gives $y=-x^2/4$.
- The line of centres of a family of circles (e.g. $y=0$) is **not** the envelope.
- A $y=0$ that is not in the general family for any finite $c$ is the usual candidate singular solution.
