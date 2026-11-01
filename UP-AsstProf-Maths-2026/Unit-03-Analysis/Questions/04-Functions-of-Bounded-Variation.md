# Unit 3 · Topic 04 — Functions of Bounded Variation
> Syllabus coverage: Functions of bounded variation (total, positive and negative variation, Jordan decomposition, relation with continuity / differentiability / Lipschitz and absolutely continuous functions, standard examples and counterexamples)
> Cheatsheet: [../Cheatsheets/04-Functions-of-Bounded-Variation.md](../Cheatsheets/04-Functions-of-Bounded-Variation.md)

**Q1.** `[Concept]` ★ (Jordan decomposition) A function $f:[a,b]\to\mathbb{R}$ is of bounded variation if and only if

(A) $f$ is continuous and bounded

(B) $f$ is the difference of two monotonically increasing functions on $[a,b]$

(C) $f$ is differentiable almost everywhere

(D) $f$ is the sum of a continuous function and a step function

**Q2.** `[Numerical]` ★ The total variation of $f(x)=\sin x$ on $[0,2\pi]$ is

(A) $0$

(B) $4$

(C) $2$

(D) $2\pi$

**Q3.** `[Numerical]` ★★ Define $f$ on $[0,2]$ by
```math
f(x)=\begin{cases}x,&0\le x\lt 1\cr 3,&x=1\cr x+1,&1\lt x\le2\end{cases}
```
The total variation $V_0^2(f)$ is

(A) $3$

(B) $4$

(C) $5$

(D) $6$

**Q4.** `[Multi-Statement]` ★★ Let $f$ be of bounded variation on $[a,b]$.

I. $f$ is bounded on $[a,b]$.

II. $f$ is continuous on $[a,b]$.

III. $f$ has at most countably many points of discontinuity.

Which of the above is/are necessarily correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and III only

**Q5.** `[Assertion-Reason]` ★★ Let $f(x)=x\sin(1/x)$ for $0\lt x\le1$ and $f(0)=0$.
**Assertion (A):** $f$ is continuous on $[0,1]$ but is not of bounded variation on $[0,1]$.
**Reason (R):** Every continuous function on a closed bounded interval is of bounded variation.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ On $[0,1]$, with each function taken to be $0$ at $x=0$, match List-I with List-II.

| List-I | List-II |
|---|---|
| a. $x\sin(1/x)$ | 1. of bounded variation but not Lipschitz |
| b. $x^2\sin(1/x)$ | 2. differentiable everywhere but not of bounded variation |
| c. $x^2\sin(1/x^2)$ | 3. continuous, not differentiable at $0$, not of bounded variation |
| d. $\sqrt{x}$ | 4. differentiable with bounded derivative, hence of bounded variation |

(A) a-3, b-4, c-2, d-1

(B) a-3, b-2, c-4, d-1

(C) a-2, b-4, c-3, d-1

(D) a-1, b-4, c-2, d-3

**Q7.** `[NOT-true / Counterexample]` ★★ Let $f,g\in BV[a,b]$. Which of the following is **NOT** true in general?

(A) $f+g$ and $fg$ are of bounded variation.

(B) If $|g|\ge c\gt 0$ on $[a,b]$, then $f/g$ is of bounded variation.

(C) $f$ is differentiable almost everywhere on $[a,b]$.

(D) $f\circ g$ is of bounded variation whenever it is defined.

**Q8.** `[Application]` ★★★ Let $f_\alpha(x)=x^\alpha\sin(1/x)$ for $0\lt x\le1$ and $f_\alpha(0)=0$. Then $f_\alpha$ is of bounded variation on $[0,1]$ if and only if

(A) $\alpha\gt 0$

(B) $\alpha\ge1$

(C) $\alpha\gt 1$

(D) $\alpha\gt 2$

**Q9.** `[Numerical]` ★★ For $f(x)=x^3-3x$ on $[-2,2]$, the **positive variation** $P_{-2}^{2}(f)$ is

(A) $4$

(B) $8$

(C) $12$

(D) $16$

**Q10.** `[Concept]` ★★ Let $f\in BV[a,b]$ and $V(x)=V_a^x(f)$ for $a\le x\le b$ (with $V(a)=0$). Which statement is correct?

(A) $V$ is increasing, and $V$ is continuous at $c$ if and only if $f$ is continuous at $c$.

(B) $V$ is always continuous, even if $f$ is not.

(C) $V$ is continuous only if $f$ is differentiable.

(D) $V-f$ is decreasing.

**Q11.** `[Application]` ★★★ Define $f$ on $[0,1]$ by $f\negthinspace \left(\frac1n\right)=\frac1{n^2}$ for $n=1,2,3,\dots$ and $f(x)=0$ at every other point. The total variation $V_0^1(f)$ equals

(A) $\dfrac{\pi^2}{6}$

(B) $\dfrac{\pi^2}{3}$

(C) $\infty$

(D) $\dfrac{\pi^2}{3}-1$

**Q12.** `[Concept]` ★ On $[a,b]$, which chain of inclusions is correct?

(A) $C^1[a,b]\subset\text{Lip}[a,b]\subset AC[a,b]\subset BV[a,b]$

(B) $BV[a,b]\subset AC[a,b]\subset\text{Lip}[a,b]\subset C^1[a,b]$

(C) $C^1[a,b]\subset AC[a,b]\subset\text{Lip}[a,b]\subset BV[a,b]$

(D) $C[a,b]\subset BV[a,b]\subset AC[a,b]$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | B | Numerical |
| 3 | C | Numerical |
| 4 | D | Multi-Statement |
| 5 | C | Assertion-Reason |
| 6 | A | Match |
| 7 | D | NOT-true / Counterexample |
| 8 | C | Application |
| 9 | B | Numerical |
| 10 | A | Concept |
| 11 | D | Application |
| 12 | A | Concept |

## Solutions
**Q1 — (B).** This is Jordan's theorem: $f=\frac{V+f}{2}-\frac{V-f}{2}$, or $f=V-(V-f)$, with both parts increasing. (C) is a consequence, not a characterisation: $x\sin(1/x)$ is differentiable a.e. but not BV.

**Q2 — (B).** $V=\int_0^{2\pi}|\cos x|\thinspace dx=4$. Equivalently, $\sin$ goes $0\to1\to-1\to0$, which gives $1+2+1$. The value $0=f(2\pi)-f(0)$ is the net change, not the variation.

**Q3 — (C).** Use the partition $0\lt 1-\varepsilon\lt 1\lt 1+\varepsilon\lt 2$. The rise on $[0,1)$ contributes $\to1$, the jump up from $1^-$ to $f(1)=3$ contributes $2$, the drop from $3$ to $f(1^+)=2$ contributes $1$, and the rise from $2$ to $3$ on $(1,2]$ contributes $1$. Total $1+2+1+1=5$. Ignoring the isolated value $f(1)=3$ gives $3$.

**Q4 — (D).** $|f(x)|\le|f(a)|+V_a^b f$, so $f$ is bounded. $f$ is a difference of monotone functions, each with countably many jumps, so III holds. II is false: a step function is BV but discontinuous.

**Q5 — (C).** At $x_k=\frac{1}{(k+\frac12)\pi}$, $|f(x_k)|=\frac{1}{(k+\frac12)\pi}$ with alternating signs, so the variation dominates $\sum\frac{2}{(k+\frac12)\pi}=\infty$. Continuity at $0$ follows from $|f|\le x$. So A is true, and A itself refutes R.

**Q6 — (A).** a: continuous, not differentiable at $0$ ($\sin(1/x)$ has no limit), and not BV (Q5), giving 3. b: $|f'|\le 2x+1$ is bounded, so $f$ is Lipschitz and BV, giving 4. c: differentiable everywhere ($f'(0)=0$), but the local extrema at $x=1/\sqrt{(k+1/2)\pi}$ give variation $\gtrsim\sum\frac{1}{k}=\infty$, giving 2. d: monotone, so BV, but $f'$ is unbounded near $0$, so not Lipschitz, giving 1.

**Q7 — (D).** Let $g(x)=x^2\sin^2(1/x)$ (Lipschitz on $[0,1]$, hence BV) and $f(t)=\sqrt t$ (monotone, hence BV). Then $f\circ g=|x\sin(1/x)|$, which is not BV. (A) and (B) are standard closure properties. (C) is Lebesgue's theorem for monotone functions applied to the Jordan decomposition.

**Q8 — (C).** The general fact is that $x^\alpha\sin(x^{-\beta})$ is BV on $[0,1]$ iff $\alpha\gt \beta$. Here $\beta=1$. For $\alpha\gt 1$, the variation is about $\sum_k (k\pi)^{-\alpha}\lt \infty$. At $\alpha=1$ it is the harmonic-type divergence of Q5. Option (B) is the usual trap.

**Q9 — (B).** $f(-2)=-2$, $f(-1)=2$, $f(1)=-2$, $f(2)=2$. The increases are $4+4=8$ and the decrease is $4$. So $V=12$, $P=8$, $N=4$. Check: $P-N=4=f(2)-f(-2)$ and $P+N=V$.

**Q10 — (A).** $V$ is increasing. It is continuous (from the right or left) at $c$ exactly when $f$ is, because the jump of $V$ at $c$ equals the corresponding $|f(c^\pm)-f(c)|$. So a continuous BV function is the difference of two **continuous** increasing functions. (D) is wrong: $V-f$ is increasing, not decreasing.

**Q11 — (D).** Every spike at an interior point $\frac1n$ ($n\ge2$) is approached from both sides by zeros, so it contributes $2\cdot\frac1{n^2}$. The endpoint $x=1$ is approached only from the left and contributes $1$. So $V=1+2\left(\frac{\pi^2}{6}-1\right)=\frac{\pi^2}{3}-1$. Counting every spike twice gives $\frac{\pi^2}{3}$, which is the trap. (With heights $\frac1n$ the variation would be $\infty$.)

**Q12 — (A).** A $C^1$ function has bounded derivative, so it is Lipschitz. Lipschitz functions are absolutely continuous (take $\delta=\varepsilon/L$). AC functions are BV. All inclusions are strict: $|x|$ is Lipschitz but not $C^1$; $\sqrt x$ is AC but not Lipschitz; the Cantor function is BV but not AC. (D) fails because $x\sin(1/x)$ is continuous but not BV.
