# Cheatsheet · Unit 9 · Topic 09 — Numerical Differentiation and Integration
> Questions: [../Questions/09-Numerical-Differentiation-Integration.md](../Questions/09-Numerical-Differentiation-Integration.md)

## 1. Numerical differentiation
### From the difference-operator series ($hD=\log E$)
- **Forward** at $x_0$: $f'(x_0)=\frac1h\left[\Delta-\frac{\Delta^2}{2}+\frac{\Delta^3}{3}-\frac{\Delta^4}{4}+\cdots\right]y_0$
- $f''(x_0)=\frac1{h^2}\left[\Delta^2-\Delta^3+\frac{11}{12}\Delta^4-\cdots\right]y_0$
- **Backward** at $x_n$: $f'(x_n)=\frac1h\left[\nabla+\frac{\nabla^2}{2}+\frac{\nabla^3}{3}+\cdots\right]y_n$
- $f''(x_n)=\frac1{h^2}\left[\nabla^2+\nabla^3+\frac{11}{12}\nabla^4+\cdots\right]y_n$

### Finite-difference formulas and errors
| Formula | Approximates | Truncation error |
|---|---|---|
| $\frac{f(x+h)-f(x)}{h}$ | $f'$ | $-\frac h2f''(\xi)$, $O(h)$ |
| $\frac{f(x)-f(x-h)}{h}$ | $f'$ | $+\frac h2f''(\xi)$, $O(h)$ |
| $\frac{f(x+h)-f(x-h)}{2h}$ | $f'$ | $-\frac{h^2}{6}f'''(\xi)$, $O(h^2)$ |
| $\frac{f(x+h)-2f(x)+f(x-h)}{h^2}$ | $f''$ | $-\frac{h^2}{12}f^{(4)}(\xi)$, $O(h^2)$ |

The error is written as (exact − approximation). Equivalently, the central difference equals $f'+\frac{h^2}6f'''+\dots$
- Differentiation is **ill-conditioned**. Round-off grows like $\varepsilon/h$, so the total error $\approx\frac{\varepsilon}{h}+Ch^p$ has an optimal $h$. Shrinking $h$ forever does not help.
- **Richardson:** if $N(h)=M+Kh^p+\dots$, then $\dfrac{2^pN(h/2)-N(h)}{2^p-1}$ removes the $h^p$ term.

## 2. Newton–Cotes integration (closed, $h=(b-a)/n$)
| Rule | Strips per panel | Single-panel formula | Panel error | Composite error | Degree of precision |
|---|---|---|---|---|---|
| Trapezoidal | 1 | $\frac h2(y_0+y_1)$ | $-\frac{h^3}{12}f''$ | $-\frac{(b-a)h^2}{12}f''$ | 1 |
| Simpson 1/3 | 2 | $\frac h3(y_0+4y_1+y_2)$ | $-\frac{h^5}{90}f^{(4)}$ | $-\frac{(b-a)h^4}{180}f^{(4)}$ | 3 |
| Simpson 3/8 | 3 | $\frac{3h}8(y_0+3y_1+3y_2+y_3)$ | $-\frac{3h^5}{80}f^{(4)}$ | $-\frac{(b-a)h^4}{80}f^{(4)}$ | 3 |
| Boole | 4 | $\frac{2h}{45}(7y_0+32y_1+12y_2+32y_3+7y_4)$ | $-\frac{8h^7}{945}f^{(6)}$ | $O(h^6)$ | 5 |
| Weddle | 6 | $\frac{3h}{10}(y_0+5y_1+y_2+6y_3+y_4+5y_5+y_6)$ | $-\frac{h^7}{140}f^{(6)}$ (approximately) | $O(h^6)$ | 5 |

**Composite formulas**
- Trapezoidal: $\frac h2[y_0+2(y_1+\dots+y_{n-1})+y_n]$, for any $n$.
- Simpson 1/3: $\frac h3[y_0+4(\text{odd})+2(\text{even interior})+y_n]$. $n$ must be **even**.
- Simpson 3/8: $n$ must be a **multiple of 3**. Weddle: $n$ must be a **multiple of 6**.
- **Degree of precision (DoP)** is the largest $m$ such that the rule is exact for $1,x,\dots,x^m$. A closed Newton–Cotes rule on $n+1$ points has DoP $n+1$ if $n$ is even and $n$ if $n$ is odd. This is why Simpson 1/3 (3 points) and 3/8 (4 points) have the same DoP of 3.
- Convexity: $f''\gt 0$ means the trapezoidal rule **overestimates** and the midpoint rule $h f(\text{mid})$ (error $+\frac{h^3}{24}f''$) **underestimates**.
- Newton–Cotes rules of high order have negative weights and are unstable, so composite low-order rules are used instead.
- **Romberg:** $R(k,j)=\dfrac{4^{j}R(k,j-1)-R(k-1,j-1)}{4^{j}-1}$. The first extrapolation of the trapezoidal rule gives Simpson's rule, and the second gives Boole's rule.

## 3. Gaussian quadrature
$$\int_{-1}^1f(x)\thinspace dx\approx\sum_{i=1}^nw_if(x_i),\qquad x_i=\text{zeros of }P_n,\qquad \text{DoP}=2n-1\ (\text{maximum possible}).$$
| $n$ | Nodes | Weights |
|---|---|---|
| 1 | $0$ | $2$ (midpoint rule) |
| 2 | $\pm\frac1{\sqrt3}$ | $1,1$ |
| 3 | $0,\ \pm\sqrt{3/5}$ | $\frac89,\ \frac59,\frac59$ |
- All weights are positive and sum to 2 (the length of $[-1,1]$). The nodes are interior points.
- Error for $n$ points: $\dfrac{2^{2n+1}(n!)^4}{(2n+1)[(2n)!]^3}f^{(2n)}(\xi)$. For $n=2$ this is $\frac1{135}f^{(4)}$.
- For $[a,b]$, substitute $x=\frac{b-a}{2}t+\frac{a+b}{2}$, so $dx=\frac{b-a}2dt$.
- Variants: Gauss–Chebyshev (weight $1/\sqrt{1-x^2}$, equal weights $\pi/n$), Gauss–Laguerre on $[0,\infty)$ with weight $e^{-x}$, Gauss–Hermite with weight $e^{-x^2}$.

## 4. Standard checks
- $\int_0^1x^2$: trapezoidal ($h=0.5$) gives $0.375$, Simpson gives $1/3$ (exact).
- $\int_0^1\frac{dx}{1+x}$ ($h=0.5$): trapezoidal gives $0.7083$, Simpson gives $0.6944$, the exact value is $\ln2=0.6931$.
- $\int_{-1}^1x^4$: 2-point Gauss gives $2/9$, the exact value is $2/5$.

## Exam traps
- Simpson's rule is exact for **cubics**, not just quadratics. Its DoP is 3, not 2.
- Simpson 1/3 and 3/8 have the **same** DoP (3) and the same order $h^4$. 3/8 has the larger error constant ($\frac{3}{80}$ vs $\frac{1}{90}$ per panel).
- The $n$-point Gauss rule has DoP $2n-1$, not $2n$ or $n$.
- Composite Simpson needs an even number of strips, which means an odd number of ordinates.
- The trapezoidal rule's panel error is $O(h^3)$, but its composite (global) error is $O(h^2)$.
- In numerical differentiation, smaller $h$ is not always better because of round-off.
