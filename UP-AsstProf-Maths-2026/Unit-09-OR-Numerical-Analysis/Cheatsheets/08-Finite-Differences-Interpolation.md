# Cheatsheet · Unit 9 · Topic 08 — Finite Differences and Interpolation
> Questions: [../Questions/08-Finite-Differences-Interpolation.md](../Questions/08-Finite-Differences-Interpolation.md)

## 1. Difference operators (step $h$, $`y_k=f(x_0+kh)`$)
| Operator | Definition | In terms of $E$ | In terms of $D=\frac{d}{dx}$ |
|---|---|---|---|
| Shift $E$ | $Ef(x)=f(x+h)$ | $E$ | $e^{hD}$ |
| Forward $\Delta$ | $f(x+h)-f(x)$ | $E-1$ | $e^{hD}-1$ |
| Backward $\nabla$ | $f(x)-f(x-h)$ | $1-E^{-1}$ | $1-e^{-hD}$ |
| Central $\delta$ | $f(x+\frac h2)-f(x-\frac h2)$ | $E^{1/2}-E^{-1/2}$ | $2\sinh\frac{hD}{2}$ |
| Average $\mu$ | $\frac12[f(x+\frac h2)+f(x-\frac h2)]$ | $\frac12(E^{1/2}+E^{-1/2})$ | $\cosh\frac{hD}{2}$ |

**Key identities**
- $\nabla=E^{-1}\Delta$, $\Delta=E\nabla$, $\delta=E^{1/2}\nabla=E^{-1/2}\Delta$
- $\Delta-\nabla=\Delta\nabla=\nabla\Delta=\delta^2$
- $\mu^2=1+\frac14\delta^2$, $\mu\delta=\frac12(\Delta+\nabla)=\frac12(E-E^{-1})$
- $hD=\log(1+\Delta)=-\log(1-\nabla)=2\sinh^{-1}(\delta/2)$
- $(1+\Delta)(1-\nabla)=1$

**Differences of polynomials**
- $`\Delta^n x^n=n!\thinspace h^n`$. For a degree-$`n`$ polynomial with leading coefficient $`a`$, $`\Delta^n p=a\thinspace n!\thinspace h^n`$ (constant) and $`\Delta^{n+1}p=0`$.
- **Factorial polynomial** $x^{(r)}=x(x-h)\cdots(x-(r-1)h)$ satisfies $\Delta x^{(r)}=rh\thinspace x^{(r-1)}$.
- $\Delta^n y_0=\sum_{k=0}^n(-1)^{k}\binom nk y_{n-k}$. Use it to find missing entries: when the data come from a degree-$`(n-1)`$ polynomial, set $\Delta^n y_0=0$.
- $\Delta(fg)=f(x+h)\Delta g+g\Delta f$, and $\Delta\frac fg=\frac{g\Delta f-f\Delta g}{g(x)g(x+h)}$.
- Error propagation: an error $\varepsilon$ in a single entry spreads in $\Delta^k$ with binomial coefficients $\binom{k}{j}(-1)^j\varepsilon$.

## 2. Newton's equal-interval formulas ($u=(x-x_0)/h$, or $(x-x_n)/h$)
- **Forward** (start of the table): $p(x)=y_0+u\Delta y_0+\frac{u(u-1)}{2!}\Delta^2y_0+\dots$
- **Backward** (end of the table): $p(x)=y_n+u\nabla y_n+\frac{u(u+1)}{2!}\nabla^2y_n+\dots$
- **Central formulas** (middle of the table): Gauss forward and backward, **Stirling** (average of the two Gauss formulas, best near $|u|\lt 1/4$), **Bessel** (best near $u\approx1/2$), Everett.
- Error of the forward formula: $\dfrac{u(u-1)\cdots(u-n)}{(n+1)!}h^{n+1}f^{(n+1)}(\xi)$.

## 3. Lagrange interpolation (arbitrary distinct nodes)
$$p_n(x)=\sum_{i=0}^n y_i\thinspace \ell_i(x),\qquad \ell_i(x)=\prod_{j\ne i}\frac{x-x_j}{x_i-x_j},\qquad \sum_i\ell_i(x)\equiv1,\ \ \ell_i(x_j)=\delta_{ij}.$$
- **Uniqueness:** exactly one polynomial of degree $`\le n`$ passes through $`n+1`$ points with distinct abscissae, because a nonzero polynomial of degree $`\le n`$ has at most $`n`$ roots.
- **Error:** $f(x)-p_n(x)=\dfrac{f^{(n+1)}(\xi)}{(n+1)!}\thinspace \omega(x)$, where $\omega(x)=\prod_{i=0}^n(x-x_i)$.
- Drawback: adding a node means recomputing everything. Newton's divided-difference form avoids this.

## 4. Divided differences
$$f[x_0]=f(x_0),\quad f[x_0,\dots,x_k]=\frac{f[x_1,\dots,x_k]-f[x_0,\dots,x_{k-1}]}{x_k-x_0}.$$
- They are **symmetric** in their arguments.
- $f[x_0,\dots,x_n]=\dfrac{f^{(n)}(\xi)}{n!}$ (mean value property).
- For a degree-$`n`$ polynomial, the $`n`$-th divided difference is the leading coefficient (constant) and the $(n+1)$-th is 0.
- With equal spacing, $f[x_0,\dots,x_k]=\dfrac{\Delta^ky_0}{k!\thinspace h^k}$.
- Standard results: $x^3$ gives $f[a,b,c]=a+b+c$ and $f[a,b,c,d]=1$; $1/x$ gives $f[x_0,\dots,x_n]=\dfrac{(-1)^n}{x_0x_1\cdots x_n}$.
- **Newton form:** $`p_n(x)=f[x_0]+f[x_0,x_1](x-x_0)+\dots+f[x_0,\dots,x_n]\prod_{i\lt n}(x-x_i)`$.

## 5. Hermite interpolation
- Data $f(x_i)$ and $f'(x_i)$ at $n+1$ nodes give $2n+2$ conditions and a unique $H$ of degree $\le 2n+1$.
- $H(x)=\sum_i\big[1-2\ell_i'(x_i)(x-x_i)\big]\ell_i^2(x)\thinspace f_i+\sum_i (x-x_i)\ell_i^2(x)\thinspace f_i'$.
- **Error:** $f(x)-H(x)=\dfrac{f^{(2n+2)}(\xi)}{(2n+2)!}\thinspace \omega(x)^2$.
- Two nodes give the cubic Hermite interpolant. Divided differences with repeated nodes use $f[x_i,x_i]=f'(x_i)$.

## 6. Cubic splines
**Definition:** $S$ is a cubic on each $[x_{i-1},x_i]$ with $S,S',S''$ continuous ($S\in C^2$), and $S(x_i)=y_i$.
- Counting: $4n$ unknowns against $4n-2$ conditions, so **2 extra conditions** are needed.
  - **Natural:** $S''(x_0)=S''(x_n)=0$.
  - **Clamped:** $S'(x_0)=f'(x_0)$ and $S'(x_n)=f'(x_n)$.
  - **Not-a-knot or periodic** are the other choices.
- With $M_i=S''(x_i)$ and uniform $h$: $M_{i-1}+4M_i+M_{i+1}=\dfrac{6}{h^2}(y_{i-1}-2y_i+y_{i+1})$. This is a tridiagonal, diagonally dominant system with a unique solution.
- **Minimum curvature property:** the natural spline minimises $\int (g'')^2$ among all $C^2$ interpolants.
- Clamped spline error: $\Vert f-S\Vert _\infty\le\frac{5}{384}h^4\Vert f^{(4)}\Vert _\infty$.
- Splines avoid the **Runge phenomenon**: high-degree equispaced interpolation of $1/(1+25x^2)$ diverges near $\pm1$. Chebyshev nodes are the other cure.
- Linear spline: continuous only, error $\le\frac{h^2}{8}\max|f''|$.

## Exam traps
- Interpolation error uses $(n+1)!$ and $f^{(n+1)}$. Hermite uses $(2n+2)!$, $f^{(2n+2)}$ and $\omega^2$.
- $\nabla=E^{-1}\Delta$, not $E\Delta$.
- $\Delta^n x^n=n!\thinspace h^n$, so don't forget $h^n$. With $h=1$, $\Delta^{n+1}$ of a degree-$`n`$ polynomial is $0$.
- A spline is piecewise cubic, not a single cubic. A cubic spline is $C^2$, not $C^3$.
- Lagrange, Newton forward and Newton divided-difference formulas on the same data give the **same** polynomial. Only the form differs.
- A "missing entry" is computed from $\Delta^ky_0=0$ with the right $k$. With $m$ known values, fit a degree-$`(m-1)`$ polynomial and set $\Delta^{m}y_0=0$. For example, 4 known values out of 5 entries give $\Delta^4y_0=0$.
