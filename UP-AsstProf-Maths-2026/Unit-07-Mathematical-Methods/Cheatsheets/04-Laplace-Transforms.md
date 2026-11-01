# Cheatsheet · Unit 7 · Topic 04 — Laplace Transforms
> Questions: [../Questions/04-Laplace-Transforms.md](../Questions/04-Laplace-Transforms.md)

## 1. Definition & existence
$$F(s)=\mathcal{L}\{f\}(s)=\int_0^\infty e^{-st}f(t)\,dt.$$
- **Exponential order** $\alpha$: $|f(t)|\le Me^{\alpha t}$ for $t\ge T$.
- **Existence theorem (sufficient):** $f$ piecewise continuous on every $[0,T]$ and of exponential order $\alpha$ ⇒ $F(s)$ exists (absolutely) for $s>\alpha$, and $F(s)\to0$ as $s\to\infty$.
- Not necessary: $t^{-1/2}$ (singular at 0) has $\mathcal{L}=\sqrt{\pi/s}$. No transform: $e^{t^2}$, $1/t$ (diverges at 0).
- $\mathcal{L}$ is linear and (Lerch) injective on continuous functions.
- If $F(s)\not\to0$ (e.g. $1$, $s$, $\frac{s}{s+1}$), it is not the transform of an ordinary function (distributions: $\mathcal{L}\{\delta\}=1$).

## 2. Table
| $f(t)$ | $F(s)$ | | $f(t)$ | $F(s)$ |
|---|---|---|---|---|
| $1$ | $\frac1s$ | | $\sin at$ | $\frac{a}{s^2+a^2}$ |
| $t^n$ | $\frac{n!}{s^{n+1}}$ | | $\cos at$ | $\frac{s}{s^2+a^2}$ |
| $t^\nu\ (\nu>-1)$ | $\frac{\Gamma(\nu+1)}{s^{\nu+1}}$ | | $\sinh at$ | $\frac{a}{s^2-a^2}$ |
| $\sqrt t$ | $\frac{\sqrt\pi}{2s^{3/2}}$ | | $\cosh at$ | $\frac{s}{s^2-a^2}$ |
| $t^{-1/2}$ | $\sqrt{\pi/s}$ | | $t\sin at$ | $\frac{2as}{(s^2+a^2)^2}$ |
| $e^{at}$ | $\frac1{s-a}$ | | $t\cos at$ | $\frac{s^2-a^2}{(s^2+a^2)^2}$ |
| $t^ne^{at}$ | $\frac{n!}{(s-a)^{n+1}}$ | | $\frac{\sin t}{t}$ | $\tan^{-1}\frac1s$ |
| $u(t-a)$ | $\frac{e^{-as}}{s}$ | | $\delta(t-a)$ | $e^{-as}$ |
| $\frac{1-\cos t}{t}$ | $\frac12\ln\frac{s^2+1}{s^2}$ | | $\mathrm{erf}\sqrt t$ | $\frac{1}{s\sqrt{s+1}}$ |
| $J_0(t)$ | $\frac{1}{\sqrt{s^2+1}}$ | | $\sin at-at\cos at$ | $\frac{2a^3}{(s^2+a^2)^2}$ |

## 3. Properties
| Property | Formula |
|---|---|
| First shifting | $\mathcal{L}\{e^{at}f\}=F(s-a)$ |
| Second shifting | $\mathcal{L}\{f(t-a)u(t-a)\}=e^{-as}F(s)$; $\mathcal{L}\{g(t)u(t-a)\}=e^{-as}\mathcal{L}\{g(t+a)\}$ |
| Change of scale | $\mathcal{L}\{f(at)\}=\frac1aF(\frac sa)$ |
| Derivative | $\mathcal{L}\{f'\}=sF-f(0)$; $\mathcal{L}\{f''\}=s^2F-sf(0)-f'(0)$; $\mathcal{L}\{f^{(n)}\}=s^nF-\sum s^{n-k}f^{(k-1)}(0)$ |
| Integral | $\mathcal{L}\{\int_0^tf\}=\frac{F(s)}{s}$ |
| Multiplication by $t^n$ | $\mathcal{L}\{t^nf\}=(-1)^nF^{(n)}(s)$ |
| Division by $t$ | $\mathcal{L}\{f/t\}=\int_s^\infty F(u)du$ (if $\lim_{t\to0^+}f/t$ exists) |
| Periodic, period $T$ | $F=\frac{1}{1-e^{-sT}}\int_0^Te^{-st}f\,dt$ |
| Convolution | $\mathcal{L}\{f*g\}=FG$, $(f*g)(t)=\int_0^tf(u)g(t-u)du$ |
| Initial value | $f(0^+)=\lim_{s\to\infty}sF(s)$ |
| Final value | $\lim_{t\to\infty}f=\lim_{s\to0}sF(s)$ **only if** all poles of $sF$ in $\mathrm{Re}\,s<0$ |

**Evaluating integrals:** $\int_0^\infty e^{-st}f\,dt=F(s)$; $\int_0^\infty\frac{f(t)}{t}dt=\int_0^\infty F(u)du$.
- $\int_0^\infty\frac{\sin t}{t}dt=\frac\pi2$; $\int_0^\infty\frac{e^{-t}\sin t}{t}dt=\frac\pi4$; $\int_0^\infty te^{-2t}\sin t\,dt=\frac{4}{25}$; $\int_0^\infty\frac{e^{-at}-e^{-bt}}{t}dt=\ln\frac ba$.

## 4. Inverse transforms
- Partial fractions; completing the square; shifting; convolution: $\mathcal{L}^{-1}\{FG\}=f*g$.
- $\mathcal{L}^{-1}\{\frac{F(s)}{s}\}=\int_0^tf$. E.g. $\frac1{s(s^2+1)}\to1-\cos t$, $\frac1{s^2(s^2+1)}\to t-\sin t$.
- $\mathcal{L}^{-1}\{\frac{1}{(s^2+a^2)^2}\}=\frac{\sin at-at\cos at}{2a^3}$; $\mathcal{L}^{-1}\{\frac{s}{(s^2+a^2)^2}\}=\frac{t\sin at}{2a}$.
- $\mathcal{L}^{-1}\{\ln\frac{s+a}{s+b}\}=\frac{e^{-bt}-e^{-at}}{t}$; $\mathcal{L}^{-1}\{\tan^{-1}\frac as\}=\frac{\sin at}{t}$ (use $\mathcal{L}^{-1}\{F'\}=-tf$).
- Heaviside expansion: $F=\frac{P}{Q}$, simple zeros $a_k$ of $Q$ ⇒ $f=\sum\frac{P(a_k)}{Q'(a_k)}e^{a_kt}$.
- Complex inversion (Bromwich): $f(t)=\frac1{2\pi i}\int_{c-i\infty}^{c+i\infty}e^{st}F(s)ds$ = sum of residues of $e^{st}F$.

## 5. Unit step and impulse
- $u(t-a)=0$ ($t<a$), $1$ ($t>a$). Piecewise $f$: write with steps, e.g. $f=g_1+(g_2-g_1)u(t-a)$.
- $\delta(t-a)$: $\int\delta(t-a)g=g(a)$, $\mathcal{L}=e^{-as}$, $u'(t-a)=\delta(t-a)$.
- Response of $y'+y=u(t-1)$, $y(0)=0$: $y=(1-e^{-(t-1)})u(t-1)$.
- $y''+y=\delta(t-\pi)$, $y(0)=y'(0)=0$: $y=\sin(t-\pi)u(t-\pi)=-\sin t\,u(t-\pi)$.

## 6. Solving ODEs and integral equations
**ODE (constant coeffs):** transform, use derivative formula with ICs, solve algebraically for $Y$, invert.
- $y''-3y'+2y=0$, $y(0)=0,y'(0)=1$: $Y=\frac1{(s-1)(s-2)}$ ⇒ $y=e^{2t}-e^t$.
- Variable coefficients $t\,y$: use $\mathcal{L}\{ty\}=-Y'$ (gives an ODE in $s$).

**Convolution integral equations:**
- $y=f+\int_0^tk(t-u)y(u)du$ ⇒ $Y=\frac{F}{1-K}$.
- $y=t+\int_0^t\sin(t-u)y\,du$ ⇒ $y=t+\frac{t^3}{6}$.
- $y=1+\int_0^t y\,du$ ⇒ $e^t$; $y=\sin t+\int_0^t y\,du$ ⇒ $Y=\frac{s}{(s-1)(s^2+1)}$ ⇒ $y=\frac12(e^t-\cos t+\sin t)$.
- Abel: $\int_0^t\frac{y(u)}{\sqrt{t-u}}du=f$ ⇒ $Y\sqrt{\pi/s}=F$.
- Integro-differential: $y'+\int_0^ty=g$ ⇒ $(s+\frac1s)Y-y(0)=G$.

## 7. Exam traps
- First shift: $e^{at}$ ⇒ $s\to s-a$ (minus!). Second shift needs $f(t-a)$, not $f(t)$, multiplied by $u(t-a)$.
- $\mathcal{L}\{fg\}\ne FG$; only convolution gives a product.
- $\mathcal{L}\{tf\}=-F'$ (minus sign); $\mathcal{L}\{f/t\}=\int_s^\infty F$.
- Final value theorem fails for $\sin t$, $\cos t$, $e^t$ (poles on/right of the imaginary axis).
- Initial value theorem gives $f(0^+)$; e.g. $F=\frac{2s+3}{s^2+4s+5}$ ⇒ $f(0^+)=2$.
- Existence conditions are sufficient, not necessary ($t^{-1/2}$).
- $\Gamma(\frac12)=\sqrt\pi$, $\Gamma(\frac32)=\frac{\sqrt\pi}{2}$.
