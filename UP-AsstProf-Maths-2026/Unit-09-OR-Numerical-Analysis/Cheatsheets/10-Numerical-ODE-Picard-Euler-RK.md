# Cheatsheet · Unit 9 · Topic 10 — Numerical ODE: Picard, Euler, Modified Euler, Runge–Kutta
> Questions: [../Questions/10-Numerical-ODE-Picard-Euler-RK.md](../Questions/10-Numerical-ODE-Picard-Euler-RK.md)

IVP: $y'=f(x,y)$, $y(x_0)=y_0$, step $h$, $x_n=x_0+nh$.

## 1. Picard's method of successive approximations
$$y_{n+1}(x)=y_0+\int_{x_0}^{x}f\big(t,y_n(t)\big)\thinspace dt,\qquad y_0(x)\equiv y_0.$$
- **Picard–Lindelöf theorem:** let $f$ be continuous on $R=\lbrace |x-x_0|\le a,\ |y-y_0|\le b\rbrace$ with $|f|\le M$, and **Lipschitz in $y$** with constant $L$. Then the iterates converge uniformly to the unique solution on $|x-x_0|\le\min(a,b/M)$.
- Error bound: $|y-y_n|\le \dfrac{M L^n|x-x_0|^{n+1}}{(n+1)!}$.
- It gives an analytic approximation (a function), not a table. It is impractical when $\int f$ is hard.
- Examples:
  - $y'=y$, $y(0)=1$: $y_n=\sum_{k=0}^n x^k/k!$.
  - $y'=x+y$, $y(0)=1$: $y_1=1+x+\frac{x^2}{2}$, $y_2=1+x+x^2+\frac{x^3}{6}$. The exact solution is $2e^x-x-1$.
  - $y'=x^2+y^2$, $y(0)=0$: $y_1=\frac{x^3}{3}$, $y_2=\frac{x^3}{3}+\frac{x^7}{63}$.

## 2. Taylor-series method
$y_{n+1}=y_n+hy_n'+\frac{h^2}{2}y_n''+\dots$ It needs the total derivatives $y''=f_x+ff_y$ and so on. RK methods are designed to avoid computing these.

## 3. Euler-type methods
| Method | Formula | Local error | Global order |
|---|---|---|---|
| Euler (explicit) | $y_{n+1}=y_n+hf(x_n,y_n)$ | $\frac{h^2}{2}y''(\xi)$ | 1 |
| Backward Euler (implicit) | $y_{n+1}=y_n+hf(x_{n+1},y_{n+1})$ | $O(h^2)$ | 1 |
| Modified Euler / Heun (predictor–corrector) | $y^\ast =y_n+hf_n$, then $y_{n+1}=y_n+\frac h2[f_n+f(x_{n+1},y^\ast )]$ | $O(h^3)$ | 2 |
| Midpoint / improved polygon | $y_{n+1}=y_n+hf\big(x_n+\frac h2,\ y_n+\frac h2f_n\big)$ | $O(h^3)$ | 2 |

Indian textbooks (e.g. Sastry) usually mean Heun's method by "modified Euler". It is often iterated: the corrector is applied repeatedly until two successive values agree. Some texts use the name for the midpoint method instead.

## 4. Runge–Kutta methods
**RK2 family:** $k_1=hf(x_n,y_n)$, $k_2=hf(x_n+ah,\ y_n+ak_1)$, $y_{n+1}=y_n+(1-\frac{1}{2a})k_1+\frac1{2a}k_2$. Here $a=1$ gives Heun and $a=\frac12$ gives the midpoint method.

**Classical RK4:**
```math
\begin{aligned}k_1&=hf(x_n,y_n), & k_2&=hf\negthinspace \left(x_n+\tfrac h2,\thinspace y_n+\tfrac{k_1}2\right),\cr  k_3&=hf\negthinspace \left(x_n+\tfrac h2,\thinspace y_n+\tfrac{k_2}2\right), & k_4&=hf(x_n+h,\thinspace y_n+k_3),\end{aligned}
```
$$y_{n+1}=y_n+\tfrac16(k_1+2k_2+2k_3+k_4).$$
- Local error $O(h^5)$ and global error $O(h^4)$. It uses 4 $f$-evaluations and no derivatives of $f$. It is self-starting and lets you change $h$ easily.
- If $f=f(x)$, RK4 becomes **Simpson's rule** and Heun becomes the **trapezoidal rule**.
- For $y'=y$ with $h=1$, RK4 gives $65/24$, the Taylor polynomial of $e$ of degree 4.
- **Butcher barriers** (stages needed for order $p$): orders 1 to 4 need $p$ stages, order 5 needs 6 stages, order 6 needs 7 stages.
- A global order $p$ means halving $h$ divides the error by $2^p$ (16 for RK4).

## 5. Errors
- **Local truncation error** is the error made in one step from exact data. **Global error** is the accumulated error at a fixed $x$.
- In general, a local error of $O(h^{p+1})$ gives a global error of $O(h^p)$, and the method is said to have **order $p$**.
- **Consistency + zero-stability ⇒ convergence** (Dahlquist). All one-step RK methods are zero-stable.

## 6. Absolute stability (test equation $y'=\lambda y$, $z=h\lambda$)
| Method | $R(z)$ | Real stability interval | A-stable? |
|---|---|---|---|
| Euler | $1+z$ | $[-2,0]$ (disc $\lvert1+z\rvert\le1$) | No |
| Backward Euler | $\dfrac1{1-z}$ | $(-\infty,0]$ (all of it) | **Yes** |
| Trapezoidal (implicit) | $\dfrac{1+z/2}{1-z/2}$ | $(-\infty,0]$ | **Yes** |
| Heun / RK2 | $1+z+\frac{z^2}2$ | $[-2,0]$ | No |
| RK4 | $\sum_{k=0}^4 z^k/k!$ | $\approx[-2.785,0]$ | No |
- The method is stable iff $|R(h\lambda)|\le1$. For $\lambda\lt 0$ real: Euler and RK2 need $h\le 2/|\lambda|$, and RK4 needs $h\le2.785/|\lambda|$.
- **No explicit RK method is A-stable**, because $R$ is a polynomial and $|R(z)|\to\infty$. Stiff problems call for implicit methods.
- Example: $y'=-10y$ with $h=0.25$ under Euler gives $y_n=(-1.5)^n$, which grows and oscillates.

## 7. Comparison
| | Picard | Euler | Modified Euler | RK4 | Taylor |
|---|---|---|---|---|---|
| Output | function | table | table | table | table |
| Order | (analytic) | 1 | 2 | 4 | as chosen |
| Needs $f_x,f_y$? | integrals | no | no | no | **yes** |

## Exam traps
- **Local and global order differ by one**: Euler has local error $O(h^2)$ and global order 1, RK4 has local error $O(h^5)$ and global order 4.
- RK methods need **no derivatives** of $f$. Taylor-series methods do.
- Euler and Heun have the **same** real stability interval $[-2,0]$, although their regions in $\mathbb C$ differ.
- Explicit Euler is not A-stable, but backward Euler is.
- The second Picard iterate of $y'=x+y$ is not the $e^x$ partial sum, because the $x$ term contributes.
- RK4 on $y'=f(x)$ is Simpson's rule, not the 3/8 rule. The 3/8 rule corresponds to Kutta's 3/8 variant of RK4.
