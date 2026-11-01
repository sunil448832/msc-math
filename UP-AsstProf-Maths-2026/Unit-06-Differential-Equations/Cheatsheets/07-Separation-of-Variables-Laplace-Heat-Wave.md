# Cheatsheet · Unit 6 · Topic 07 — Separation of Variables: Laplace, Heat and Wave Equations
> Questions: [../Questions/07-Separation-of-Variables-Laplace-Heat-Wave.md](../Questions/07-Separation-of-Variables-Laplace-Heat-Wave.md)

## 0. The method
1. Assume $u=X(x)T(t)$ (or $X(x)Y(y)$, or $R(r)\Theta(\theta)$) and divide through, e.g. $\frac{X''}{X}=\frac{T'}{kT}=-\lambda$.
2. Solve the **spatial eigenvalue problem**, using the homogeneous BCs (see Topic 04).
3. Solve the other ODE for each $\lambda_n$.
4. Superpose: $u=\sum c_nX_nT_n$, and fix $c_n$ from the initial or non-homogeneous data via Fourier coefficients.
5. **Non-homogeneous BCs:** write $u=v(x)+w(x,t)$, where $v$ is the steady state, so that $w$ has homogeneous BCs.

**Fourier coefficients on $(0,L)$:**
$$b_n=\frac2L\int_0^Lf(x)\sin\frac{n\pi x}{L}dx,\qquad a_n=\frac2L\int_0^Lf(x)\cos\frac{n\pi x}{L}dx .$$
| $f$ on $(0,\pi)$ | sine coefficients $b_n$ |
|---|---|
| $1$ | $\frac{2(1-(-1)^n)}{n\pi}$, i.e. $\frac{4}{n\pi}$ for odd $n$ and $0$ for even $n$ |
| $x$ | $\frac{2(-1)^{n+1}}{n}$ |
| $x(\pi-x)$ | $\frac{4(1-(-1)^n)}{\pi n^3}$, i.e. $\frac{8}{\pi n^3}$ for odd $n$ |
| $\sin mx$ | $\delta_{nm}$ (read it off directly) |

## 1. Heat equation $u_t=k\,u_{xx}$ on $0<x<L$
| BCs | Solution |
|---|---|
| $u(0)=u(L)=0$ | $u=\sum b_n e^{-k(n\pi/L)^2t}\sin\frac{n\pi x}{L}$ |
| $u_x(0)=u_x(L)=0$ | $u=\frac{a_0}{2}+\sum a_ne^{-k(n\pi/L)^2t}\cos\frac{n\pi x}{L}$, which tends to the **mean** $\frac1L\int f$ |
| $u(0)=T_1,\ u(L)=T_2$ | $u=T_1+\frac{(T_2-T_1)x}{L}+w$, where $w$ satisfies the Dirichlet problem with $w(x,0)=f-v$ |

- **Time factor:** $e^{-k\lambda t}$ with $\lambda=(n\pi/L)^2$, so the exponent involves $n^2$, not $n$.
- **Properties:** maximum principle (max/min attained at $t=0$ or on the boundary), uniqueness, **instant smoothing** ($u\in C^\infty$ for $t>0$), infinite speed of propagation, and backward-in-time ill-posedness.
- **On $\mathbb{R}$:** $u=\frac{1}{\sqrt{4\pi kt}}\int e^{-(x-s)^2/4kt}f(s)\,ds$ (the heat kernel).

## 2. Wave equation $u_{tt}=c^2u_{xx}$
**d'Alembert's formula (on $\mathbb{R}$):**
$$u(x,t)=\frac{f(x+ct)+f(x-ct)}{2}+\frac1{2c}\int_{x-ct}^{x+ct}g(s)\,ds .$$
- The domain of dependence of $(x_0,t_0)$ is $[x_0-ct_0,\,x_0+ct_0]$. Signals travel at the finite speed $c$.
- Singularities **propagate** along the characteristics $x\pm ct=$ const and are not smoothed.
- A classical solution needs $f\in C^2$ and $g\in C^1$.

**Finite string, fixed ends ($0<x<L$):**
$$u=\sum_{n\ge1}\Big(A_n\cos\frac{n\pi ct}{L}+B_n\sin\frac{n\pi ct}{L}\Big)\sin\frac{n\pi x}{L},$$
$$A_n=\frac2L\int_0^Lf\sin\frac{n\pi x}{L},\qquad B_n=\frac{2}{n\pi c}\int_0^Lg\sin\frac{n\pi x}{L}.$$
- The $n$th mode has angular frequency $\omega_n=\frac{n\pi c}{L}$ and frequency $\nu_n=\frac{nc}{2L}$. The fundamental is $\nu_1=\frac{1}{2L}\sqrt{T/\rho}$.
- Every solution is periodic in $t$ with period $2L/c$.
- **Energy:** $E=\frac12\int_0^L(u_t^2+c^2u_x^2)\,dx$ is conserved (for fixed or free ends).
- **Plucked string** (triangle of height $h$ at the midpoint): $A_n=\frac{8h}{n^2\pi^2}\sin\frac{n\pi}{2}$.

## 3. Laplace's equation $\nabla^2u=0$
**Rectangle** $0<x<a$, $0<y<b$, with $u=0$ on three sides and $u(x,b)=f(x)$:
$$u=\sum B_n\sin\frac{n\pi x}{a}\sinh\frac{n\pi y}{a},\qquad B_n=\frac{2}{a\sinh(n\pi b/a)}\int_0^af\sin\frac{n\pi x}{a}dx .$$
If the non-zero side is $y=0$, use $\sinh\frac{n\pi(b-y)}{a}$. For a semi-infinite strip $y>0$ with $u$ bounded, use $e^{-n\pi y/a}$.

**Disc** $r<a$, with $u(a,\theta)=f(\theta)$ (bounded at $r=0$):
$$u=\frac{a_0}{2}+\sum_{n\ge1}\Big(\frac ra\Big)^n(a_n\cos n\theta+b_n\sin n\theta),$$
where $a_n,b_n$ are the Fourier coefficients of $f$.
- The **exterior** problem uses $(a/r)^n$.
- An **annulus** uses $c_0+d_0\ln r+\sum(c_nr^n+d_nr^{-n})(\dots)$.
- **Poisson kernel:** $u(r,\theta)=\frac{1}{2\pi}\int_0^{2\pi}\frac{a^2-r^2}{a^2-2ar\cos(\theta-\phi)+r^2}f(\phi)\,d\phi$.
- **Example:** $f=\cos^2\theta$ gives $u=\frac12+\frac{r^2}{2}\cos2\theta$ (on the unit disc).
- **Properties:** mean value property, maximum principle, uniqueness for the Dirichlet problem, and real-analyticity. The Neumann problem is solvable only if $\oint\partial_nu=0$, and its solution is unique up to a constant.
- **Separated forms:** in Cartesian coordinates, $X''=-\lambda X$ and $Y''=\lambda Y$ give trig × hyperbolic. In polar coordinates, $r^2R''+rR'-n^2R=0$ (Euler) gives $r^{\pm n}$ (and $1,\ln r$ for $n=0$).

## 4. Quick comparison
| | Heat | Wave | Laplace |
|---|---|---|---|
| Type | parabolic | hyperbolic | elliptic |
| Data | IC + BC | 2 ICs + BC | BC only |
| Time factor | $e^{-k\lambda t}$ | $\cos/\sin(c\sqrt\lambda t)$ | (none; $\sinh/\cosh$ in $y$) |
| Smoothing | yes | no | solutions analytic |
| Speed | infinite | finite $c$ | – |
| Energy / max principle | max principle | energy conserved | max principle |

## Exam traps
- In the heat equation, the exponent is $-k\,n^2\pi^2t/L^2$. Using $n$ instead of $n^2$ is a classic distractor.
- For a string started with velocity $g$, divide by $\frac{n\pi c}{L}$: $B_n=\frac{2}{n\pi c}\int g\sin$.
- If the initial data is already a finite sine sum, **read off the coefficients** rather than integrating.
- Neumann conditions lead to the mean value of the initial data, not to $0$.
- Interior disc: $r^n$ only (drop $r^{-n}$ and $\ln r$). Exterior: $r^{-n}$.
- At the centre of a disc, $u$ equals the **mean of the boundary data** ($a_0/2$).
- Dirichlet in $x$ with $u=0$ on $y=0$ leads to $\sinh$, not $\cosh$.
