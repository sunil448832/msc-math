# Cheatsheet · Unit 7 · Topic 02 — Integral Equations: Volterra Type, Successive Methods
> Questions: [../Questions/02-Integral-Equations-Volterra-Successive-Methods.md](../Questions/02-Integral-Equations-Volterra-Successive-Methods.md)

## 1. Classification
General linear form: $h(x)\thinspace y(x)=f(x)+\lambda\int_a^{b\text{ or }x}K(x,t)\thinspace y(t)\thinspace dt$.
| Name | Form |
|---|---|
| Fredholm, 1st kind | $f(x)=\lambda\int_a^b K(x,t)y(t)dt$ |
| Fredholm, 2nd kind | $y(x)=f(x)+\lambda\int_a^b K(x,t)y(t)dt$ |
| Volterra, 1st kind | $f(x)=\lambda\int_a^x K(x,t)y(t)dt$ |
| Volterra, 2nd kind | $y(x)=f(x)+\lambda\int_a^x K(x,t)y(t)dt$ |
| 3rd kind | $h(x)y=\dots$ with $h$ vanishing somewhere |
- **Homogeneous:** $f\equiv0$. **Singular:** infinite interval or kernel unbounded (e.g. Abel $K=(x-t)^{-\alpha}$).
- **Symmetric kernel:** $K(x,t)=K(t,x)$. **Convolution (difference) kernel:** $K=k(x-t)$.
- **Volterra = Fredholm with $K(x,t)=0$ for $t\gt x$.**
- An **integro-differential equation** contains $y'$ etc. as well.

## 2. ODE ↔ Integral equation
**Key formula (repeated integration):**
$$\int_a^x\negthinspace \negthinspace \int_a^{x_1}\negthinspace \negthinspace \cdots f\ dt\cdots=\int_a^x\frac{(x-t)^{n-1}}{(n-1)!}f(t)\thinspace dt$$
**IVP → Volterra.** For $y''+A(x)y'+B(x)y=g$, $y(a)=y_0$, $y'(a)=y_1$: put $u=y''$, then
$y'=y_1+\int_a^x u$, $y=y_0+y_1(x-a)+\int_a^x(x-t)u(t)dt$, and substitute.

Directly in $y$ (constant coefficients, e.g. $y''+\omega^2y=g$):
$$y(x)=y_0+y_1(x-a)+\int_a^x(x-t)\big[g(t)-\omega^2y(t)\big]dt.$$
Example: $y''+y=0,\ y(0)=1,\ y'(0)=0$ ⇔ $y=1-\int_0^x(x-t)y\thinspace dt$.

**BVP → Fredholm** via Green's function. For $y''+\lambda y=0$ (or $=-\lambda\thinspace \cdot$ source), $y(0)=y(1)=0$:
```math
y(x)=\lambda\int_0^1 G(x,t)y(t)dt,\qquad G(x,t)=\begin{cases}t(1-x),&0\le t\le x\cr  x(1-t),&x\le t\le1\end{cases}
```
On $[0,\ell]$: $G=\frac{t(\ell-x)}{\ell}$ ($t\le x$), $\frac{x(\ell-t)}{\ell}$ ($t\ge x$). Properties: continuous, symmetric, satisfies BCs, $\partial_xG$ jumps by $-1$ at $x=t$.

**IE → ODE:** differentiate using Leibniz:
$$\frac{d}{dx}\int_a^x K(x,t)y(t)dt=K(x,x)y(x)+\int_a^x K_x(x,t)y(t)dt$$
and read off initial conditions by putting $x=a$.

## 3. Volterra 1st kind → 2nd kind
If $K(x,x)\neq0$, differentiate $\int_a^x Ky\thinspace dt=f$:
$$y(x)=\frac{f'(x)}{K(x,x)}-\int_a^x\frac{K_x(x,t)}{K(x,x)}y(t)dt.$$
Need $f(a)=0$ for consistency. If $K(x,x)\equiv0$, differentiate again.

## 4. Successive approximations (Picard / Neumann)
$y_0=f$ (or any continuous guess), $y_{n}(x)=f(x)+\lambda\int K(x,t)y_{n-1}(t)dt$.

## 5. Successive substitutions, iterated & resolvent kernels
Substituting the equation into itself:
$$y=f+\sum_{n\ge1}\lambda^n\int K_n(x,t)f(t)dt\quad(\text{Neumann series}).$$
| | Fredholm | Volterra |
|---|---|---|
| $K_n(x,t)$ | $\int_a^b K(x,s)K_{n-1}(s,t)ds$ | $\int_t^x K(x,s)K_{n-1}(s,t)ds$ |
| Bound | $\lvert K_n\rvert\le M^n(b-a)^{n-1}$ | $\lvert K_n\rvert\le M^n\frac{(x-t)^{n-1}}{(n-1)!}$ |
| Convergence | $\lvert\lambda\rvert\lt \frac{1}{M(b-a)}$ (or $\lt 1/\lVert K\rVert_2$) | **all** $\lambda$ |
**Resolvent kernel** $R(x,t;\lambda)=\sum_{n\ge1}\lambda^{n-1}K_n(x,t)$; solution
$$y(x)=f(x)+\lambda\int R(x,t;\lambda)f(t)\thinspace dt.$$
$R$ satisfies $R(x,t;\lambda)=K(x,t)+\lambda\int K(x,s)R(s,t;\lambda)ds$.

**Volterra theorem:** $K$ continuous on $a\le t\le x\le b$, $f$ continuous ⇒ unique continuous solution for every $\lambda$; resolvent entire in $\lambda$; no characteristic values.

### Standard Volterra resolvents
| $K(x,t)$ | $K_n$ | $R(x,t;\lambda)$ |
|---|---|---|
| $1$ | $\frac{(x-t)^{n-1}}{(n-1)!}$ | $e^{\lambda(x-t)}$ |
| $e^{x-t}$ | $e^{x-t}\frac{(x-t)^{n-1}}{(n-1)!}$ | $e^{(1+\lambda)(x-t)}$ |
| $x-t$ | $\frac{(x-t)^{2n-1}}{(2n-1)!}$ | $\frac{\sinh\sqrt\lambda(x-t)}{\sqrt\lambda}$ ($\lambda=1$: $`\sinh(x-t)`$) |
| $a(x)/a(t)$-type $\frac{g(x)}{g(t)}$ | $\frac{g(x)}{g(t)}\frac{(x-t)^{n-1}}{(n-1)!}$ | $\frac{g(x)}{g(t)}e^{\lambda(x-t)}$ |

## 6. Convolution-type Volterra (use Laplace)
$y=f+\lambda\int_0^x k(x-t)y(t)dt$ ⇒ $Y=\dfrac{F}{1-\lambda K(s)}$.
First kind $\int_0^x k(x-t)y\thinspace dt=f$ ⇒ $Y=F/K$.
| Equation | Solution |
|---|---|
| $y=1+\int_0^x y$ | $e^x$ |
| $y=1-\int_0^x y$ | $e^{-x}$ |
| $y=1\mp\int_0^x(x-t)y$ | $\cos x$ / $\cosh x$ |
| $y=x-\int_0^x(x-t)y$ | $\sin x$ |
| $y=1+\int_0^x t\thinspace y$ | $e^{x^2/2}$ (not convolution; ODE $y'=xy$) |
| $\int_0^x e^{x-t}y=x$ | $1-x$ |

**Abel's equation** $\int_0^x\frac{y(t)}{(x-t)^{\alpha}}dt=f(x)$, $0\lt \alpha\lt 1$:
$$y(x)=\frac{\sin\alpha\pi}{\pi}\frac{d}{dx}\int_0^x\frac{f(t)}{(x-t)^{1-\alpha}}dt.$$
For $\alpha=\frac12$: $f=x$ ⇒ $y=\frac{2\sqrt x}{\pi}$; $f=1$ ⇒ $y=\frac{1}{\pi\sqrt x}$; $f=\sqrt x$ ⇒ $y=\frac12$.

## 7. Exam traps
- Volterra iterated kernels integrate from $t$ to $x$, Fredholm from $a$ to $b$.
- Volterra 2nd kind: **no** characteristic values; the Neumann series always converges. Fredholm: only for small $|\lambda|$.
- Volterra 1st kind may have no continuous solution (need $f(a)=0$, smoothness).
- IVP → Volterra; BVP → Fredholm (Green's function). Don't mix.
- In IVP conversion, don't forget the $y'(a)(x-a)$ term; kernel is $(x-t)$, not $(t-x)$.
- Green's function of $-y''$ is $+t(1-x)$ (nonnegative); of $y''$ it is the negative.
- Successive approximation $y_n$ ≠ partial sum with factorials of the exponential — compute it.
