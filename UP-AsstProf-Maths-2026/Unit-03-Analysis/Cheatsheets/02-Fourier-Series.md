# Cheatsheet · Unit 3 · Topic 02 — Fourier Series
> Questions: [../Questions/02-Fourier-Series.md](../Questions/02-Fourier-Series.md)

## 1. Euler (Fourier) coefficients
For $f$ integrable on $[-\pi,\pi]$ (period $2\pi$):
$$f(x)\sim\frac{a_0}{2}+\sum_{n=1}^\infty(a_n\cos nx+b_n\sin nx),\qquad a_n=\frac1\pi\int_{-\pi}^{\pi}f(x)\cos nx\,dx,\quad b_n=\frac1\pi\int_{-\pi}^{\pi}f(x)\sin nx\,dx.$$
- The constant term is $\frac{a_0}{2}=\frac1{2\pi}\int_{-\pi}^{\pi}f$, the **mean value** of $f$.
- **Orthogonality** ($m,n\ge1$): $\int_{-\pi}^{\pi}\cos mx\cos nx=\int\sin mx\sin nx=\pi\delta_{mn}$; $\int\sin mx\cos nx=0$; $\int_{-\pi}^{\pi}1\,dx=2\pi$.
- Any interval of length $2\pi$ works, e.g. $(0,2\pi)$: $a_n=\frac1\pi\int_0^{2\pi}f\cos nx$.
- **Period $2L$** on $(-L,L)$: replace $nx$ by $\frac{n\pi x}{L}$ and $\frac1\pi$ by $\frac1L$:
$a_n=\frac1L\int_{-L}^{L}f\cos\frac{n\pi x}{L}dx$, $b_n=\frac1L\int_{-L}^{L}f\sin\frac{n\pi x}{L}dx$.
- Complex form: $f\sim\sum c_ne^{inx}$, $c_n=\frac1{2\pi}\int f e^{-inx}$, $c_{\pm n}=\frac{a_n\mp ib_n}{2}$.

## 2. Even / odd and half-range series
| $f$ on $(-\pi,\pi)$ | Coefficients |
|---|---|
| even | $b_n=0$, $a_n=\frac2\pi\int_0^\pi f\cos nx$ (cosine series) |
| odd | $a_n=0$ (including $a_0$), $b_n=\frac2\pi\int_0^\pi f\sin nx$ (sine series) |
- **Half-range sine series** of $f$ on $(0,\pi)$ = Fourier series of its **odd** extension. **Half-range cosine series** = Fourier series of its **even** extension.
- On $(0,L)$: $b_n=\frac2L\int_0^Lf\sin\frac{n\pi x}{L}$ and $a_n=\frac2L\int_0^Lf\cos\frac{n\pi x}{L}$.

## 3. Convergence
- **Dirichlet conditions:** $f$ is $2\pi$-periodic, bounded, has finitely many maxima/minima and finitely many discontinuities in a period (or more simply: $f$ is piecewise smooth). Then the Fourier series converges at **every** $x$ to $\frac{f(x^+)+f(x^-)}{2}$.
- At the endpoints $\pm\pi$, use the **periodic extension**: the value is $\frac{f(-\pi^+)+f(\pi^-)}{2}$.
- **Riemann–Lebesgue lemma:** $f\in L^1$ ⇒ $a_n,b_n\to0$.
- **Fejér:** for continuous periodic $f$, the Cesàro means of the partial sums converge **uniformly** to $f$.
- A continuous $f$ can have a Fourier series that **diverges at a point** (du Bois-Reymond). Carleson: for $f\in L^2$ the series converges a.e.
- **Uniform convergence:** if $f$ is continuous, periodic ($f(-\pi)=f(\pi)$) and piecewise $C^1$, then $\sum(|a_n|+|b_n|)<\infty$ and the convergence is uniform. If the periodic extension has a jump, the convergence is **never** uniform near the jump.
- **Gibbs phenomenon:** near a jump the partial sums overshoot by about $9\%$ of the jump size, and this does not vanish as $n\to\infty$.
- **Term-by-term:** you may always integrate a Fourier series term by term (for integrable $f$). Differentiation needs more (continuity, periodicity, $f'$ piecewise smooth).

## 4. Bessel and Parseval
- **Bessel:** $\frac{a_0^2}{2}+\sum(a_n^2+b_n^2)\le\frac1\pi\int_{-\pi}^{\pi}f^2$.
- **Parseval** (equality for every $f\in L^2$, or Riemann square-integrable $f$): $\frac1\pi\int_{-\pi}^{\pi}f^2=\frac{a_0^2}{2}+\sum_{n\ge1}(a_n^2+b_n^2)$.
- Period $2L$: $\frac1L\int_{-L}^{L}f^2=\frac{a_0^2}{2}+\sum(a_n^2+b_n^2)$.

## 5. Standard expansions (on $(-\pi,\pi)$ unless stated)
| $f$ | Fourier series | Values it yields |
|---|---|---|
| $x$ | $2\sum\frac{(-1)^{n+1}}{n}\sin nx$ | $x=\frac\pi2$: $1-\frac13+\frac15-\cdots=\frac\pi4$; Parseval: $\sum\frac1{n^2}=\frac{\pi^2}{6}$ |
| $x^2$ | $\frac{\pi^2}3+4\sum\frac{(-1)^n}{n^2}\cos nx$ | $x=\pi$: $\sum\frac1{n^2}=\frac{\pi^2}6$; $x=0$: $\sum\frac{(-1)^{n+1}}{n^2}=\frac{\pi^2}{12}$; Parseval: $\sum\frac1{n^4}=\frac{\pi^4}{90}$ |
| $\lvert x\rvert$ | $\frac\pi2-\frac4\pi\sum_{n\text{ odd}}\frac{\cos nx}{n^2}$ | $x=0$: $\sum_{n\text{ odd}}\frac1{n^2}=\frac{\pi^2}8$; Parseval: $\sum_{\text{odd}}\frac1{n^4}=\frac{\pi^4}{96}$ |
| $\operatorname{sgn}x$ (square wave) | $\frac4\pi\sum_{n\text{ odd}}\frac{\sin nx}{n}$ | $x=\frac\pi2$: Leibniz $\frac\pi4$; Parseval: $\sum_{\text{odd}}\frac1{n^2}=\frac{\pi^2}8$ |
| $\lvert\sin x\rvert$ | $\frac2\pi-\frac4\pi\sum_{m\ge1}\frac{\cos2mx}{4m^2-1}$ | $x=0$: $\sum\frac1{4m^2-1}=\frac12$ |
| $\frac{\pi-x}{2}$ on $(0,2\pi)$ | $\sum_{n\ge1}\frac{\sin nx}{n}$ | |
| $e^{ax}$ | $\frac{2\sinh a\pi}{\pi}\left[\frac1{2a}+\sum\frac{(-1)^n}{a^2+n^2}(a\cos nx-n\sin nx)\right]$ | $\sum\frac{(-1)^n}{a^2+n^2}$ |
- The half-range series of $1$ on $(0,\pi)$ is the square-wave series, and the half-range cosine series of $x$ on $(0,\pi)$ is the $|x|$ series.
- $\zeta(2)=\frac{\pi^2}6$, $\zeta(4)=\frac{\pi^4}{90}$, $\sum_{\text{odd}}\frac1{n^2}=\frac{\pi^2}8$, $\sum\frac{(-1)^{n+1}}{n^2}=\frac{\pi^2}{12}$, $\sum_{\text{odd}}\frac1{n^4}=\frac{\pi^4}{96}$.

## 6. Exam traps
- Use $\frac{a_0}{2}$ (not $a_0$) in the series and in Parseval.
- The value at a jump is the **average**. For $f$ given on $(0,2\pi)$, the point $x=0$ is a jump between $f(0^+)$ and $f(2\pi^-)$.
- At $x=\pm\pi$ the series of $x$ gives $0$, not $\pm\pi$.
- An odd function has $a_0=0$ too. An even function can have $a_0\ne0$.
- Coefficients tending to $0$ (Riemann–Lebesgue) says nothing about uniform convergence.
- Fourier series of a continuous function need not converge everywhere. Absolutely summable coefficients give a continuous sum, **not** a differentiable one (Weierstrass function).
- For period $2L$, do not forget to change $\frac1\pi$ to $\frac1L$.
