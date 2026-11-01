# Cheatsheet · Unit 3 · Topic 03 — Riemann Integral & Improper Integrals
> Questions: [../Questions/03-Riemann-Integral-Improper-Integrals.md](../Questions/03-Riemann-Integral-Improper-Integrals.md)

## 1. Definitions
- For a partition $P=\lbrace x_0\lt \dots\lt x_n\rbrace$ of $[a,b]$ and bounded $f$: $U(P,f)=\sum M_i\Delta x_i$ and $L(P,f)=\sum m_i\Delta x_i$.
- $f\in\mathcal R[a,b]\iff\inf_PU=\sup_PL$. Refining $P$ makes $L$ larger and $U$ smaller, and $L(P_1)\le U(P_2)$ for any two partitions.
- **Riemann's criterion:** $f\in\mathcal R\iff\forall\varepsilon\thinspace \exists P:\ U(P,f)-L(P,f)\lt \varepsilon$.
- **Riemann sums:** if $f\in\mathcal R$, then $\lim_{n\to\infty}\frac{b-a}{n}\sum_{k=1}^nf\negthinspace \left(a+k\frac{b-a}{n}\right)=\int_a^bf$.
- Riemann integrability **requires boundedness**: an unbounded function is never Riemann integrable (it needs an improper integral).

## 2. Which functions are integrable
- **Lebesgue's criterion:** a bounded $f$ is in $\mathcal R[a,b]\iff$ its set of discontinuities $D_f$ has measure $0$.
- Integrable: continuous functions; monotone functions (countably many jumps); bounded functions with finitely or countably many discontinuities; Thomae's function ($\int=0$); $\sin(1/x)$ with any value at $0$; $\chi_C$ for the Cantor set $C$ (uncountably many discontinuities, but $m(C)=0$).
- Not integrable: the Dirichlet function $\chi_{\mathbb{Q}}$ ($U=1$, $L=0$); $\chi_{\text{fat Cantor}}$ (discontinuous on a set of positive measure); any unbounded function.
- **Closure properties:** $\mathcal R[a,b]$ is closed under $+$, scalar multiples, products, $|f|$, $\max$/$`\min`$, $1/f$ when $|f|\ge c\gt 0$, and $\phi\circ f$ for continuous $\phi$.
- **Not closed:** $|f|\in\mathcal R\not\Rightarrow f\in\mathcal R$ ($f=\pm1$ on $\mathbb{Q}$/irrationals). $f\circ g$ with $f\in\mathcal R$ and $g$ continuous can fail. A pointwise limit of integrable functions can fail ($\chi_{\lbrace r_1,\dots,r_n\rbrace }\to\chi_{\mathbb Q}$).
- Changing $f$ at finitely many points changes neither integrability nor the value.

## 3. Properties and theorems
- $\left|\int f\right|\le\int|f|$; $m(b-a)\le\int_a^bf\le M(b-a)$.
- **First MVT:** for $f$ continuous, $\int_a^bf=f(c)(b-a)$. **Generalised:** for $g\ge0$ integrable, $\int fg=f(c)\int g$.
- **Second MVT (Bonnet):** for $g$ monotone, $\int_a^bfg=g(a)\int_a^\xi f+g(b)\int_\xi^bf$.
- **FTC-I:** for $f\in\mathcal R$, $F(x)=\int_a^xf$ is Lipschitz (hence continuous), and $F'(c)=f(c)$ at every point where $f$ is continuous.
- **FTC-II:** if $F'=f$ on $[a,b]$ and $f\in\mathcal R$, then $\int_a^bf=F(b)-F(a)$. The derivative $F'$ can be bounded but **not** integrable (Volterra), so the hypothesis $f\in\mathcal R$ is needed.
- **Leibniz rule:** $\dfrac{d}{dx}\int_{u(x)}^{v(x)}f(t)\thinspace dt=f(v)v'-f(u)u'$.
- An integral $=0$ with $f\ge0$ **continuous** forces $f\equiv0$. Without continuity, $f$ need only be $0$ at its points of continuity.

## 4. Improper integrals
**Type I** $\int_a^\infty f$ and **Type II** (unbounded near a point) are both defined as limits.

| Benchmark | Converges iff |
|---|---|
| $\int_1^\infty\frac{dx}{x^p}$ | $p\gt 1$ |
| $\int_0^1\frac{dx}{x^p}$ | $p\lt 1$ |
| $\int_0^\infty\frac{dx}{x^p}$ | never |
| $\int_2^\infty\frac{dx}{x(\log x)^p}$ | $p\gt 1$ |
| $\int_0^\infty x^{p-1}e^{-x}dx$ | $p\gt 0$ (this is $`\Gamma(p)`$) |
| $\int_0^1x^{p-1}(1-x)^{q-1}dx$ | $p,q\gt 0$ (this is $`B(p,q)`$) |
| $\int_0^\infty\frac{x^{p-1}}{1+x}dx$ | $0\lt p\lt 1$, value $\frac{\pi}{\sin p\pi}$ |
| $\int_0^\infty\frac{\sin x}{x^p}dx$ | $0\lt p\lt 2$ (absolutely only for $1\lt p\lt 2$) |
| $\int_0^1\log x\thinspace dx$ | converges ($=-1$) |
- **Tests:** comparison; limit comparison ($`f/g\to c\in(0,\infty)`$); the **$\mu$-test** ($x^\mu f(x)\to$ finite with $\mu\gt 1$ at $\infty$, or $\mu\lt 1$ at $0$ ⇒ converges); absolute convergence ⇒ convergence.
- **Dirichlet test:** $\int_a^xf$ bounded and $g\downarrow0$ ⇒ $\int fg$ converges ($\int\frac{\sin x}{x}$). **Abel test:** $\int f$ converges and $g$ monotone bounded ⇒ $\int fg$ converges.
- $\int_0^\infty\frac{\sin x}{x}dx=\frac\pi2$, but this is **conditional**: $\int\left|\frac{\sin x}{x}\right|=\infty$.
- Fresnel: $\int_0^\infty\sin x^2\thinspace dx=\int_0^\infty\cos x^2\thinspace dx=\frac12\sqrt{\frac\pi2}$. These converge although the integrands do **not** tend to $0$.
- **Cauchy principal value:** $PV\int_{-1}^1\frac{dx}{x}=0$, but the improper integral diverges.
- Frullani: $\int_0^\infty\frac{f(ax)-f(bx)}{x}dx=(f(0)-f(\infty))\log\frac ba$; e.g. $\int_0^\infty\frac{e^{-ax}-e^{-bx}}{x}=\log\frac ba$.

## 5. Beta and Gamma
- $\Gamma(p)=\int_0^\infty x^{p-1}e^{-x}dx$, $\Gamma(p+1)=p\Gamma(p)$, $\Gamma(n+1)=n!$, $\Gamma(\frac12)=\sqrt\pi$, $\Gamma(\frac32)=\frac{\sqrt\pi}{2}$, $\Gamma(\frac52)=\frac{3\sqrt\pi}{4}$.
- $B(p,q)=\int_0^1x^{p-1}(1-x)^{q-1}dx=\dfrac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}=2\int_0^{\pi/2}\sin^{2p-1}\theta\cos^{2q-1}\theta\thinspace d\theta=\int_0^\infty\frac{x^{p-1}}{(1+x)^{p+q}}dx$.
- **Reflection:** $\Gamma(p)\Gamma(1-p)=\dfrac{\pi}{\sin p\pi}$ for $0\lt p\lt 1$. **Duplication:** $\Gamma(p)\Gamma(p+\frac12)=2^{1-2p}\sqrt\pi\thinspace \Gamma(2p)$.
- $\int_0^\infty e^{-ax^2}dx=\frac12\sqrt{\frac\pi a}$; $\int_0^\infty x^{n}e^{-x^2}dx=\frac12\Gamma\left(\frac{n+1}2\right)$; $\int_0^\infty x^{m}e^{-ax}dx=\frac{m!}{a^{m+1}}$.
- **Wallis:** $\int_0^{\pi/2}\sin^nx\thinspace dx=\frac{n-1}{n}\cdot\frac{n-3}{n-2}\cdots$ (times $\frac\pi2$ if $n$ is even, times $1$ if $n$ is odd).
- $\int_0^{\pi/2}\sin^m\theta\cos^n\theta\thinspace d\theta=\frac12B\negthinspace \left(\frac{m+1}2,\frac{n+1}2\right)$.

## 6. Exam traps
- "Countably many discontinuities" is **sufficient**, but "discontinuities form a null set" is the exact criterion. A dense discontinuity set is fine (Thomae).
- $|f|$ integrable does not imply $f$ integrable.
- $F(x)=\int_a^xf$ is always continuous, but differentiable with $F'=f$ only where $f$ is continuous.
- Check **both** ends of an improper integral (e.g. $\int_0^\infty\frac{x^{p-1}}{1+x}$ and $\int_0^\infty\frac{\sin x}{x^p}$).
- An integrand that does not tend to $0$ can still have a convergent improper integral (Fresnel). Unlike series, there is no "$`n`$th term test".
- Convergence of $\int_{-\infty}^\infty f$ needs **both** tails separately; $\lim_{R\to\infty}\int_{-R}^R$ is only the principal value.
- In Beta-function questions match the exponents carefully: $x^{4}(1-x)^{3}$ is $B(5,4)$, not $B(4,3)$.
