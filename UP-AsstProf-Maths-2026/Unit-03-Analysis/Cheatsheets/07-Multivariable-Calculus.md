# Cheatsheet · Unit 3 · Topic 07 — Multivariable Calculus
> Questions: [../Questions/07-Multivariable-Calculus.md](../Questions/07-Multivariable-Calculus.md)

## 1. Limits and continuity in $\mathbb R^2$
- $\lim_{(x,y)\to(a,b)}f=L$ means $|f-L|<\varepsilon$ whenever $0<\|(x,y)-(a,b)\|<\delta$.
- **Path test:** if two paths give different limits, the limit does not exist. Use $y=mx$, and then $y=mx^2$ (curves can expose what lines miss).
- **Polar test:** if $|f(r\cos\theta,r\sin\theta)-L|\le g(r)\to0$ **uniformly in $\theta$**, the limit is $L$.
- Iterated limits may exist and differ: $\frac{x^2-y^2}{x^2+y^2}$ gives $1$ and $-1$. If the double limit exists and the iterated limits exist, all three are equal.

| $f$ (with $f(0,0)=0$) | Limit at origin | Notes |
|---|---|---|
| $\frac{xy}{x^2+y^2}$ | DNE ($\frac{m}{1+m^2}$) | partials exist (both $0$) |
| $\frac{x^2y}{x^4+y^2}$ | DNE ($\frac12$ on $y=x^2$) | limit $0$ along every line; all directional derivatives exist |
| $\frac{x^2y}{x^2+y^2}$ | $0$ | continuous, not differentiable ($D_uf=a^2b$ is not linear) |
| $\frac{xy(x^2-y^2)}{x^2+y^2}$ | $0$ | $C^1$, but $f_{xy}(0,0)\ne f_{yx}(0,0)$ ($\pm1$) |
| $\sqrt{|xy|}$ | $0$ | partials $0$, not differentiable |
| $(x^2+y^2)\sin\frac1{\sqrt{x^2+y^2}}$ | $0$ | differentiable, but the partials are **not continuous** |

## 2. Derivatives
- **Partial derivative:** $f_x(a,b)=\lim_{h\to0}\frac{f(a+h,b)-f(a,b)}{h}$.
- **Directional derivative** along a **unit** vector $\mathbf u$: $D_{\mathbf u}f(p)=\lim_{t\to0}\frac{f(p+t\mathbf u)-f(p)}{t}$.
- **Total derivative (Fréchet):** $f:\mathbb R^n\to\mathbb R^m$ is differentiable at $p$ if there is a linear map $L$ with
  $$\lim_{h\to0}\frac{\|f(p+h)-f(p)-Lh\|}{\|h\|}=0.$$
  Then $L=Df(p)$, whose matrix is the **Jacobian** $\left(\partial f_i/\partial x_j\right)_{m\times n}$.
- If $f$ is differentiable: $D_{\mathbf u}f=\nabla f\cdot\mathbf u$. The maximum of $D_{\mathbf u}f$ is $\|\nabla f\|$, in the direction of $\nabla f$, and $\nabla f$ is normal to the level set.
- **Differentiability test at $(0,0)$:** check $\frac{f(h,k)-f(0,0)-f_xh-f_yk}{\sqrt{h^2+k^2}}\to0$.

### Implications
$$C^1\ (\text{continuous partials}) \Rightarrow \text{differentiable} \Rightarrow \begin{cases}\text{continuous}\\ \text{all } D_uf \text{ exist, linear in } u\end{cases}\Rightarrow\text{partials exist}$$
- **No arrow reverses.**
- Partials existing does **not** give continuity.
- Every directional derivative existing does **not** give continuity.
- Sufficient condition: one partial exists at $p$, and the other exists near $p$ and is continuous at $p$.

## 3. Higher derivatives
- **Schwarz/Clairaut:** if $f_{xy}$ and $f_{yx}$ exist near $p$ and are continuous at $p$ (in particular if $f\in C^2$), then $f_{xy}(p)=f_{yx}(p)$.
- **Young's version:** if $f_x,f_y$ are differentiable at $p$, the mixed partials agree.
- **Taylor (2 variables):**
  $$f(a+h,b+k)=f+(hf_x+kf_y)+\tfrac1{2!}(h^2f_{xx}+2hkf_{xy}+k^2f_{yy})+\cdots$$
- **Euler (homogeneous of degree $n$):** $xf_x+yf_y=nf$ and $x^2f_{xx}+2xyf_{xy}+y^2f_{yy}=n(n-1)f$.

## 4. Chain rule, Jacobians, implicit and inverse functions
- $D(g\circ f)(p)=Dg(f(p))\,Df(p)$ (matrix product).
- **Jacobian rules:** $\frac{\partial(u,v)}{\partial(x,y)}\cdot\frac{\partial(x,y)}{\partial(u,v)}=1$. If $u,v$ are functionally dependent, then $J\equiv0$.
- **Standard Jacobians:**
  - polar: $r$
  - cylindrical: $r$
  - spherical: $r^2\sin\phi$
  - $(u,v)=(x^2-y^2,2xy)$: $4(x^2+y^2)$
- **Implicit Function Theorem:** if $F\in C^1$, $F(a,b)=0$ and $F_y(a,b)\ne0$, then near $a$ there is a unique $C^1$ function $y=g(x)$ with $F(x,g(x))=0$, and $g'=-F_x/F_y$.
  - For $F(x,y,z)=0$: $z_x=-F_x/F_z$ and $z_y=-F_y/F_z$.
  - Vector form: $\det\partial F/\partial y\ne0$.
- **Inverse Function Theorem:** if $f\in C^1$ and $\det Jf(p)\ne0$, then $f$ is a local $C^1$ diffeomorphism near $p$.
  - This is **local only**: $(e^x\cos y,e^x\sin y)$ has $J=e^{2x}\neq0$ but is not injective.

## 5. Maxima and minima
- **Necessary condition:** an interior extremum of a differentiable $f$ has $\nabla f=0$ (a critical point).
- **Second-derivative test** at a critical point, with $r=f_{xx},s=f_{xy},t=f_{yy}$:

| Condition | Nature |
|---|---|
| $rt-s^2>0,\ r>0$ | local minimum |
| $rt-s^2>0,\ r<0$ | local maximum |
| $rt-s^2<0$ | saddle point |
| $rt-s^2=0$ | inconclusive (e.g. $x^4+y^4$ min, $x^3+y^3$ neither, $x^4-y^4$ saddle) |

- **$n$ variables:** the Hessian is positive definite (all leading principal minors $>0$) for a minimum, negative definite (minors alternate $-,+,-,\dots$) for a maximum, and indefinite for a saddle.
- **Worked example:** $x^3+y^3-3xy$ has a saddle at $(0,0)$ and a local minimum $-1$ at $(1,1)$.
- **Extreme value theorem:** a continuous function on a compact set attains its max and min. Check interior critical points **and** the boundary.

## 6. Lagrange multipliers
- To find extrema of $f$ subject to $g=c$ (with $\nabla g\ne0$): solve $\nabla f=\lambda\nabla g$, $g=c$.
- With two constraints: $\nabla f=\lambda\nabla g+\mu\nabla h$.
- **Standard answers:**
  - Distance from the origin to $ax+by+cz=d$: $\frac{|d|}{\sqrt{a^2+b^2+c^2}}$, so $\min(x^2+y^2+z^2)=\frac{d^2}{a^2+b^2+c^2}$.
  - $\max xyz$ subject to $x+y+z=3k$ ($x,y,z>0$): $k^3$ (AM–GM).
  - $\max xyz$ on $x^2+y^2+z^2=3$: $1$.
  - Extrema of $ax+by$ on $x^2+y^2=1$: $\pm\sqrt{a^2+b^2}$.
  - Extrema of a quadratic form $\mathbf x^TA\mathbf x$ on $\|\mathbf x\|=1$: the extreme eigenvalues of $A$.

## Exam traps
- Normalise the direction vector before computing a directional derivative.
- "All directional derivatives exist" does not give differentiability, or even continuity.
- Differentiable does not imply $C^1$: $x^2\sin(1/x)$-type examples have discontinuous partials.
- When $rt-s^2=0$, look at the function directly. Never conclude "no extremum".
- Equality of mixed partials needs **continuity** of them, not just existence.
- The inverse function theorem gives **local** invertibility only.
- In a Lagrange problem, $\lambda$ itself is not the answer. Substitute the point back into $f$.
