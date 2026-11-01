# Cheatsheet · Unit 2 · Topic 02 — Linear Functionals and Dual Spaces

## 1. Linear functionals
- A **linear functional** on $V$ over $F$ is a linear map $f:V\to F$. The **dual space** is $V^\ast =L(V,F)$.
- Examples: trace on $M_n$; $p\mapsto p(a)$ (evaluation); $p\mapsto\int_a^b p$; $x\mapsto a\cdot x$ on $F^n$.
- Non-examples: $\det$ (for $n\ge2$), $x\mapsto\Vert x\Vert$, $x\mapsto x_1x_2$, $x\mapsto x_1+1$.
- If $f\ne0$, then $f$ is onto $F$ and $\ker f$ is a **hyperplane** of dimension $n-1$.
- If $\ker f\subseteq\ker g$ and $f\ne0$, then $g=cf$. Two non-zero functionals with the same kernel are scalar multiples of each other.
- More generally, $g\in\mathop{\mathrm{span}}\nolimits\lbrace f_1,\dots,f_k\rbrace \iff\bigcap\ker f_i\subseteq\ker g$.

## 2. Dual basis
- For a basis $\mathcal B=\lbrace v_1,\dots,v_n\rbrace$ the dual basis $\lbrace f_i\rbrace$ is defined by $f_i(v_j)=\delta_{ij}$. Hence $\dim V^\ast =\dim V$ when $V$ is finite-dimensional.
- $v=\sum_i f_i(v)\thinspace v_i$ (the $f_i$ give coordinates) and $f=\sum_i f(v_i)\thinspace f_i$ for $f\in V^\ast$.
- **Computing it in $F^n$:** put $v_j$ as the columns of $P$. The dual basis functionals are the **rows of $P^{-1}$**.

## 3. Annihilators
$W^0=\lbrace f\in V^\ast : f|_W=0\rbrace$ is a subspace of $V^\ast$.

| Property | Formula |
|---|---|
| Dimension | $\dim W+\dim W^0=\dim V$ |
| Order reversal | $W_1\subseteq W_2\Rightarrow W_2^0\subseteq W_1^0$ |
| Sum | $(W_1+W_2)^0=W_1^0\cap W_2^0$ |
| Intersection | $(W_1\cap W_2)^0=W_1^0+W_2^0$ (finite-dimensional) |
| Double annihilator | $W^{00}=J(W)$, identified with $W$ |
| Quotient | $W^0\cong (V/W)^\ast$, and $W^\ast \cong V^\ast /W^0$ |

- Every $k$-dimensional subspace of $F^n$ is the solution set of $n-k$ independent homogeneous linear equations, namely a basis of $W^0$.

## 4. Double dual
- The natural map $J:V\to V^{\ast \ast }$, $J(v)(f)=f(v)$, is linear and **injective for every $V$**.
- If $\dim V\lt \infty$, $J$ is an isomorphism. It is canonical, needing no choice of basis, whereas $V\cong V^\ast$ depends on a basis.
- If $\dim V=\infty$, then $\dim V^\ast \gt \dim V$ and $J$ is **not onto**.

## 5. Transpose (dual map)
For $T:V\to W$, define $T^t:W^\ast \to V^\ast$ by $T^t(g)=g\circ T$.
- $`[T^t]_{\mathcal B^\ast ,\mathcal C^\ast }=\big([T]_{\mathcal C,\mathcal B}\big)^T`$.
- $\ker T^t=(\mathop{\mathrm{range}}\nolimits T)^0$ and $\mathop{\mathrm{range}}\nolimits T^t=(\ker T)^0$.
- $\mathop{\mathrm{rank}}\nolimits T^t=\mathop{\mathrm{rank}}\nolimits T$, which is the abstract form of *row rank = column rank*.
- $(ST)^t=T^tS^t$ and $(T^{-1})^t=(T^t)^{-1}$.
- $T$ is injective $\iff T^t$ is surjective, and $T$ is surjective $\iff T^t$ is injective.

## Exam traps
- $\dim\ker T^t$ uses $\dim W$ (the *codomain* of $T$): $\dim\ker T^t=\dim W-\mathop{\mathrm{rank}}\nolimits T$.
- The dual basis of a non-standard basis is **not** made of the coordinate functionals $x,y$. You must invert.
- $(W_1\cap W_2)^0$ is a **sum**, not an intersection.
- Injectivity of $V\to V^{\ast \ast }$ holds always; only surjectivity needs finite dimension.
- $\det$ and norms are not linear functionals.
