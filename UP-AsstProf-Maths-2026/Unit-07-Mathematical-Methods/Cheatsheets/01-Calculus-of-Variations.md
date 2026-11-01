# Cheatsheet · Unit 7 · Topic 01 — Calculus of Variations
> Questions: [../Questions/01-Calculus-of-Variations.md](../Questions/01-Calculus-of-Variations.md)

## 1. Functionals
- A **functional** $J:\mathcal{D}\to\mathbb{R}$ assigns a number to each function, e.g. $J[y]=\int_a^b F(x,y,y')\,dx$.
- **Linear functional:** $J[\alpha y+\beta z]=\alpha J[y]+\beta J[z]$. Examples: $\int_a^b(p\,y+q\,y')dx$, $y(x_0)$, $y'(x_0)$. Non-examples: $\int y^2$, $\int\sqrt{1+y'^2}$, $\int(y+1)dx$ (affine, not linear).
- **Continuity** in $C^0$ norm $\|y\|_0=\max|y|$ (strong) or $C^1$ norm $\|y\|_1=\max|y|+\max|y'|$ (weak).
- **Strong extremum:** compare with curves close in $C^0$; **weak extremum:** close in $C^1$. Strong ⇒ weak (more competitors), not conversely.
- **First variation:** $\delta J[h]=\frac{d}{d\varepsilon}J[y+\varepsilon h]\big|_{\varepsilon=0}$ (a linear functional of $h$). Necessary condition: $\delta J=0$.
- **Fundamental lemma:** if $M$ continuous and $\int_a^b M h\,dx=0$ for all $h\in C^1$ with $h(a)=h(b)=0$, then $M\equiv0$.

## 2. Euler–Lagrange equation
For $J[y]=\int_a^b F(x,y,y')dx$, $y(a)=A$, $y(b)=B$, $F\in C^2$:
$$\boxed{F_y-\frac{d}{dx}F_{y'}=0}\qquad\text{expanded: } F_{y'y'}y''+F_{y'y}y'+F_{y'x}-F_y=0$$
Second-order ODE; its solutions are **extremals**. It is *necessary*, not sufficient.

### Special cases (first integrals)
| $F$ depends on | Reduced equation |
|---|---|
| $F(x,y')$ ($y$ absent) | $F_{y'}=c$ |
| $F(y,y')$ ($x$ absent) | **Beltrami:** $F-y'F_{y'}=c$ |
| $F(x,y)$ ($y'$ absent) | $F_y=0$ (algebraic, generally no BC fit) |
| $F(y')$ only | $y''=0$ ⇒ straight lines (if $F''\ne0$) |
| $F=M(x,y)+N(x,y)y'$ (linear in $y'$) | EL ⇔ $M_y=N_x$; if exact, $J$ is path-independent (EL holds identically) |

Linear-in-$y'$ trap: $\int(y^2+2xyy')dx=[xy^2]_a^b$ – every admissible curve is "extremal".

### Quick EL results
| $F$ | EL | Extremal |
|---|---|---|
| $y'^2+2fy$ | $y''=f$ | integrate twice |
| $y'^2-y^2$ | $y''+y=0$ | $A\cos x+B\sin x$ |
| $y'^2+y^2$ | $y''-y=0$ | $A\cosh x+B\sinh x$ |
| $y'^2-y^2+2xy$ | $y''+y=x$ | $x+A\cos x+B\sin x$ |
| $\sqrt{1+y'^2}$ | $y''=0$ | straight line |
| $y\sqrt{1+y'^2}$ | Beltrami | catenary $y=c\cosh\frac{x-d}{c}$ |
| $\sqrt{1+y'^2}/\sqrt{y}$ (brachistochrone, $y$ downward) | Beltrami: $y(1+y'^2)=k$ | cycloid $x=a(\theta-\sin\theta),\ y=a(1-\cos\theta)$ |
| $x\,y'^2$ … ($y$ absent) | $xy'=c$ | $y=c\ln x+d$ |

## 3. Classic problems
| Problem | Answer |
|---|---|
| Shortest curve in a plane | straight line |
| Brachistochrone | cycloid |
| Minimal surface of revolution | catenary (catenoid) |
| Geodesics on sphere | great circles |
| Geodesics on circular cylinder | helices (incl. generators, circles) |
| Isoperimetric (max area, fixed perimeter) | circle |
| Hanging chain (min potential energy, fixed length) | catenary |

## 4. Generalisations
- **Several functions** $F(x,y_1,\dots,y_n,y_1',\dots,y_n')$: $F_{y_i}-\frac{d}{dx}F_{y_i'}=0$, $i=1..n$ (a system).
- **Higher derivatives** $F(x,y,y',\dots,y^{(n)})$: **Euler–Poisson**
$$F_y-\frac{d}{dx}F_{y'}+\frac{d^2}{dx^2}F_{y''}-\cdots+(-1)^n\frac{d^n}{dx^n}F_{y^{(n)}}=0$$
  order $2n$; needs $2n$ BCs ($y,\dots,y^{(n-1)}$ at both ends).
- **Several independent variables** $\iint F(x,y,u,u_x,u_y)$: **Ostrogradsky** $F_u-\partial_x F_{u_x}-\partial_y F_{u_y}=0$. E.g. $\iint(u_x^2+u_y^2)$ ⇒ Laplace $\nabla^2u=0$.
- **Isoperimetric** (constraint $\int G\,dx=\ell$): apply EL to $H=F+\lambda G$ (Lagrange multiplier). If $y$ is an extremal of $\int G$ itself, the rule needs modification (abnormal case).
- **Holonomic constraint** $\phi(x,y,z)=0$: EL for $F+\lambda(x)\phi$.

## 5. Boundary conditions
- Fixed ends: $y(a)=A$, $y(b)=B$.
- **Free end** at $x=b$ (natural BC): $F_{y'}\big|_{x=b}=0$.
- **Variable end** on curve $y=\varphi(x)$ (transversality): $\big[F+(\varphi'-y')F_{y'}\big]_{x=b}=0$. For $F=f(x,y)\sqrt{1+y'^2}$ this is **orthogonality**: $y'\varphi'=-1$.
- Free end with $x=b$ free and $y$ free: $F_{y'}=0$ and $F-y'F_{y'}=0$.

## 6. Sufficient conditions (weak minimum)
Second variation: $\delta^2J=\int_a^b(Ph'^2+Qh^2)dx$, $P=\tfrac12F_{y'y'}$, $Q=\tfrac12\big(F_{yy}-\tfrac{d}{dx}F_{yy'}\big)$.
| Condition | Statement | Role |
|---|---|---|
| Euler | $y$ satisfies EL | necessary |
| **Legendre** | $F_{y'y'}\ge0$ along extremal (min); $\le0$ (max) | necessary |
| Strengthened Legendre | $F_{y'y'}>0$ | needed for sufficiency |
| **Jacobi** | no point conjugate to $a$ in $(a,b]$ | necessary in weak form ($(a,b)$), strict form sufficient with strengthened Legendre |
| **Weierstrass** $E$-function | $E=F(x,y,p)-F(x,y,y')-(p-y')F_{y'}(x,y,y')\ge0$ | for strong minimum |

- **Jacobi equation:** $\frac{d}{dx}(Ph')-Qh=0$, $h(a)=0$, $h'(a)=1$. A **conjugate point** $\tilde a$ is the next zero of $h$.
- **Sufficient (weak min):** EL + $P>0$ on $[a,b]$ + no conjugate point in $(a,b]$.
- Example: $\int_0^a(y'^2-y^2)$: Jacobi $h''+h=0$ ⇒ $h=\sin x$, conjugate point $\pi$. $y\equiv0$ is a min iff $a<\pi$ (at $a\ge\pi$ it fails; at $a>\pi$ $J$ can be made negative).
- If $F_{y'y'}>0$ for **all** $(x,y,y')$ and the extremal is unique/fits a field, often a global min (convexity in $y'$, and in $(y,y')$ jointly ⇒ global min).

## 7. Exam traps
- EL sign: $F_y\mathbf{-}\frac{d}{dx}F_{y'}$; Euler–Poisson signs **alternate** ($+$ on the $y''$ term).
- Beltrami ($x$ absent) is $F-y'F_{y'}=c$, not $F_{y'}=c$ (that is for $y$ absent).
- EL is necessary only; Legendre is necessary only; Legendre + Jacobi gives sufficiency.
- Conjugate point **at** $b$ already destroys strict sufficiency.
- Integrand linear in $y'$ and exact ⇒ $J$ depends only on end points.
- Free end ⇒ natural BC $F_{y'}=0$, do not invent $y=0$.
- Isoperimetric problems: use $F+\lambda G$, then fix $\lambda$ from the constraint.
- $\int y^2$, $\int(y+1)$, $|y(0)|$ are not linear functionals.
