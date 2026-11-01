# Cheatsheet · Unit 3 · Topic 04 — Functions of Bounded Variation
> Questions: [../Questions/04-Functions-of-Bounded-Variation.md](../Questions/04-Functions-of-Bounded-Variation.md)

## 1. Definitions
- For $P:a=x_0<\dots<x_n=b$, set $V(P,f)=\sum|f(x_i)-f(x_{i-1})|$. The **total variation** is $V_a^b(f)=\sup_PV(P,f)$. $f\in BV[a,b]\iff V_a^b(f)<\infty$.
- **Positive / negative variation:** $P_a^b=\sup_P\sum[f(x_i)-f(x_{i-1})]^+$ and $N_a^b=\sup_P\sum[f(x_i)-f(x_{i-1})]^-$. Then
$$V=P+N,\qquad f(b)-f(a)=P-N.$$
- **Additivity:** $V_a^b=V_a^c+V_c^b$ for $a<c<b$. Refining a partition never decreases $V(P,f)$.

## 2. Computing the variation
| Situation | Formula |
|---|---|
| $f$ monotone | $V=\lvert f(b)-f(a)\rvert$ |
| $f$ piecewise monotone with turning points $a=c_0<c_1<\dots<c_k=b$ | $V=\sum\lvert f(c_i)-f(c_{i-1})\rvert$ |
| $f\in C^1$ (or $f$ AC) | $V=\int_a^b\lvert f'(x)\rvert\,dx$ |
| jump at an interior point $c$ | contributes $\lvert f(c)-f(c^-)\rvert+\lvert f(c^+)-f(c)\rvert$ |
| isolated spike of height $h$ at an interior point | contributes $2h$; at an endpoint it contributes $h$ |
- Examples: $\sin x$ on $[0,2\pi]$ gives $4$; $x^3-3x$ on $[-2,2]$ gives $V=12$, $P=8$, $N=4$; $[x]$ on $[0,n]$ gives $n$.

## 3. Main theorems
- **BV ⇒ bounded:** $|f(x)|\le|f(a)|+V_a^b(f)$.
- **Jordan decomposition:** $f\in BV\iff f=g-h$ with $g,h$ increasing. Take $g=V_a^x$ and $h=V_a^x-f$, or $g=f(a)+P_a^x$ and $h=N_a^x$.
- $V(x)=V_a^x f$ is increasing, and $V$ is continuous at $c\iff f$ is continuous at $c$. So a **continuous** BV function is a difference of continuous increasing functions.
- **Discontinuities:** a BV function has only jump (first-kind) discontinuities, and at most **countably** many. Hence $f\in BV$ is Riemann integrable.
- **Lebesgue:** $f\in BV$ ⇒ $f'$ exists a.e. and $f'\in L^1$, with $\int_a^b|f'|\le V_a^b f$ (equality iff $f$ is AC).
- **Closure:** $BV$ is closed under $f\pm g$, $fg$, $cf$, and $f/g$ when $|g|\ge c>0$. With the norm $\|f\|=|f(a)|+V_a^b f$ it is a Banach algebra.
- **Not closed under composition:** $\sqrt t\circ x^2\sin^2(1/x)=|x\sin(1/x)|\notin BV$. It is closed under $\phi\circ f$ when $\phi$ is **Lipschitz**.
- Helly's selection theorem: a uniformly bounded sequence in BV with uniformly bounded variation has a pointwise convergent subsequence.
- For continuous $f$: the graph $\{(x,f(x))\}$ is a **rectifiable** curve $\iff f\in BV[a,b]$.

## 4. Inclusions (all strict)
$$C^1[a,b]\subsetneq\text{Lip}[a,b]\subsetneq AC[a,b]\subsetneq BV[a,b]\cap C[a,b]\subsetneq BV[a,b].$$
- Bounded derivative ⇒ Lipschitz ⇒ AC ⇒ BV. Monotone ⇒ BV.
- $C[a,b]\not\subset BV$ and $BV\not\subset C[a,b]$. Differentiable everywhere does **not** imply BV.

## 5. Standard examples (value $0$ at $x=0$, on $[0,1]$)
| Function | Status |
|---|---|
| $x\sin(1/x)$ | continuous, **not BV** |
| $x^2\sin(1/x)$ | differentiable, $f'$ bounded ⇒ Lipschitz ⇒ BV |
| $x^2\sin(1/x^2)$ | differentiable everywhere, **not BV** ($f'$ unbounded) |
| $x^\alpha\sin(x^{-\beta})$ | BV $\iff\alpha>\beta$ |
| $\sqrt x$ | monotone ⇒ BV; AC; not Lipschitz |
| Cantor function | continuous, increasing ⇒ BV; $f'=0$ a.e.; **not AC** |
| $\chi_{\mathbb Q}$ | not BV (every partition can pick up $\pm1$ jumps) |
| spikes $f(1/n)=h_n$, else $0$ | BV $\iff\sum h_n<\infty$; $V=h_1+2\sum_{n\ge2}h_n$ |
| step function with finitely many jumps | BV, discontinuous |

## 6. Exam traps
- Total variation is not the net change: for $\sin$ on $[0,2\pi]$, $V=4$, not $0$.
- Count both sides of an isolated value at a jump or spike, but only one side at an endpoint.
- "Continuous" and "differentiable everywhere" do **not** imply BV. "Bounded derivative" does.
- BV functions need not be continuous, but their discontinuities are countable jumps.
- The Cantor function is BV and continuous but **not** absolutely continuous, so FTC fails: $\int_0^1 f'=0\ne1=f(1)-f(0)$.
- For $x^\alpha\sin(1/x)$ the condition is the strict inequality $\alpha>1$; $\alpha=1$ is **not** BV.
- Composition of two BV functions can fail to be BV. You need the outer function to be Lipschitz.
