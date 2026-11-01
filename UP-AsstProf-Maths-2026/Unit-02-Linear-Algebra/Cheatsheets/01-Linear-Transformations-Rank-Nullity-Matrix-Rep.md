# Cheatsheet · Unit 2 · Topic 01 — Linear Transformations, Rank–Nullity, Matrix Representation

## 1. Vector space basics
- **Subspace test:** $W\neq\emptyset$ and $au+bv\in W$ for all $u,v\in W$ and all scalars $a,b$.
- The union of two subspaces is a subspace **iff** one of them contains the other. The intersection of subspaces is always a subspace.
- **Basis** = linearly independent spanning set. All bases have the same size, $\dim V$.
- In an $n$-dimensional space, any $n$ independent vectors form a basis, and so do any $n$ vectors that span. A set of more than $n$ vectors is dependent.
- **Dimension formula:** $\dim(U+W)=\dim U+\dim W-\dim(U\cap W)$. Hence $\dim(U\cap W)\ge \dim U+\dim W-n$.
- The sum is direct, $V=U\oplus W$, iff $U+W=V$ and $U\cap W=\lbrace 0\rbrace$.

| Space | Dimension |
|---|---|
| $M_{m\times n}(F)$ | $mn$ |
| symmetric $n\times n$ | $n(n+1)/2$ |
| skew-symmetric $n\times n$ | $n(n-1)/2$ |
| trace-zero $n\times n$ | $n^2-1$ |
| upper triangular $n\times n$ | $n(n+1)/2$ |
| diagonal $n\times n$ | $n$ |
| $P_n$ (polynomials of degree $\le n$) | $n+1$ |
| $\mathbb C^n$ over $\mathbb{R}$ | $2n$ |
| Hermitian $n\times n$ (a **real** space) | $n^2$ |
| $L(V,W)$ | $\dim V\cdot\dim W$ |

## 2. Linear transformations
- $T:V\to W$ is linear iff $T(au+bv)=aT(u)+bT(v)$. Consequently $T(0)=0$, so $x\mapsto x+c$ with $c\ne0$ is **not** linear.
- Linearity depends on the scalar field. $z\mapsto\bar z$ is $\mathbb{R}$-linear but not $\mathbb{C}$-linear.
- $\ker T$ is a subspace of $V$ and $\operatorname{range}T$ is a subspace of $W$.
- $T$ is injective $\iff \ker T=\lbrace 0\rbrace$.
- A linear map is determined by its values on a basis, and those values can be chosen arbitrarily.
- **Algebra of linear maps:** $L(V,W)$ is a vector space. $L(V,V)$ is an algebra under composition, and it is non-commutative when $\dim V\ge2$.

## 3. Rank–Nullity Theorem
For $V$ finite-dimensional and $T:V\to W$ linear:
$$\dim V=\operatorname{rank}T+\operatorname{nullity}T.$$
Consequences:
- An injective $T$ needs $\dim V\le \dim W$, and a surjective $T$ needs $\dim V\ge\dim W$.
- If $\dim V=\dim W\lt \infty$, then injective $\iff$ surjective $\iff$ bijective.
- $\ker T=\operatorname{range}T$ forces $\dim V=2\thinspace \operatorname{rank}T$, so $\dim V$ must be even.
- $T^2=0 \iff \operatorname{range}T\subseteq\ker T$, which gives $\operatorname{rank}T\le n/2$.
- Composition: $\operatorname{rank}(ST)\le\min(\operatorname{rank}S,\operatorname{rank}T)$ and $\operatorname{nullity}(ST)\le \operatorname{nullity}S+\operatorname{nullity}T$.

## 4. Matrix representation
- With ordered bases $\mathcal{B}=\lbrace v_j\rbrace$ of $V$ and $\mathcal{C}=\lbrace w_i\rbrace$ of $W$, the $j$-th **column** of $`[T]_{\mathcal{C},\mathcal{B}}`$ is the coordinate vector $`[T v_j]_{\mathcal{C}}`$.
- Then $`[Tv]_{\mathcal C}=[T]_{\mathcal C,\mathcal B}[v]_{\mathcal B}`$ and $[ST]=[S][T]$, so composition corresponds to matrix product.
- Differentiation $D$ on $P_n$ with basis $\lbrace 1,x,\dots,x^n\rbrace$ is a nilpotent matrix with superdiagonal $1,2,\dots,n$. It has rank $n$, nullity $1$, trace $0$, and $D^{n+1}=0$.

## 5. Change of basis and similarity
- Let $P$ be the matrix whose columns are the new basis vectors $\mathcal{B}'$ written in the old basis $\mathcal{B}$. Then $`[v]_{\mathcal B}=P[v]_{\mathcal B'}`$ and $`[T]_{\mathcal B'}=P^{-1}[T]_{\mathcal B}P`$.
- For $T:V\to W$ with base changes $P$ in $V$ and $Q$ in $W$, the new matrix is $Q^{-1}AP$. This is **equivalence**, and two matrices are equivalent iff they have the same rank.
- **Similar matrices** $B=P^{-1}AP$ share the rank, trace, determinant, characteristic polynomial, minimal polynomial, eigenvalues with their algebraic and geometric multiplicities, and Jordan form.
- They do **not** in general share eigenvectors (these become $P^{-1}v$), symmetry, or entries.

## 6. Standard examples
| Map | Kernel | Range |
|---|---|---|
| Projection $(x,y,z)\mapsto(x,y,0)$ | $z$-axis | $xy$-plane |
| $D$ on $P_n$ | constants | $P_{n-1}$ |
| $A\mapsto A-A^T$ on $M_n$ | symmetric matrices | skew-symmetric matrices |
| $A\mapsto\operatorname{tr}A$ | trace-zero matrices ($\dim n^2-1$) | $F$ |
| Right shift on $\mathbb R^\infty$ | $\lbrace 0\rbrace$ | not onto, so injective $\not\Rightarrow$ surjective in infinite dimensions |

## Exam traps
- In the Rank–Nullity Theorem, the *domain* dimension is the one that splits. The codomain dimension does not appear.
- "Injective $\Leftrightarrow$ surjective" needs equal **finite** dimensions.
- Columns of $[T]$ are the images of the basis vectors (written as columns, not rows), and the order of the basis matters.
- $\dim(U\cap W)$ is only bounded below by $\dim U+\dim W-n$. The upper bound is $\min(\dim U,\dim W)$.
- Equal rank, trace and determinant do **not** imply similarity. Equal rank alone gives only equivalence.
