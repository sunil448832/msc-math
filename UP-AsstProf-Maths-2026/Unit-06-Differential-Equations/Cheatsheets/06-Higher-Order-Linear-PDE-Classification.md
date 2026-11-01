# Cheatsheet · Unit 6 · Topic 06 — Higher Order Linear PDEs and Classification
> Questions: [../Questions/06-Higher-Order-Linear-PDE-Classification.md](../Questions/06-Higher-Order-Linear-PDE-Classification.md)

Notation: $D=\partial_x$, $D'=\partial_y$, and $F(D,D')z=f(x,y)$. The general solution is $z=\text{CF}+\text{PI}$.

## 1. Homogeneous equation (all terms of the same order $n$): complementary function
Put $D=m$, $D'=1$ to get the auxiliary equation $a_0m^n+a_1m^{n-1}+\dots+a_n=0$.
| Roots | CF |
|---|---|
| distinct $m_1,\dots,m_n$ | $\sum f_i(y+m_ix)$ |
| $m$ repeated $r$ times | $f_1(y+mx)+xf_2(y+mx)+\dots+x^{r-1}f_r(y+mx)$ |
| factor $D'$ (i.e. $m=\infty$) | contributes $f(x)$ |

The factor $(bD-aD')$ gives $f(ax+by)$ (since $b\cdot a-a\cdot b=0$), and $(D-mD')$ gives $f(y+mx)$.
- $(D^2-3DD'+2D'^2)z=0$ gives $z=f_1(y+x)+f_2(y+2x)$.
- The wave equation $(D^2-c^2D'^2)z=0$ (with $x\to t$) gives $f(x+ct)+g(x-ct)$.
- $(D+2D')^2z=0$ gives $f(y-2x)+xg(y-2x)$.

## 2. Particular integral, homogeneous $F$ of degree $n$
| RHS | PI |
|---|---|
| $e^{ax+by}$ | $\dfrac{e^{ax+by}}{F(a,b)}$ if $F(a,b)\ne0$ |
| failure: $(bD-aD')^r$ divides $F$ | for $F=(D-mD')^r$ and RHS $\phi(y+mx)$: $\frac{x^r}{r!}\phi(y+mx)$ |
| $\sin(ax+by)$, $\cos(ax+by)$ | replace $D^2\to-a^2$, $DD'\to-ab$, $D'^2\to-b^2$ |
| $\phi(ax+by)$ general | $\frac{1}{F(a,b)}\iint\cdots\int\phi(u)\,du^n$ with $u=ax+by$ (if $F(a,b)\ne0$) |
| $x^my^n$ | expand $F^{-1}$ in powers of $D'/D$ or $D/D'$ |

Key formula: $\dfrac{1}{D-mD'}\,\phi(x,y)=\int\phi(x,c-mx)\,dx\Big|_{c=y+mx}$.

**Worked failure case:** $(D^2-D'^2)z=e^{x+y}$ gives $\frac{1}{(D-D')}\frac{e^{x+y}}{2}=\frac{x}{2}e^{x+y}$.

## 3. Non-homogeneous equations (terms of mixed order)
- **Reducible** (factors into linear factors $(D-mD'-c)$): each factor contributes $e^{cx}f(y+mx)$, and a repeated factor gives $e^{cx}[f_1+xf_2](y+mx)$. A factor $(\beta D-\alpha D'-\gamma)$ gives $e^{\gamma x/\beta}f(\beta y+\alpha x)$.
- **Irreducible** (e.g. $D-D'^2$): use $z=\sum A\,e^{hx+ky}$ with $F(h,k)=0$. For $D-D'^2$ this gives $h=k^2$.
- **PI:** $\frac{1}{F}e^{ax+by}=\frac{e^{ax+by}}{F(a,b)}$; $\frac{1}{F(D,D')}e^{ax+by}V=e^{ax+by}\frac{1}{F(D+a,D'+b)}V$.

## 4. Classification of second-order linear PDEs
$$Au_{xx}+Bu_{xy}+Cu_{yy}+Du_x+Eu_y+Fu=G .$$
| $\Delta=B^2-4AC$ | Type | Prototype | Canonical form |
|---|---|---|---|
| $>0$ | hyperbolic | $u_{tt}=c^2u_{xx}$ | $u_{\xi\eta}=\dots$ or $u_{\xi\xi}-u_{\eta\eta}=\dots$ |
| $=0$ | parabolic | $u_t=ku_{xx}$ | $u_{\eta\eta}=\dots$ |
| $<0$ | elliptic | $u_{xx}+u_{yy}=0$ | $u_{\alpha\alpha}+u_{\beta\beta}=\dots$ |

(If the equation is written as $Au_{xx}+2Bu_{xy}+Cu_{yy}$, use $B^2-AC$ instead.)
- The type depends **only on the principal part** and may vary from point to point.
- **Invariance:** under a change of variables, $\Delta'=J^2\Delta$, so the type is preserved.
- **$n$ variables:** look at the eigenvalues of the coefficient matrix. All of the same sign means elliptic; one of opposite sign and the rest the same means (normal) hyperbolic; a zero eigenvalue means parabolic; at least two of each sign and none zero means ultra-hyperbolic.

| Equation | Type |
|---|---|
| $yu_{xx}+u_{yy}=0$ (Tricomi) | hyperbolic for $y<0$, parabolic on $y=0$, elliptic for $y>0$ |
| $u_{xx}+xu_{yy}=0$ | hyperbolic for $x<0$, elliptic for $x>0$ |
| $x^2u_{xx}-y^2u_{yy}=0$ | hyperbolic for $xy\ne0$ |
| $u_{xx}-x^2u_{yy}=0$ | hyperbolic for $x\ne0$, parabolic on $x=0$ |
| $x^2u_{xx}+2xyu_{xy}+y^2u_{yy}=0$ | parabolic everywhere ($\Delta=0$) |
| $u_{xx}+2u_{xy}+5u_{yy}=0$ | elliptic ($\Delta=-16$) |
| $(1+x^2)u_{xx}+(1+y^2)u_{yy}=0$ | elliptic everywhere |

## 5. Characteristics and reduction to canonical form
The characteristic equation is
$$A\,dy^2-B\,dx\,dy+C\,dx^2=0\quad\Longleftrightarrow\quad A\Big(\frac{dy}{dx}\Big)^2-B\frac{dy}{dx}+C=0 .$$
- **Hyperbolic:** two real families $\phi_1=c$ and $\phi_2=c$. Put $\xi=\phi_1$, $\eta=\phi_2$ to get $u_{\xi\eta}=\dots$.
  - Example: $u_{xx}-u_{yy}=0$ has characteristics $x\pm y=c$.
  - Example: $u_{xx}-x^2u_{yy}=0$ has $\frac{dy}{dx}=\pm x$, so $\xi=y+\frac{x^2}{2}$ and $\eta=y-\frac{x^2}{2}$.
- **Parabolic:** one family $\phi=c$. Put $\xi=\phi$ and choose $\eta$ independent (e.g. $\eta=x$) to get $u_{\eta\eta}=\dots$.
  - Example: $u_{xx}+4u_{xy}+4u_{yy}=0$ has $\frac{dy}{dx}=2$, so $\xi=y-2x$, $\eta=x$, giving $u_{\eta\eta}=0$ and $u=f(y-2x)+xg(y-2x)$.
- **Elliptic:** complex characteristics $\phi=\alpha\pm i\beta$. Put $\xi=\alpha$, $\eta=\beta$ to get $u_{\xi\xi}+u_{\eta\eta}=\dots$.
- $u_{xy}=0$ has characteristics $x=c$ and $y=c$, with solution $u=f(x)+g(y)$.

## 6. Well-posed problems (Hadamard)
| Type | Natural problem |
|---|---|
| Elliptic | boundary value problem (Dirichlet/Neumann) on a closed boundary |
| Parabolic | initial data plus boundary data (forward in time) |
| Hyperbolic | Cauchy data ($u$ and $u_t$) on a non-characteristic curve |

Hadamard's example: the Cauchy problem for Laplace's equation is **ill-posed**. The data $u(x,0)=0$, $u_y(x,0)=\frac{\sin nx}{n}$ give $u=\frac{\sin nx\sinh ny}{n^2}$, which blows up as $n\to\infty$ even though the data tend to $0$.

## Exam traps
- Check which convention is being used for the middle coefficient ($B$ or $2B$) before computing the discriminant.
- Lower-order terms **never** change the type.
- The solution $f(y+mx)$ comes from the factor $(D-mD')$: watch the sign.
- In the failure case, multiply by $x$ **and** divide by the derivative of the vanishing factor. For example, $(D^2-D'^2)$ on $e^{x+y}$ gives $\frac{x}{2}e^{x+y}$, not $xe^{x+y}$.
- In the trigonometric PI rule, $D'^2\to-b^2$ (not $+b^2$), and the rule works only when $F$ contains $D^2$, $DD'$ and $D'^2$ only.
- A variable-coefficient PDE can change type across a curve (Tricomi, $u_{xx}+xu_{yy}$).
