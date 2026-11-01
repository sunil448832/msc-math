# Cheatsheet · Unit 6 · Topic 04 — Sturm–Liouville Boundary Value Problems
> Questions: [../Questions/04-Sturm-Liouville-BVP.md](../Questions/04-Sturm-Liouville-BVP.md)

## 1. Self-adjoint form
Any equation $a_0y''+a_1y'+a_2y=0$ with $a_0\ne0$ can be put in **self-adjoint form**
$$\big(p(x)y'\big)'+q(x)y=0,\qquad p=e^{\int a_1/a_0\,dx},\quad q=\frac{a_2}{a_0}\,p .$$
- $L[y]=a_0y''+a_1y'+a_2y$ is **formally self-adjoint** iff $a_0'=a_1$.
- **Lagrange identity:** $uL[v]-vL[u]=\frac{d}{dx}\big[p(uv'-vu')\big]$.
- **Green's formula:** $\int_a^b(uLv-vLu)\,dx=\big[p(uv'-vu')\big]_a^b$.

## 2. Sturm–Liouville problem
$$(p y')'+(q+\lambda r)y=0,\quad a<x<b,$$
$$\alpha_1y(a)+\alpha_2y'(a)=0,\qquad \beta_1y(b)+\beta_2y'(b)=0 \quad(\text{separated conditions}).$$
The problem is **regular** if $p,p',q,r$ are continuous on $[a,b]$, $p>0$ and $r>0$ on $[a,b]$, and the boundary conditions are separated. It is **singular** if $p$ vanishes at an endpoint (Legendre, Chebyshev) or the interval is infinite (Hermite, Laguerre). In that case boundedness replaces a boundary condition.

**Theorems for a regular S–L problem:**
1. The eigenvalues are **real** and **simple** (each has one eigenfunction up to a constant).
2. They form a sequence $\lambda_1<\lambda_2<\dots\to\infty$, so there is a smallest eigenvalue.
3. Eigenfunctions for distinct eigenvalues are **orthogonal with weight $r$**: $\int_a^b r\,\phi_m\phi_n\,dx=0$.
4. The $n$th eigenfunction has exactly $n-1$ zeros in $(a,b)$.
5. The eigenfunctions are complete: $f\sim\sum c_n\phi_n$ with $c_n=\frac{\int rf\phi_n}{\int r\phi_n^2}$.
6. If $q\le0$ and $\alpha_1\alpha_2\le0$, $\beta_1\beta_2\ge0$, then all $\lambda\ge0$. **Rayleigh quotient:** $\lambda=\frac{-[p\phi\phi']_a^b+\int(p\phi'^2-q\phi^2)}{\int r\phi^2}$.

**Periodic conditions** ($y(a)=y(b)$, $y'(a)=y'(b)$, $p(a)=p(b)$) also give a self-adjoint problem, but eigenvalues can be **double**: on $[-\pi,\pi]$, $\lambda=n^2$ has eigenfunctions $\cos nx$ and $\sin nx$.

## 3. Standard eigenvalue problems for $y''+\lambda y=0$ on $[0,L]$
| BCs | $\lambda_n$ | $\phi_n$ |
|---|---|---|
| $y(0)=y(L)=0$ | $(n\pi/L)^2,\ n\ge1$ | $\sin\frac{n\pi x}{L}$ |
| $y'(0)=y'(L)=0$ | $(n\pi/L)^2,\ n\ge0$ (includes $0$) | $\cos\frac{n\pi x}{L}$ |
| $y(0)=0,\ y'(L)=0$ | $\big(\frac{(2n-1)\pi}{2L}\big)^2$ | $\sin\frac{(2n-1)\pi x}{2L}$ |
| $y'(0)=0,\ y(L)=0$ | $\big(\frac{(2n-1)\pi}{2L}\big)^2$ | $\cos\frac{(2n-1)\pi x}{2L}$ |
| periodic on $[-L,L]$ | $(n\pi/L)^2,\ n\ge0$ | $1$, $\cos$, $\sin$ (double for $n\ge1$) |
| $y(0)=0,\ y'(1)+hy(1)=0$ | $\lambda=k^2$, where $\tan k=-k/h$ | $\sin kx$ |
| $x^2y''+xy'+\lambda y=0,\ y(1)=y(e)=0$ | $n^2\pi^2$ | $\sin(n\pi\ln x)$, with weight $1/x$ |

## 4. Classical singular S–L problems and weights
| Equation | S–L form | Weight, interval |
|---|---|---|
| Legendre | $((1-x^2)y')'+n(n+1)y=0$ | $1$, $[-1,1]$ |
| Chebyshev | $(\sqrt{1-x^2}\,y')'+\frac{n^2}{\sqrt{1-x^2}}y=0$ | $(1-x^2)^{-1/2}$, $[-1,1]$ |
| Hermite | $(e^{-x^2}y')'+2ne^{-x^2}y=0$ | $e^{-x^2}$, $\mathbb{R}$ |
| Laguerre | $(xe^{-x}y')'+ne^{-x}y=0$ | $e^{-x}$, $[0,\infty)$ |
| Bessel (fixed $\nu$) | $(xy')'+\big(\lambda x-\frac{\nu^2}{x}\big)y=0$ | $x$, $[0,a]$; the functions are $J_\nu(\sqrt{\lambda}x)$ |

## 5. Green's function for a BVP
For $L[y]=(py')'+qy=-f$ with homogeneous separated BCs (and $0$ not an eigenvalue), take $u_1$ satisfying the left BC and $u_2$ satisfying the right BC. Then
$$G(x,s)=\begin{cases}\dfrac{u_1(x)u_2(s)}{pW},&x\le s\\[2mm]\dfrac{u_1(s)u_2(x)}{pW},&x\ge s\end{cases}\qquad pW=\text{const},\ \text{with } W=u_1u_2'-u_1'u_2,$$
and the sign is fixed by the convention used. **Properties:** $G$ is continuous, symmetric ($G(x,s)=G(s,x)$), satisfies the BCs, and its derivative $\partial_xG$ **jumps by $-1/p(s)$** at $x=s$.

| Problem | $G(x,s)$ for $x\le s$ (swap $x,s$ for $x\ge s$) |
|---|---|
| $-y''=f$, $y(0)=y(1)=0$ | $x(1-s)$ |
| $-y''=f$, $y(0)=0,\ y'(1)=0$ | $x$ |
| $-y''=f$, $y(0)=y(L)=0$ | $x(L-s)/L$ |

## 6. Sturm theorems for $y''+q(x)y=0$
- **Separation:** the zeros of two LI solutions **strictly interlace**.
- **Comparison:** if $q_2\ge q_1$ ($q_2\not\equiv q_1$), then between two consecutive zeros of a solution of $y''+q_1y=0$ lies at least one zero of every solution of $y''+q_2y=0$.
- **Spacing:** if $m^2\le q\le M^2$, consecutive zeros satisfy $\pi/M\le d\le\pi/m$.
- If $q\le0$, a non-trivial solution has **at most one zero** (non-oscillatory).
- If $q(x)\ge m^2>0$ on $[a,\infty)$, every solution has infinitely many zeros (oscillatory).
- **Bessel:** in $u=\sqrt{x}\,J_\nu$ form we have $u''+\big(1+\frac{1-4\nu^2}{4x^2}\big)u=0$, so $J_\nu$ has infinitely many positive zeros. For $\nu>\tfrac12$ the spacing exceeds $\pi$, for $\nu<\tfrac12$ it is less than $\pi$, and for $\nu=\tfrac12$ it is exactly $\pi$.
- To remove the first-derivative term, put $y=u\,e^{-\frac12\int P}$.

## Exam traps
- Dirichlet conditions start at $n=1$, Neumann conditions at $n=0$ (where $\lambda=0$ is an eigenvalue).
- Mixed conditions give odd multiples: $\lambda=\big(\frac{(2n-1)\pi}{2L}\big)^2$.
- Orthogonality is **with respect to the weight $r$**, not always $dx$. Example: $\sin(n\pi\ln x)$ is orthogonal with weight $1/x$.
- "Each eigenvalue is simple" requires **separated** conditions. It fails for periodic ones.
- The Green's function sign depends on whether the problem is written $Ly=f$ or $Ly=-f$.
- In the Sturm comparison theorem, a larger $q$ means **more** zeros (closer together).
