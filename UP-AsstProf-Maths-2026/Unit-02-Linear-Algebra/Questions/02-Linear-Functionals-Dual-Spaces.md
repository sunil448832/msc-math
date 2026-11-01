# Unit 2 · Topic 02 — Linear Functionals and Dual Spaces
> Syllabus coverage: linear functionals, dual spaces
> Cheatsheet: [../Cheatsheets/02-Linear-Functionals-Dual-Spaces.md](../Cheatsheets/02-Linear-Functionals-Dual-Spaces.md)

**Q1.** `[Concept]` ★ The dimension of the dual space of $M_{2\times3}(\mathbb{R})$ is

(A) 5

(B) 6

(C) 12

(D) 36

**Q2.** `[Numerical]` ★★ Let $\mathcal{B}=\lbrace v_1=(1,0),\thinspace v_2=(1,1)\rbrace$ be a basis of $\mathbb R^2$ and $\lbrace f_1,f_2\rbrace$ its dual basis. Then

(A) $f_1(x,y)=x-y,\ f_2(x,y)=y$

(B) $f_1(x,y)=x,\ f_2(x,y)=y$

(C) $f_1(x,y)=x,\ f_2(x,y)=x+y$

(D) $f_1(x,y)=x+y,\ f_2(x,y)=-y$

**Q3.** `[Numerical]` ★★ Let $W=\mathop{\mathrm{span}}\nolimits\lbrace (1,2,0,0,1),\thinspace (2,4,0,0,2),\thinspace (0,0,1,1,0)\rbrace \subseteq\mathbb R^5$. The dimension of the annihilator $W^0\subseteq(\mathbb R^5)^\ast$ is

(A) 1

(B) 2

(C) 3

(D) 5

**Q4.** `[Multi-Statement]` ★★ Let $W_1,W_2$ be subspaces of a finite-dimensional space $V$. Consider:

I. $W_1\subseteq W_2\implies W_2^0\subseteq W_1^0$.

II. $(W_1+W_2)^0=W_1^0\cap W_2^0$.

III. $(W_1\cap W_2)^0=W_1^0\cap W_2^0$.

Which is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q5.** `[Assertion-Reason]` ★★★
**Assertion (A):** For an infinite-dimensional vector space $V$, the natural map $V\to V^{\ast \ast }$ need not be an isomorphism.
**Reason (R):** The natural map $J:V\to V^{\ast \ast }$, $J(v)(f)=f(v)$, is injective for every vector space $V$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Let $T:V\to W$ be linear between finite-dimensional spaces, $T^t:W^\ast \to V^\ast$ its transpose ($T^t g=g\circ T$), and $U$ a subspace of $V$. Match:

| List-I | List-II |
|---|---|
| (a) $\ker T^t$ | 1. $(\ker T)^0$ |
| (b) $\mathop{\mathrm{range}}\nolimits T^t$ | 2. $(\mathop{\mathrm{range}}\nolimits T)^0$ |
| (c) $\dim U^0$ | 3. transpose of $[T]_{\mathcal C,\mathcal B}$ |
| (d) $[T^t]_{\mathcal B^\ast ,\mathcal C^\ast }$ | 4. $\dim V-\dim U$ |

(A) a-1, b-2, c-4, d-3

(B) a-1, b-2, c-3, d-4

(C) a-2, b-1, c-3, d-4

(D) a-2, b-1, c-4, d-3

**Q7.** `[NOT-true / Counterexample]` ★★ For $n\ge2$, which of the following is **NOT** a linear functional on $M_n(\mathbb{R})$?

(A) $A\mapsto\mathop{\mathrm{tr}}\nolimits A$

(B) $A\mapsto a_{11}$

(C) $A\mapsto\det A$

(D) $A\mapsto\sum_{i,j}a_{ij}$

**Q8.** `[Application]` ★★★ Let $f,g$ be linear functionals on a vector space $V$ with $f\neq0$ and $\ker f\subseteq\ker g$. Then necessarily

(A) $g=cf$ for some scalar $c$

(B) $g=f$

(C) $\ker f=\ker g$

(D) $g=0$

**Q9.** `[Concept]` ★ If $f$ is a non-zero linear functional on an $n$-dimensional space $V$, then $\dim\ker f$ is

(A) $0$

(B) $1$

(C) $n-1$

(D) $n$

**Q10.** `[Numerical]` ★★ On $P_2$ (real polynomials of degree $\le2$) let $\lbrace f_0,f_1,f_2\rbrace$ be the basis dual to $\lbrace 1,x,x^2\rbrace$. The functional $\varphi(p)=\int_0^1p(x)\thinspace dx$ equals

(A) $f_0+f_1+f_2$

(B) $f_0+\tfrac12f_1+\tfrac13f_2$

(C) $f_0+2f_1+3f_2$

(D) $\tfrac12f_1+\tfrac13f_2$

**Q11.** `[Application]` ★★ Let $T:\mathbb R^4\to\mathbb R^3$ be linear of rank 2. Then $\dim\ker(T^t)$, where $T^t:(\mathbb R^3)^\ast \to(\mathbb R^4)^\ast$, is

(A) 0

(B) 3

(C) 2

(D) 1

**Q12.** `[Concept]` ★ If $\lbrace v_1,\dots,v_n\rbrace$ is a basis of $V$ with dual basis $\lbrace f_1,\dots,f_n\rbrace$, then for every $v\in V$

(A) $v=\sum_i f_i(v)\thinspace v_i$

(B) $v=\sum_i f_i(v_i)\thinspace v$

(C) $v=\sum_i f_1(v)\thinspace v_i$

(D) $v=\sum_i v_i$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | A | Numerical |
| 3 | C | Numerical |
| 4 | D | Multi-Statement |
| 5 | B | Assertion-Reason |
| 6 | D | Match |
| 7 | C | NOT-true |
| 8 | A | Application |
| 9 | C | Concept |
| 10 | B | Numerical |
| 11 | D | Application |
| 12 | A | Concept |

## Solutions
**Q1 — (B).** For finite-dimensional $V$, $\dim V^\ast =\dim V=2\cdot3=6$.

**Q2 — (A).** We need $f_i(v_j)=\delta_{ij}$. Check: $f_1(1,0)=1$, $f_1(1,1)=0$, $f_2(1,0)=0$, $f_2(1,1)=1$. Equivalently, the rows of $`\begin{pmatrix}1&1\cr 0&1\end{pmatrix}^{-1}=\begin{pmatrix}1&-1\cr 0&1\end{pmatrix}`$ give the dual basis. (B) is dual to the *standard* basis.

**Q3 — (C).** The second vector is twice the first, so $\dim W=2$ and $\dim W^0=5-2=3$.

**Q4 — (D).** I and II follow straight from the definitions. III is false: the correct identity is $(W_1\cap W_2)^0=W_1^0+W_2^0$. For example, two distinct lines in $\mathbb R^2$ have intersection $\lbrace 0\rbrace$ with annihilator $V^\ast$, while $W_1^0\cap W_2^0=\lbrace 0\rbrace$.

**Q5 — (B).** Both statements are true. A holds because for infinite-dimensional $V$, $\dim V^{\ast \ast }\gt \dim V$, so $J$ is injective but not onto. R gives injectivity, but injectivity does not explain why $J$ fails to be onto. The explanation is the dimension jump.

**Q6 — (D).** $g\in\ker T^t\iff g\circ T=0\iff g$ vanishes on range $T$. Also $\mathop{\mathrm{range}}\nolimits T^t=(\ker T)^0$, $\dim U^0=\dim V-\dim U$, and the matrix of $T^t$ in the dual bases is the transpose $A^T$.

**Q7 — (C).** $\det(2I)=2^n\ne2\det I$, so $\det$ is not linear (it is multilinear in the rows). The others are linear.

**Q8 — (A).** Pick $v_0$ with $f(v_0)=1$. Then $v-f(v)v_0\in\ker f\subseteq\ker g$, so $g(v)=g(v_0)f(v)$ and $g=cf$ with $c=g(v_0)$. The constant $c$ may be $0$, so (C) and (D) need not hold.

**Q9 — (C).** A non-zero functional has rank 1, so the nullity is $n-1$ and the kernel is a hyperplane.

**Q10 — (B).** $\varphi(1)=1$, $\varphi(x)=\tfrac12$, $\varphi(x^2)=\tfrac13$, and any functional equals $\sum\varphi(v_i)f_i$.

**Q11 — (D).** $\mathop{\mathrm{rank}}\nolimits T^t=\mathop{\mathrm{rank}}\nolimits T=2$, and $T^t$ has a 3-dimensional domain, so nullity $=3-2=1$. Equivalently, $\ker T^t=(\mathop{\mathrm{range}}\nolimits T)^0$ has dimension $3-2$. (C) wrongly uses the domain of $T$.

**Q12 — (A).** Applying $f_j$ to $v=\sum a_iv_i$ gives $a_j=f_j(v)$. So the dual basis returns the coordinates.
