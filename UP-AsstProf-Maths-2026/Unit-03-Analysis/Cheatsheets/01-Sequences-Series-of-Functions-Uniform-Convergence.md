# Cheatsheet · Unit 3 · Topic 01 — Sequences & Series of Functions, Uniform Convergence
> Questions: [../Questions/01-Sequences-Series-of-Functions-Uniform-Convergence.md](../Questions/01-Sequences-Series-of-Functions-Uniform-Convergence.md)

## 1. Real sequences — essentials
- **limsup / liminf:** $\limsup a_n=\inf_n\sup_{k\ge n}a_k$ = largest subsequential limit; $\liminf$ = smallest. $(a_n)$ converges $\iff \limsup=\liminf$ (finite).
- $\limsup(a_n+b_n)\le\limsup a_n+\limsup b_n$ (inequality can be strict). $\liminf(-a_n)=-\limsup a_n$.
- **Bolzano–Weierstrass:** every bounded sequence in $\mathbb{R}^n$ has a convergent subsequence.
- **Monotone convergence:** a monotone sequence converges $\iff$ it is bounded.
- **Cauchy:** in $\mathbb{R}$, Cauchy $\iff$ convergent (completeness). Fails in $\mathbb{Q}$.
- Standard limits: $n^{1/n}\to1$, $(1+1/n)^n\to e$, $(n!)^{1/n}/n\to 1/e$, $\frac{a_{n+1}}{a_n}\to L\Rightarrow a_n^{1/n}\to L$ (the converse fails).
- **Cesàro:** $a_n\to L\Rightarrow \frac{a_1+\dots+a_n}{n}\to L$. **Stolz–Cesàro:** $\frac{a_{n+1}-a_n}{b_{n+1}-b_n}\to L$, $b_n\uparrow\infty$ $\Rightarrow \frac{a_n}{b_n}\to L$.

## 2. Series of reals — tests
| Test | Statement |
|---|---|
| $n$th term | $\sum a_n$ converges $\Rightarrow a_n\to0$ (not conversely: $\sum 1/n$) |
| $p$-series | $\sum 1/n^p$ converges $\iff p>1$; $\sum \frac{1}{n(\log n)^p}$ converges $\iff p>1$ |
| Comparison / limit comparison | $a_n,b_n>0$, $a_n/b_n\to c\in(0,\infty)$ ⇒ same behaviour |
| Ratio (d'Alembert) | $\limsup\frac{a_{n+1}}{a_n}<1$ conv.; $\liminf>1$ div.; $=1$ inconclusive |
| Root (Cauchy) | $\limsup a_n^{1/n}<1$ conv.; $>1$ div. (stronger than ratio) |
| Cauchy condensation | $a_n\downarrow0$: $\sum a_n$ and $\sum 2^ka_{2^k}$ converge together |
| Integral | $f\ge0$ decreasing: $\sum f(n)$ and $\int_1^\infty f$ converge together |
| Raabe | $n\left(\frac{a_n}{a_{n+1}}-1\right)\to L$: $L>1$ conv., $L<1$ div. |
| Leibniz | $a_n\downarrow0\Rightarrow\sum(-1)^na_n$ converges; error $\le a_{n+1}$ |
| Dirichlet / Abel | $\sum a_n$ has bounded partial sums and $b_n\downarrow0$ ⇒ $\sum a_nb_n$ conv.; $\sum a_n$ conv. and $b_n$ monotone bounded ⇒ conv. |
- Absolute convergence ⇒ convergence. **Riemann rearrangement:** a conditionally convergent series can be rearranged to any sum in $[-\infty,\infty]$. An absolutely convergent series has the same sum under every rearrangement.

## 3. Pointwise vs uniform convergence
- $f_n\to f$ **uniformly** on $E$ $\iff M_n:=\sup_{E}|f_n-f|\to0$.
- **Cauchy criterion:** uniform $\iff \forall\varepsilon\,\exists N:\ |f_n(x)-f_m(x)|<\varepsilon$ for all $m,n\ge N$ and all $x\in E$.
- **Recipe:** find the pointwise limit $f$ → maximize $|f_n-f|$ (calculus) → check whether that max tends to $0$. Or show non-uniformity by finding $x_n$ with $|f_n(x_n)-f(x_n)|\not\to0$.

| $f_n$ on $[0,1]$ | pointwise limit | $\sup|f_n-f|$ | uniform? |
|---|---|---|---|
| $x^n$ | $0$ ($x<1$), $1$ ($x=1$) | $1$ | No (on $[0,a]$, $a<1$: yes) |
| $\frac{nx}{1+n^2x^2}$ | $0$ | $1/2$ at $x=1/n$ | No |
| $\frac{x}{1+nx^2}$ | $0$ | $\frac1{2\sqrt n}$ | Yes |
| $nx(1-x)^n$, $nx^n(1-x)$ | $0$ | $\to 1/e$ | No |
| $x^n(1-x)$ | $0$ | $\sim\frac1{en}$ | Yes |
| $n^2xe^{-nx}$ | $0$ | $n/e$ | No; $\int_0^1\to1\ne0$ |
| $\frac{\sin nx}{\sqrt n}$ on $\mathbb{R}$ | $0$ | $1/\sqrt n$ | Yes, but $f_n'=\sqrt n\cos nx$ diverges |

## 4. What uniform convergence preserves
| Property | Theorem (exact hypotheses) |
|---|---|
| Continuity | $f_n$ continuous, $f_n\to f$ uniformly on $E$ ⇒ $f$ continuous. (Contrapositive: a discontinuous limit means the convergence is not uniform.) |
| Integration | $f_n\in\mathcal R[a,b]$, $f_n\to f$ uniformly ⇒ $f\in\mathcal R[a,b]$ and $\int f_n\to\int f$ (needs a **bounded** interval) |
| Differentiation | $f_n$ differentiable on $[a,b]$, $(f_n(x_0))$ converges for some $x_0$, $f_n'$ converges **uniformly** ⇒ $f_n\to f$ uniformly and $f'=\lim f_n'$ |
| Boundedness | each $f_n$ bounded + uniform ⇒ $f$ bounded and the family is uniformly bounded |
- A uniform limit of differentiable functions need not be differentiable: $\sqrt{x^2+1/n}\to|x|$.
- **Weierstrass approximation:** every continuous $f$ on $[a,b]$ is a uniform limit of polynomials.

## 5. Series of functions
- **Weierstrass M-test:** $|u_n(x)|\le M_n$ on $E$ and $\sum M_n<\infty$ ⇒ $\sum u_n$ converges uniformly and absolutely on $E$. E.g. $\sum\frac{\sin nx}{n^p}$, $p>1$, on $\mathbb{R}$.
- **Dirichlet/Abel tests (uniform versions):** e.g. $\sum\frac{\sin nx}{n}$ converges uniformly on $[\delta,2\pi-\delta]$ but **not** on $[0,2\pi]$.
- **Dini's theorem:** $K$ **compact**, $f_n\in C(K)$, $f_n(x)$ **monotone** in $n$ for each $x$, and the limit $f$ **continuous** ⇒ uniform convergence. Each hypothesis is needed: $x^n$ on $[0,1)$ (non-compact); $x^n$ on $[0,1]$ (discontinuous limit); $\frac{nx}{1+n^2x^2}$ (not monotone).
- Example: $\sum_{n\ge0}\frac{x^2}{(1+x^2)^n}=1+x^2$ ($x\ne0$), $=0$ at $x=0$. The sum is discontinuous, so the convergence is not uniform near $0$.

## 6. Power series $\sum a_n(x-c)^n$
- **Cauchy–Hadamard:** $\dfrac1R=\limsup|a_n|^{1/n}$. If $\left|\frac{a_{n+1}}{a_n}\right|\to L$, then $R=1/L$.
- Converges absolutely for $|x-c|<R$, diverges for $|x-c|>R$, and converges **uniformly on every $[c-r,c+r]$ with $r<R$**. At the endpoints anything can happen; check them separately.
- **Abel's theorem:** if the series converges at $x=R$, it converges uniformly on $[0,R]$ and the sum is left-continuous at $R$. (Used to get $\log2=1-\frac12+\frac13-\cdots$ and $\frac\pi4=1-\frac13+\cdots$.)
- Term-by-term differentiation and integration keep the same $R$, but endpoint behaviour may change.
- Standard radii: $\sum\frac{n!}{n^n}z^n$: $R=e$; $\sum n!z^n$: $R=0$; $\sum\frac{z^n}{n!}$: $R=\infty$; $\sum z^{n!}$, $\sum z^{2^n}$: $R=1$ (lacunary); $\sum a_nz^n$ with $a_n\in\{2^n,3^n\}$ alternately: $R=1/3$; $\sum n^kz^n$: $R=1$.
- Radius of $\sum a_nz^{2n}$ is $\sqrt{R}$, where $R$ is the radius of $\sum a_nz^n$.

## 7. Exam traps
- Pointwise convergence to a continuous limit does **not** imply uniform convergence ($\frac{nx}{1+n^2x^2}$).
- $\lim\int f_n\ne\int\lim f_n$ in general ($n^2xe^{-nx}$, $nx(1-x^2)^n$). Check uniform convergence, or use the dominated convergence theorem (Lebesgue integral topic).
- Ratio-test limit $=1$ tells you nothing; the root test is stronger (it works whenever the ratio test does).
- The radius of convergence uses **limsup**, not lim; with mixed subsequences take the **max** growth rate.
- Uniform convergence on each $[a,b]\subset(0,1)$ does **not** mean uniform convergence on $(0,1)$.
- $\sum u_n$ uniformly convergent ⇒ $u_n\to0$ uniformly (a quick test for non-uniformity).
- Endpoints of the interval of convergence: $\sum\frac{x^n}{n}$ gives $[-1,1)$; $\sum\frac{x^n}{n^2}$ gives $[-1,1]$; $\sum x^n$ gives $(-1,1)$.
