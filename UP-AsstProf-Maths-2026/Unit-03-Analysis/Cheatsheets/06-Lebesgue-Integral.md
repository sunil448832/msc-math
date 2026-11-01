# Cheatsheet · Unit 3 · Topic 06 — Lebesgue Integral
> Questions: [../Questions/06-Lebesgue-Integral.md](../Questions/06-Lebesgue-Integral.md)

## 1. Construction (in 4 steps)
1. **Simple** $s=\sum_{i=1}^k a_i\chi_{E_i}$ ($a_i\ge0$, $E_i$ measurable): $\int s=\sum a_i\, m(E_i)$ (with $0\cdot\infty=0$).
2. **Non-negative measurable** $f$: $\int f=\sup\{\int s: 0\le s\le f,\ s \text{ simple}\}\in[0,\infty]$.
3. **General** $f=f^+-f^-$: $f$ is **integrable** ($f\in L^1$) iff $\int|f|<\infty$, and then $\int f=\int f^+-\int f^-$.
4. The Lebesgue integral is **absolute**: $f\in L^1\iff|f|\in L^1$.

Basic facts:
- $f=g$ a.e. $\Rightarrow\int f=\int g$.
- $f\ge0$ and $\int f=0\Rightarrow f=0$ a.e.
- $\int_E f=0$ whenever $m(E)=0$.
- $f\in L^1\Rightarrow |f|<\infty$ a.e.
- Chebyshev: $m\{|f|\ge\alpha\}\le\frac1\alpha\int|f|$.
- Absolute continuity: for every $\varepsilon>0$ there is $\delta>0$ with $m(E)<\delta\Rightarrow\int_E|f|<\varepsilon$.

## 2. The three convergence theorems
| Theorem | Hypotheses | Conclusion |
|---|---|---|
| **MCT** (Beppo Levi) | $f_n$ measurable, $0\le f_1\le f_2\le\cdots$, $f_n\to f$ | $\int f_n\uparrow\int f$ (may be $\infty$) |
| **Fatou** | $f_n\ge0$ measurable | $\int\liminf f_n\le\liminf\int f_n$ |
| **DCT** (Lebesgue) | $f_n\to f$ a.e., $|f_n|\le g$ a.e., $g\in L^1$ | $f\in L^1$ and $\int|f_n-f|\to0$, so $\int f_n\to\int f$ |
| **BCT** (bounded convergence) | $m(E)<\infty$, $|f_n|\le M$, $f_n\to f$ a.e. on $E$ | $\int_E f_n\to\int_E f$ |

- **Series form of MCT:** for $g_n\ge0$, $\int\sum g_n=\sum\int g_n$.
- **Series form of DCT:** if $\sum\int|g_n|<\infty$, then $\sum g_n$ converges a.e. and $\int\sum g_n=\sum\int g_n$.
- Uniform convergence on a set of **finite** measure gives $\int f_n\to\int f$. On a set of infinite measure it does not (see $\frac1n\chi_{[0,n]}$).

## 3. Standard counterexamples ($f_n\to0$ pointwise but $\int f_n\not\to0$)
| $f_n$ | $\int f_n$ | What goes wrong |
|---|---|---|
| $n\chi_{(0,1/n)}$ | $1$ | spike; no integrable dominant (Fatou strict) |
| $\chi_{[n,n+1]}$ | $1$ | mass escapes to $\infty$ |
| $\frac1n\chi_{[0,n]}$ | $1$ | uniform convergence but infinite measure |
| $nx^{n-1}$ on $[0,1]$ | $1$ | concentration at $x=1$ |
| typewriter $\chi_{[j/2^k,(j+1)/2^k]}$ | $2^{-k}\to0$ | $L^1$-convergent but convergent at **no** point |

## 4. Riemann vs Lebesgue
- **Lebesgue's criterion:** a bounded $f$ on $[a,b]$ is Riemann integrable iff $m(\{\text{discontinuities}\})=0$.
- Bounded and Riemann integrable $\Rightarrow$ Lebesgue integrable, with the same value. The converse fails: $\chi_{\mathbb Q}$ on $[0,1]$ has $\int=0$ but is not Riemann integrable.
- An **improper** Riemann integral may converge without the function being in $L^1$: $\int_0^\infty\frac{\sin x}{x}dx=\frac\pi2$, but $\int_0^\infty\frac{|\sin x|}{x}=\infty$.
- If $f\ge0$, the improper Riemann integral and the Lebesgue integral agree (via MCT).
- Thomae's function: Riemann integrable (discontinuous only on $\mathbb Q$), integral $0$.

## 5. $L^p$ basics
- $\|f\|_p=\left(\int|f|^p\right)^{1/p}$ for $1\le p<\infty$, and $\|f\|_\infty=\operatorname{ess\,sup}|f|$. Elements are classes of functions equal a.e.
- **Hölder:** $\|fg\|_1\le\|f\|_p\|g\|_q$ for $\frac1p+\frac1q=1$. **Minkowski:** $\|f+g\|_p\le\|f\|_p+\|g\|_p$ for $p\ge1$.
- **Riesz–Fischer:** $L^p$ is a Banach space for $1\le p\le\infty$. $L^2$ is a **Hilbert** space, and it is the only $L^p$ that is one.
- If $f_n\to f$ in $L^p$, a **subsequence** converges a.e.
- **Inclusions:**
  - finite measure ($[0,1]$): $p<q\Rightarrow L^q\subseteq L^p$, $\|f\|_p\le\|f\|_q$; also $L^\infty\subseteq L^p$.
  - sequence spaces: $p<q\Rightarrow\ell^p\subseteq\ell^q$ (the reverse direction).
  - on $\mathbb R$: no inclusion.
- **Power test** on $(0,1)$: $x^{-a}\in L^p\iff ap<1$. On $(1,\infty)$: $x^{-a}\in L^p\iff ap>1$.
- **Density:** continuous functions with compact support, step functions and simple functions are dense in $L^p$ for $1\le p<\infty$. This fails for $L^\infty$.
- **Separable:** $L^p$ for $1\le p<\infty$. Not separable: $L^\infty$.
- **Duals:** $(L^p)^*=L^q$ for $1\le p<\infty$; $L^p$ is reflexive for $1<p<\infty$.

## 6. Quick evaluation tricks
- $\lim\int_0^n(1-x/n)^n dx=\int_0^\infty e^{-x}=1$ (MCT).
- $\lim\int_0^\infty\frac{n\sin(x/n)}{x(1+x^2)}=\frac\pi2$ (DCT, using $|\sin u|\le|u|$).
- $\int_0^1\frac{nx^{n-1}}{1+x}\to\frac12$: in general $\int_0^1 nx^{n-1}g(x)\,dx\to g(1)$ for continuous $g$.
- Cauchy–Schwarz on $[0,1]$: $\left(\int f\right)^2\le\int f^2$.

## Exam traps
- MCT needs **monotone and non-negative**. DCT needs an **integrable dominating function**, not just a bounded one, unless the measure is finite (BCT).
- Fatou fails without $f_n\ge0$ (or a common integrable lower bound).
- "Riemann integrable on $[a,b]$ $\Rightarrow$ Lebesgue integrable" is for **proper** (bounded) integrals only. An improper integral may be conditionally convergent.
- $L^1$ convergence does **not** imply a.e. convergence, and a.e. convergence does **not** imply $L^1$ convergence.
- The $L^p$ inclusion goes opposite ways on $[0,1]$ and on $\ell^p$.
- $\|\cdot\|_p$ for $0<p<1$ is **not** a norm (the triangle inequality fails).
