# Unit 7 · Topic 04 — Laplace Transforms
> Syllabus coverage: Laplace transforms (existence, shifting theorems, derivatives/integrals of transforms, convolution, inverse transforms, initial/final value theorems, unit step and impulse, solution of ODEs and integral equations)
> Cheatsheet: [../Cheatsheets/04-Laplace-Transforms.md](../Cheatsheets/04-Laplace-Transforms.md)

**Q1.** `[Concept]` ★ $\mathcal{L}\{\sqrt t\}$ equals

(A) $\dfrac{\sqrt\pi}{2s^{3/2}}$

(B) $\dfrac{\sqrt\pi}{s^{1/2}}$

(C) $\dfrac{1}{2s^{3/2}}$

(D) $\dfrac{\sqrt\pi}{s^{3/2}}$

**Q2.** `[Numerical]` ★ $\mathcal{L}\{e^{2t}\sin 3t\}$ equals

(A) $\dfrac{3}{(s+2)^2+9}$

(B) $\dfrac{s-2}{(s-2)^2+9}$

(C) $\dfrac{3}{(s-2)^2+9}$

(D) $\dfrac{3}{(s-2)^2-9}$

**Q3.** `[Numerical]` ★★ $\mathcal{L}\{t\sin t\}$ equals

(A) $\dfrac{2s}{(s^2+1)^2}$

(B) $\dfrac{s^2-1}{(s^2+1)^2}$

(C) $\dfrac{-2s}{(s^2+1)^2}$

(D) $\dfrac{1}{(s^2+1)^2}$

**Q4.** `[Numerical]` ★★ $\mathcal{L}^{-1}\left\{\dfrac{1}{s(s^2+1)}\right\}$ equals

(A) $1+\cos t$

(B) $\sin t$

(C) $1-\cos t$

(D) $t-\sin t$

**Q5.** `[Numerical]` ★★★ The value of $\displaystyle\int_0^\infty \frac{e^{-t}\sin t}{t}\,dt$ is

(A) $\dfrac{\pi}{2}$

(B) $\dfrac{\pi}{4}$

(C) $\dfrac{1}{2}$

(D) $\ln 2$

**Q6.** `[Concept]` ★★ $\mathcal{L}^{-1}\left\{\dfrac{e^{-2s}}{s^2}\right\}$ equals ($u$ = unit step)

(A) $t\,u(t-2)$

(B) $(t-2)\,u(t)$

(C) $(t+2)\,u(t+2)$

(D) $(t-2)\,u(t-2)$

**Q7.** `[Application]` ★★★ The solution of the integral equation $y(t)=t+\displaystyle\int_0^t \sin(t-u)\,y(u)\,du$ is

(A) $t+\dfrac{t^3}{6}$

(B) $\sinh t$

(C) $t+\dfrac{t^3}{3}$

(D) $t-\dfrac{t^3}{6}$

**Q8.** `[Multi-Statement]` ★★ Consider the statements:

I. Every piecewise continuous function of exponential order on $[0,\infty)$ has a Laplace transform for all sufficiently large $s$.

II. $\mathcal{L}\{t^{-1/2}\}$ exists, although $t^{-1/2}$ is not piecewise continuous on $[0,\infty)$.

III. $\mathcal{L}\{e^{t^2}\}$ exists for $s>0$.

IV. If $f$ is piecewise continuous and of exponential order, then $\mathcal{L}\{f\}(s)\to0$ as $s\to\infty$.

Which are correct?

(A) I and II only

(B) I, II and IV only

(C) I and III only

(D) I, II, III and IV

**Q9.** `[Assertion-Reason]` ★★
**Assertion (A):** By the final value theorem, $\displaystyle\lim_{t\to\infty}\sin t=\lim_{s\to0}\frac{s}{s^2+1}=0$.
**Reason (R):** The final value theorem $\lim_{t\to\infty}f(t)=\lim_{s\to0}sF(s)$ is valid only when all poles of $sF(s)$ lie in the open left half-plane.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[Match]` ★★ Match $F(s)$ (List-I) with $f(t)=\mathcal{L}^{-1}\{F\}$ (List-II).

| List-I | List-II |
|---|---|
| (a) $\dfrac{s}{s^2+a^2}$ | 1. $t\,e^{at}$ |
| (b) $\dfrac{a}{s^2-a^2}$ | 2. $\delta(t)$ |
| (c) $\dfrac{1}{(s-a)^2}$ | 3. $\cos at$ |
| (d) $1$ | 4. $\sinh at$ |

(A) a-3, b-1, c-4, d-2

(B) a-3, b-4, c-1, d-2

(C) a-4, b-3, c-1, d-2

(D) a-3, b-4, c-2, d-1

**Q11.** `[NOT-true / Counterexample]` ★ With $F=\mathcal{L}\{f\}$, $G=\mathcal{L}\{g\}$, which is NOT true in general?

(A) $\mathcal{L}\left\{\int_0^t f(u)g(t-u)\,du\right\}=F(s)G(s)$

(B) $\mathcal{L}\{f'(t)\}=sF(s)-f(0)$

(C) $\mathcal{L}\{f(t)g(t)\}=F(s)G(s)$

(D) $\mathcal{L}\left\{\dfrac{f(t)}{t}\right\}=\displaystyle\int_s^\infty F(u)\,du$ (when $\lim_{t\to0^+}f(t)/t$ exists)

**Q12.** `[Numerical]` ★★ If $F(s)=\dfrac{s+3}{s(s+1)(s+2)}$, then $\displaystyle\lim_{t\to\infty}f(t)$ equals

(A) $0$

(B) $3$

(C) $\dfrac{3}{2}$

(D) $\dfrac{1}{2}$

**Q13.** `[Numerical]` ★★ If $y'+y=u(t-1)$, $y(0)=0$, then $y(2)$ equals

(A) $1-e^{-2}$

(B) $0$

(C) $e^{-1}$

(D) $1-e^{-1}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | C | Numerical |
| 3 | A | Numerical |
| 4 | C | Numerical |
| 5 | B | Numerical |
| 6 | D | Concept |
| 7 | A | Application |
| 8 | B | Multi-Statement |
| 9 | D | Assertion-Reason |
| 10 | B | Match |
| 11 | C | NOT-true / Counterexample |
| 12 | C | Numerical |
| 13 | D | Numerical |

## Solutions
**Q1 — (A).** $\mathcal{L}\{t^\nu\}=\frac{\Gamma(\nu+1)}{s^{\nu+1}}$; $\Gamma(3/2)=\frac{\sqrt\pi}{2}$. (B) is $\mathcal{L}\{t^{-1/2}\}$.

**Q2 — (C).** First shifting: $\mathcal{L}\{e^{at}f\}=F(s-a)$ with $F=\frac{3}{s^2+9}$. (A) shifts the wrong way.

**Q3 — (A).** $\mathcal{L}\{tf\}=-F'(s)=-\frac{d}{ds}\frac1{s^2+1}=\frac{2s}{(s^2+1)^2}$. (B) is $\mathcal{L}\{t\cos t\}$; (C) forgets the minus sign.

**Q4 — (C).** $\frac{1}{s(s^2+1)}=\frac1s-\frac{s}{s^2+1}$ ⇒ $1-\cos t$ (or $\int_0^t\sin u\,du$). (D) is $\mathcal{L}^{-1}\{\frac{1}{s^2(s^2+1)}\}$.

**Q5 — (B).** $\mathcal{L}\{\frac{\sin t}{t}\}=\int_s^\infty\frac{du}{u^2+1}=\tan^{-1}\frac1s$; at $s=1$: $\pi/4$. (A) is the value at $s=0$.

**Q6 — (D).** Second shifting: $\mathcal{L}\{f(t-a)u(t-a)\}=e^{-as}F(s)$ with $f=t$, $a=2$. (A) shifts the step but not the function.

**Q7 — (A).** $Y=\frac1{s^2}+\frac{Y}{s^2+1}$ ⇒ $Y\frac{s^2}{s^2+1}=\frac1{s^2}$ ⇒ $Y=\frac{s^2+1}{s^4}=\frac1{s^2}+\frac1{s^4}$ ⇒ $y=t+\frac{t^3}{6}$. (D) comes from a sign error.

**Q8 — (B).** I: standard existence theorem (sufficient). II: $\mathcal{L}\{t^{-1/2}\}=\sqrt{\pi/s}$, so the condition in I is not necessary. III: $e^{t^2-st}\to\infty$, no transform. IV: true for such $f$ (so e.g. $F(s)=1$ or $s$ is not the transform of an ordinary function).

**Q9 — (D).** $\lim_{t\to\infty}\sin t$ does not exist; $sF(s)=\frac{s}{s^2+1}$ has poles $\pm i$ on the imaginary axis, so the FVT does not apply. A is false, R is true.

**Q10 — (B).** $\cos at$; $\sinh at$; first shift of $\mathcal{L}\{t\}=1/s^2$ gives $te^{at}$; $\mathcal{L}\{\delta\}=1$.

**Q11 — (C).** The transform of a product is not the product of transforms (that is the convolution theorem, A). E.g. $f=g=1$: $\mathcal{L}\{1\}=\frac1s\ne\frac1{s^2}$.

**Q12 — (C).** $sF=\frac{s+3}{(s+1)(s+2)}$ has poles $-1,-2$ (left half-plane), so FVT applies: $\frac{3}{2}$. (B) forgets the factor $(s+1)(s+2)=2$ at $s=0$; (A) wrongly assumes $f$ must decay (the pole of $F$ at $s=0$ gives a constant term $\frac32$ in $f$).

**Q13 — (D).** $(s+1)Y=\frac{e^{-s}}{s}$ ⇒ $Y=e^{-s}\left(\frac1s-\frac1{s+1}\right)$ ⇒ $y=\left(1-e^{-(t-1)}\right)u(t-1)$. At $t=2$: $1-e^{-1}$. (A) ignores the delay.
