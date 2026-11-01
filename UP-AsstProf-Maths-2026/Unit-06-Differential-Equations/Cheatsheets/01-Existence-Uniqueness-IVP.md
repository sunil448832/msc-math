# Cheatsheet · Unit 6 · Topic 01 — Existence and Uniqueness of IVPs
> Questions: [../Questions/01-Existence-Uniqueness-IVP.md](../Questions/01-Existence-Uniqueness-IVP.md)

## 1. Set-up
IVP: $y'=f(x,y)$, $y(x_0)=y_0$. This is equivalent (for continuous $f$) to the **integral equation**
$$y(x)=y_0+\int_{x_0}^{x} f(t,y(t))\,dt .$$

## 2. Lipschitz condition
$f$ is **Lipschitz in $y$** on $D$ if there is an $L$ with $|f(x,y_1)-f(x,y_2)|\le L|y_1-y_2|$ for all $(x,y_1),(x,y_2)\in D$.

- **Sufficient test:** if $\partial f/\partial y$ exists and $|\partial f/\partial y|\le K$ on a domain that is convex in $y$, then $f$ is Lipschitz with $L=K$ (by the MVT).
- Lipschitz does **not** require differentiability: $|y|$ is Lipschitz with $L=1$.
- **Not Lipschitz near $y=0$:** $y^{1/3}$, $y^{2/3}$, $\sqrt{|y|}$, $y\ln|y|$.
- On a **bounded** rectangle, $y^2$ is Lipschitz. On $\mathbb{R}^2$ it is only *locally* Lipschitz.
- Lipschitz in $y$ implies continuity in $y$ (the converse is false).

## 3. Main theorems
| Theorem | Hypothesis | Conclusion |
|---|---|---|
| **Peano** | $f$ continuous on $R$ | **existence** on $\lvert x-x_0\rvert\le h$ (possibly non-unique) |
| **Picard–Lindelöf** | $f$ continuous on $R$ and Lipschitz in $y$ | **unique** solution on $\lvert x-x_0\rvert\le h$ |
| **Global (linear growth / global Lipschitz)** | $f$ continuous on $[a,b]\times\mathbb{R}$, Lipschitz in $y$ there | unique solution on all of $[a,b]$ |
| **Linear ODE** $y'+p(x)y=q(x)$ | $p,q$ continuous on $I$ | unique solution on **all of $I$** |
| **Osgood** | $\lvert f(x,y_1)-f(x,y_2)\rvert\le\omega(\lvert y_1-y_2\rvert)$ with $\int_0\frac{du}{\omega(u)}=\infty$ | uniqueness |

Here $R=\{|x-x_0|\le a,\ |y-y_0|\le b\}$, $M=\max_R|f|$ and
$$\boxed{h=\min\Big(a,\ \frac{b}{M}\Big)}$$
- Lipschitz is **sufficient, not necessary** for uniqueness.
- Continuity alone gives existence but **not uniqueness**.

## 4. Picard iterates
$$y_0(x)\equiv y_0,\qquad y_{n+1}(x)=y_0+\int_{x_0}^x f(t,y_n(t))\,dt.$$
- They converge uniformly on $|x-x_0|\le h$, with error $|y-y_n|\le \dfrac{M L^n h^{n+1}}{(n+1)!}$.
- $y'=y$, $y(0)=1$ gives $y_n=\sum_{k=0}^n x^k/k!$.
- $y'=x+y$, $y(0)=1$ gives $y_1=1+x+\frac{x^2}{2}$ and $y_2=1+x+x^2+\frac{x^3}{6}$. The exact solution is $2e^x-x-1$.
- $y'=2x(1+y)$, $y(0)=0$ gives $y_n=x^2+\frac{x^4}{2!}+\dots+\frac{x^{2n}}{n!}$, with exact solution $e^{x^2}-1$.

## 5. Standard non-uniqueness examples
| IVP | Solutions |
|---|---|
| $y'=y^{1/3},\ y(0)=0$ | $y=0$ and $y=\pm\big(\tfrac{2}{3}(x-c)\big)^{3/2}$ for $x\ge c$: infinitely many |
| $y'=3y^{2/3},\ y(0)=0$ | $y=0$ and $y=(x-c)^3$ (pieced together with $0$): infinitely many |
| $y'=2\sqrt{\lvert y\rvert},\ y(0)=0$ | $y=0$ and $y=(x-c)^2$ for $x\ge c$ |
| $y'=\sqrt{\lvert y\rvert},\ y(0)=y_0\ne0$ | **unique** locally (locally Lipschitz away from $0$) |
| $xy'=2y,\ y(0)=0$ | $y=cx^2$: infinitely many ($f=2y/x$ is discontinuous at $x=0$) |
| $xy'=2y,\ y(0)=1$ | **no** solution |

## 6. Interval of existence and blow-up
- $y'=y^2,\ y(0)=y_0>0$ gives $y=\dfrac{y_0}{1-y_0x}$, with maximal interval $(-\infty,1/y_0)$.
- $y'=1+y^2,\ y(0)=0$ gives $y=\tan x$ on $(-\pi/2,\pi/2)$.
- Picard's $h$ for $y'=y^2$, $y(0)=1$: we get $h=\min\big(a,\frac{b}{(1+b)^2}\big)$, which is at most $\tfrac14$ (attained at $b=1$). The guaranteed $h$ is often much smaller than the true interval.
- **Continuation:** a solution can be extended until $(x,y(x))$ leaves every compact subset of the domain, i.e. it blows up or reaches the boundary.

## 7. Related facts
- **Gronwall:** if $u(x)\le C+\int_{x_0}^x L\,u$, then $u\le Ce^{L|x-x_0|}$. This gives uniqueness and continuous dependence: $|y_1-y_2|\le|y_1(x_0)-y_2(x_0)|e^{L|x-x_0|}$.
- The proof of Picard's theorem uses the **Banach contraction principle** on $C[x_0-h,x_0+h]$ (using a weighted norm, or a small $h$ with $Lh<1$).
- For systems and $n$th-order equations the same theorems hold with $|\cdot|$ replaced by a norm.

## Exam traps
- In $h=\min(a,b/M)$, $M$ is the **max of $|f|$ over the rectangle**, not its value at $(x_0,y_0)$.
- "Continuous implies unique" is **false**. "Lipschitz implies unique" is **true**. "Unique implies Lipschitz" is **false**.
- $|y|$ is Lipschitz even though it is not differentiable at $0$.
- $\sqrt{|y|}$ fails uniqueness **only** at $y_0=0$.
- For a linear ODE, the existence interval is the **entire** interval of continuity of the coefficients containing $x_0$. Do not compute $b/M$.
- Do not confuse the Picard iterates with the Taylor series. They coincide only for special equations such as $y'=y$.
