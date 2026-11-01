# Cheatsheet · Unit 9 · Topic 06 — Roots: Bisection, Fixed Point, Newton–Raphson
> Questions: [../Questions/06-Roots-Bisection-Fixed-Point-Newton-Raphson.md](../Questions/06-Roots-Bisection-Fixed-Point-Newton-Raphson.md)

## 1. Order of convergence
If $e_n=x_n-\alpha\to0$ and $\displaystyle\lim\frac{|e_{n+1}|}{|e_n|^p}=C\ne0$ (finite), the **order** is $p$ and $C$ is the asymptotic error constant.
- $p=1$ (linear) requires $0<C<1$. $p=2$ is quadratic.
- Roughly, each step multiplies the number of correct digits by $p$.

## 2. Bisection
- **Hypothesis:** $f$ continuous on $[a,b]$ and $f(a)f(b)<0$. Then IVT gives a root, and the method **always converges**.
- Error bound $|x_n-\alpha|\le \dfrac{b-a}{2^{n}}$ (or $\frac{b-a}{2^{n+1}}$ when the midpoint of the $n$-th interval is the estimate).
- Steps needed for tolerance $\varepsilon$: $n\ge \dfrac{\log\big((b-a)/\varepsilon\big)}{\log2}$.
- Linear convergence (ratio $1/2$ of the bound). It uses only the sign of $f$.

## 3. Regula falsi and secant
$$x_{n+1}=\frac{x_{n-1}f(x_n)-x_nf(x_{n-1})}{f(x_n)-f(x_{n-1})}$$
| | Regula falsi | Secant |
|---|---|---|
| Keeps a bracket? | Yes (keeps the sign change) | No |
| Always converges (given a bracket)? | Yes | No |
| Order | 1 (one endpoint often stays fixed) | $\frac{1+\sqrt5}{2}\approx1.618$ |
| New $f$-evaluations per step | 1 | 1 |

## 4. Fixed-point iteration $x_{n+1}=g(x_n)$
**Existence:** if $g\in C[a,b]$ and $g([a,b])\subseteq[a,b]$, then a fixed point exists (apply IVT to $g(x)-x$).
**Uniqueness and convergence (contraction):** if also $|g'(x)|\le k<1$ on $[a,b]$, the fixed point is unique, the iteration converges for **every** $x_0\in[a,b]$, and
$$|x_n-\alpha|\le k^n|x_0-\alpha|,\qquad |x_n-\alpha|\le\frac{k^n}{1-k}|x_1-x_0|.$$
**Local behaviour at $\alpha$:**
- $|g'(\alpha)|<1$ gives local convergence (attracting). $|g'(\alpha)|>1$ gives divergence (repelling).
- $e_{n+1}\approx g'(\alpha)e_n$. If $g'(\alpha)>0$ the approach is monotone; if $g'(\alpha)<0$ it oscillates.
- If $g'(\alpha)=\dots=g^{(p-1)}(\alpha)=0\ne g^{(p)}(\alpha)$, the order is $p$.

*Example:* for $x^2-3x+2=0$, $g(x)=(x^2+2)/3$ attracts to 1 ($g'=2/3$) and repels from 2 ($g'=4/3$).

## 5. Newton–Raphson
$$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)},\qquad e_{n+1}\approx\frac{f''(\alpha)}{2f'(\alpha)}\,e_n^2.$$
- It is fixed-point iteration with $g=x-f/f'$. For a simple root $g'(\alpha)=0$, which gives **order 2**.
- **Sufficient condition (Fourier):** on $[a,b]$, let $f(a)f(b)<0$, let $f'$ and $f''$ keep constant signs, and let $f(x_0)f''(x_0)>0$. Then Newton converges monotonically.
- At a root of **multiplicity $m$**: $g'(\alpha)=1-\frac1m$, so convergence is **linear** with ratio $1-1/m$. The fix $x_{n+1}=x_n-m\,f/f'$ is quadratic again. Newton applied to $u=f/f'$ also works.
- It is an open method. It can cycle (e.g. $x^3-2x+2$ with $x_0=0$ gives $0\to1\to0$), diverge, or fail when $f'(x_n)=0$.
- Each step costs 2 evaluations ($f$ and $f'$). The efficiency index is $2^{1/2}\approx1.414$, against $1.618$ for secant.

### Standard Newton iterations
| Target | $f(x)$ | Iteration |
|---|---|---|
| $\sqrt N$ | $x^2-N$ | $\tfrac12\left(x+\tfrac Nx\right)$ (Heron) |
| $\sqrt[k]{N}$ | $x^k-N$ | $\tfrac1k\left((k-1)x+\tfrac{N}{x^{k-1}}\right)$ |
| $1/N$ (no division) | $\tfrac1x-N$ | $x(2-Nx)$ |
| $1/\sqrt N$ | $\tfrac1{x^2}-N$ | $\tfrac12x(3-Nx^2)$ |

For $1/N$, the iteration converges iff $0<x_0<2/N$.

## 6. Orders at a glance
| Method | Order | Bracketing? |
|---|---|---|
| Bisection | 1 | yes |
| Regula falsi | 1 | yes |
| Secant | 1.618 | no |
| Muller | 1.84 | no |
| Newton–Raphson | 2 | no |
| Chebyshev / Halley | 3 | no |
| Fixed point, $g'(\alpha)\ne0$ | 1 | no |

## 7. Graeffe / polynomial facts (occasionally asked)
- Descartes' rule of signs: the number of positive roots is at most the number of sign changes in the coefficients of $f(x)$, and differs from it by an even number.
- Newton's method on a polynomial uses synthetic division (Horner) to evaluate $f$ and $f'$.

## Exam traps
- "Newton always converges" is false. It is **locally** quadratic only.
- Quadratic convergence of fixed-point iteration needs $g'(\alpha)=0$, not just $|g'(\alpha)|<1$.
- Newton at a double root is **linear** with ratio $1/2$, and at a root of multiplicity $m$ the ratio is $1-1/m$.
- Bisection's convergence does not depend on smoothness, only on continuity and a sign change.
- Regula falsi brackets but is only linear. Secant does not bracket but is superlinear.
- Count bisection steps with $2^n>(b-a)/\varepsilon$ and check whether the question uses $2^n$ or $2^{n+1}$.
