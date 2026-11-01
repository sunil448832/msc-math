# Cheatsheet · Unit 6 · Topic 05 — First Order PDEs: Lagrange and Charpit
> Questions: [../Questions/05-First-Order-PDE-Lagrange-Charpit.md](../Questions/05-First-Order-PDE-Lagrange-Charpit.md)

Notation: $z=z(x,y)$, $p=z_x$, $q=z_y$.

## 1. Classification of first-order PDEs
| Type | Form | Example |
|---|---|---|
| Linear | $a(x,y)p+b(x,y)q+c(x,y)z=d(x,y)$ | $xp+yq=z$ |
| Semilinear | $a(x,y)p+b(x,y)q=c(x,y,z)$ | $p+q=z^2$ |
| Quasilinear | $P(x,y,z)p+Q(x,y,z)q=R(x,y,z)$ | $zp+q=0$ (Burgers type) |
| Nonlinear | anything else | $p^2+q^2=1$, $pq=z$ |

The classes are nested: linear ⊂ semilinear ⊂ quasilinear ⊂ all first-order PDEs.

## 2. Forming PDEs by elimination
- **Arbitrary constants:** $z=F(x,y,a,b)$ with 2 constants gives a first-order PDE. If there are more constants than independent variables, the result is of higher order.
- **Arbitrary function:** $\phi(u,v)=0$ gives the linear (Lagrange) PDE $Pp+Qq=R$, where
$$P=\frac{\partial(u,v)}{\partial(y,z)},\quad Q=\frac{\partial(u,v)}{\partial(z,x)},\quad R=\frac{\partial(u,v)}{\partial(x,y)} .$$
- **Standard results:**

| Relation | PDE obtained |
|---|---|
| $z=f(x^2+y^2)$ | $yp-xq=0$ |
| $z=f(y/x)$ | $xp+yq=0$ |
| $z=x^nf(y/x)$ | $xp+yq=nz$ |
| $z=(x+a)(y+b)$ | $pq=z$ |
| $z=ax+by+ab$ | $z=px+qy+pq$ |
| $z=f(x-ct)$ | $z_t+cz_x=0$ |
| $(x-a)^2+(y-b)^2+z^2=1$ | $z^2(1+p^2+q^2)=1$ |

## 3. Lagrange's method for $Pp+Qq=R$ (quasilinear)
1. Write the auxiliary equations $\dfrac{dx}{P}=\dfrac{dy}{Q}=\dfrac{dz}{R}$.
2. Find two independent integrals $u=c_1$ and $v=c_2$.
3. The **general solution** is $\phi(u,v)=0$ (or $`v=f(u)`$).

**Multipliers trick:** if $lP+mQ+nR=0$, then $l\thinspace dx+m\thinspace dy+n\thinspace dz=0$.
| PDE | Integrals |
|---|---|
| $(y-z)p+(z-x)q=x-y$ | $x+y+z$, $x^2+y^2+z^2$ |
| $x(y-z)p+y(z-x)q=z(x-y)$ | $x+y+z$, $xyz$ |
| $(mz-ny)p+(nx-lz)q=ly-mx$ | $lx+my+nz$, $x^2+y^2+z^2$ |
| $x^2p+y^2q=z^2$ | $\frac1x-\frac1y$, $\frac1y-\frac1z$ |
| $p+q=1$ | $x-y$, $z-x$, so $z=x+f(x-y)$ |
| $xp+yq=z$ | $y/x$, $z/x$ |

**Cauchy problem / integral surface through a curve.** Parametrise the curve as $x(s),y(s),z(s)$, substitute into $u=c_1$, $v=c_2$, and eliminate $s$ to get a relation $F(c_1,c_2)=0$. Then replace $c_1\to u$ and $c_2\to v$.

## 4. Nonlinear PDEs: types of solution
- **Complete integral:** $z=F(x,y,a,b)$, with two arbitrary constants (rank condition: the matrix $`\begin{pmatrix}F_a&F_{xa}&F_{ya}\cr F_b&F_{xb}&F_{yb}\end{pmatrix}`$ has rank 2).
- **General integral:** put $b=\phi(a)$ and take the envelope by eliminating $a$ from $z=F(x,y,a,\phi(a))$ and $F_a+F_b\phi'(a)=0$.
- **Singular integral:** eliminate $a,b$ from $z=F$, $F_a=0$, $F_b=0$. Equivalently, eliminate $p,q$ from $f=0$, $f_p=0$, $f_q=0$. It **may not exist**.

## 5. Charpit's method for $f(x,y,z,p,q)=0$
$$\frac{dp}{f_x+pf_z}=\frac{dq}{f_y+qf_z}=\frac{dz}{-pf_p-qf_q}=\frac{dx}{-f_p}=\frac{dy}{-f_q}$$
Find one integral involving $p$ or $q$, solve together with $f=0$ for $p$ and $q$, then integrate $dz=p\thinspace dx+q\thinspace dy$.
(**Jacobi's method** is the analogue for three or more independent variables.)

## 6. Standard forms (shortcuts to Charpit)
| Form | Method | Example |
|---|---|---|
| I. $f(p,q)=0$ | $z=ax+by+c$ with $f(a,b)=0$ | $p^2+q^2=1$ gives $z=ax+\sqrt{1-a^2}\thinspace y+c$; $pq=1$ gives $z=ax+y/a+c$ |
| II. $f(z,p,q)=0$ | $u=x+ay$, $q=ap$, $p=dz/du$ | $pq=z$ gives $4az=(x+ay+b)^2$; $p(1+q)=qz$ gives $\ln(az-1)=x+ay+b$ |
| III. $f_1(x,p)=f_2(y,q)$ (separable) | set both sides equal to $a$ | $p^2+q^2=x+y$ gives $z=\frac23(x+a)^{3/2}+\frac23(y-a)^{3/2}+b$; $p-x^2=q+y^2$ gives $z=ax+\frac{x^3}{3}+ay-\frac{y^3}{3}+b$ |
| IV. Clairaut $z=px+qy+f(p,q)$ | $z=ax+by+f(a,b)$ | $z=px+qy+pq$ gives $z=ax+by+ab$, singular integral $z=-xy$; $z=px+qy+p^2+q^2$ gives singular integral $4z=-(x^2+y^2)$ |

**Reductions:** for $f(x^mp,y^nq)=0$ use $X=x^{1-m}$ (or $X=\ln x$ when $m=1$). For $f(z^kp,z^kq)=0$ use $Z=z^{k+1}$ (or $\ln z$ when $k=-1$).

## 7. Characteristics (geometric view)
For a quasilinear equation, the characteristic curves are the solutions of $\frac{dx}{P}=\frac{dy}{Q}=\frac{dz}{R}$, and integral surfaces are unions of them. The Cauchy problem has a unique local solution if the data curve is **non-characteristic**, i.e. its projection satisfies $P\thinspace y'(s)-Q\thinspace x'(s)\neq0$.

## Exam traps
- The general solution of a Lagrange equation involves an **arbitrary function**, not arbitrary constants.
- Clairaut's singular integral needs careful signs: $z=px+qy+p^2+q^2$ gives $z=-\frac{x^2+y^2}{4}$.
- $(x+a)(y+b)$ gives $z=pq$, not $p+q$.
- Standard form II gives a factor of $4a$: $pq=z$ leads to $4az=(x+ay+b)^2$.
- Not every complete integral leads to a singular integral (e.g. $p^2+q^2=1$ has none).
- "Quasilinear" means linear in the highest derivatives $p,q$, but the coefficients may depend on $z$.
