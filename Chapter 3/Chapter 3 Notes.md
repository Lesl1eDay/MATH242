[TOC]

# Chapter 3 Notes

## Overview

> $$
> \begin{equation}
> \begin{cases}
> Open\ and\ closed\ subset\ of\ a\ metric\ space \\
> Formal\ properties\ of\ open\ subsets \\
> Closed\ sets\ by\ convergence\ of\ sequences \\
> Convergence/Continuity\ using\ open\ sets \\
> Equivalence\ for\ two\ distances \\
> Homeomorphism \\
> \end{cases}
> \end{equation}
> $$
>

## 3.1. Open sets and closed sets

### Definition for open sets and closed sets

> Definition 3.1.1.
>
> Let $(X,d)$ be a metric space, and let $A\subseteq X$. 
>
> Open: we say that $A$ is open in $(X,d)$ if $\forall p\in A$, $\exist \epsilon>0$, s.t. $B_{\epsilon}(p)\subseteq A$.
>
> Closed: If $B\subseteq X$ then we say that B is closed in $(X,d)$ if $X\backslash B$ is open.
>
> 一般的开集证明思路: 证明所证集内的任一元素的任一开球内的元素都在所证集中. i.e. 所证集内任一元素的任一开球是所证集的子集.

### Formal properties of open sets

> Lemma 3.1.4 — Open sets properties 
>
> Let $(X,d_{X})$ be a metric space.
>
> 1.  The subsets $\empty$ and $X$ are open
> 2.  An arbitrary union of open sets is open (任意并)
> 3.  A finite intersection of open sets is open (有限交)
>
> About closed sets:
>
> 1.  The subsets $\empty$ and $X$ are closed 
> 2.  The arbitrary intersection of closed sets is closed  (任意交)
> 3.  A finite union of closed sets is closed (有限并) 

### Closed sets by  the convergence of sequences

> Lemma 3.1.8.
>
> Let $(X,d)$ be a metric space, and let $A\subseteq X$. Then,
>
> The subset A is closed $\iff$ $\forall (x_{n})$ of $A$, if $(x_{n})$ converges to $\mathcal{l}\in X$ then $\mathcal{l}\in A$. 

## 3.2. Topology 

> Definition 3.2.1. 
>
> A topology $\mathcal{U}$ on $X$ is a collection of subsets $\mathcal{U}_{i}$ of $X$, called the <u>open subsets</u> of $X$ (开子集族), that satisfies the following properties.
>
> ($T_{1}$) The subsets $\empty$ , $X\in \mathcal{U}$
>
> ($T_{2}$) If  $\mathcal{U}_{i}\in \mathcal{U}$ for all $i\in I$ $\implies$ $\bigcup_{i\in I}\mathcal{U}_{i}\in \mathcal{U}$ (任意并)
>
> ($T_{3}$) If $\mathcal{U}_{1},...,\mathcal{U}_{N}\in \mathcal{U}$ $\implies$ $\bigcap_{i=1}^{N}\mathcal{U}_{i}\in\mathcal{U}$ (有限交)

> Remark 3.2.5.
> $$
> \begin{equation}
>   \begin{cases}
>   Discrete\ topology\ \mathscr{P}(X) \\
>   Trivial\ topology\ \mathcal{U}=\set{\empty,X}
>   \end{cases}
> \end{equation}
> $$

### Convergence/Continuity in topological terms

> Theorem 3.2.8. — <u>Convergence</u>
>
> Let $(X,d)$ be a metric space, $(x_{n})$ a sequence of $X$, and let $\mathcal{l}\in X$. Then the following are equivalent: 
>
> 1. $(x_{n})$ converges to $\mathcal{l}$
> 2.  $\forall$ <u>open subset</u>  $\mathcal{U}\subseteq X$ with $\mathcal{l}\in\mathcal{U}$, $\exist N\in\mathbb{N}$  s.t. $(x_{n})\in\mathcal{U}\quad \forall n>N$
>
> Tips: 当收敛时$(x_{n})$只有有限多的项在$\mathcal{U}$外面

> Theorem 3.2.9. — <u>Continuity</u>
>
> Let $(X,d_{X})$ and $(Y,d_{Y})$ be metric spaces, and let $f:\ X\rightarrow Y$. Then the following are equivalent.
>
> 1. $f$ is continuous.
> 2. $\forall$ <u>open set</u>  $\mathcal{U}\subseteq Y$, the *inverse image* $f^{-1}(\mathcal{U})$ is open in $X$.
>
> Remark 3.2.10.
>
> $\forall$ open subset  $\mathcal{U}\subseteq Y$, $f^{-1}(\mathcal{U})$  is open $\iff$ $\forall$ closed set $C\subseteq Y$, $f^{-1}(C)$  is closed.
>
> Tips: 上述的闭集用开集表示即可.

## 3.3. Equivalent distances

### Equivalence for two distances

> Two distances are equivalent if the notions of convergence and continuity defined using one are the same as those defined using the other. (上面使用了<u>开集</u>来定义度量空间内收敛性与连续性)

> Definition 3.3.1.
>
> Let $X$ be a set. Let $d,d'$ be two different distances on $X$. Then we say that $d$ and $d'$ are equivalent whenever the <u>open sets</u> of $(X,d)$  <u>coincide</u> with those of $(X,d')$ . We write $d \sim d’$  to denote that two distances are equivalent.
>
> Tips: 即开集表示一致.

> Corollary 3.3.2. — Convergence
>
> Let $(X,d)$ and $(X,d')$ be metric spaces with $d\sim d'$, and let $(x_{n})$ be sequence of $X$ and $\mathcal{l}\in X$. Then we have 
> $$
> (x_{n})\xrightarrow[]{d}\mathcal{l}\iff (x_{n})\xrightarrow[]{d'}\mathcal{l}
> $$
> Corollary 3.3.3. — Continuity
>
> Let $(X,d_X)$, $(X,d'_X)$ and $(Y,d_Y)$, $(Y,d'_Y)$ be metric spaces where $d_X\sim d'_X$ and $d_Y\sim d'_Y$. Then
> $$
> \underbrace{f:\ (X,d_X)\rightarrow (Y,d_Y)}_{is\ continuous}\iff\underbrace{f:\ (X,d'_X)\rightarrow(Y,d'_Y)}_{is\ continuous}
> $$

> Lemma 3.3.5. 
>
> Let $(X,d)$, $(X,d')$ be metric spaces on the same underlying set. Suppose $\forall x,y$, $\exist C>0$, s.t.
> $$
> d(x,y)\leq C\cdot d'(x,y)
> $$
> Then,
> $$
> \mathcal{U}\subseteq(X,d)\ open\implies\mathcal{U}\subseteq(X,d')\ open
> $$
> Corollary 3.3.6. — <u>Give an easy sufficient condition for two distances to be equivalent</u>
>
> According to the lemma above, if $\forall x,y\in X$, $\exist C,C'>0$, s.t.
> $$
> d(x,y)\leq C\cdot d'(x,y)\quad and\quad d'(x,y)\leq C'\cdot d(x,y)
> $$
> Then according to definition 3.3.1., $d$ is equivalent to $d’$.

> From Chapter 1, if $p\neq q$, then $(\mathbb{R}^{n},d_{p})$ and $(\mathbb{R},d_{q})$ are *not isometric*.
>
> Corollary 3.3.7. — equivalence for $d_p$ and $d_q$
>
> On $\mathbb{R}^{n}$, the distances $d_p$ and $d_q$ are equivalent $\forall p,q\geq1$ including $p,q=\infty$.

> The case of the space of functions $C[0,1]$ and two distances $d_{L^1}$ and $d_{L^{\infty}}$:
>
> Lemma 3.3.8.
>
> The inequality $d_{L^{1}}(f,g)\leq d_{L^{\infty}}(f,g)$ holds $\forall f,g\in C[0,1]$.
>
> Remark 3.3.9.
>
> The distance $d_{L^{1}}$ and $d_{L^{\infty}}$ are not equivalent.

> Remark 3.3.12.
>
> For $p\geq1$, the space of sequences $\mathcal{l}^p$ can be endowed with distances $d_q$ and $d_{q'}$  $\forall p\leq q<q'$. These two distances are <u>not equivalent</u>.

## 3.4. Homeomorphisms

> Definition 3.4.1. — 集到集的双连续映射
>
> Let $(X,d_X)$, $(Y,d_Y)$ be metric spaces. We say that $f:\ X\rightarrow Y$ is a homeomorphism when
>
> 1. $f$ is bijective 
> 2. Both $f$ and $f^{-1}$ are continuous
>
> We say that the two metric spaces are homeomorphic when there exists such a $f$.
>
> $f$ 可以将$(X,d_X)$中的开集通过映射:
> $$
> \mathcal{U}\rightarrow f(\mathcal{U}),\quad \mathcal{V}\rightarrow f^{-1}(\mathcal{V})
> $$
> 来得到$(Y,d_Y)$中的开集.

> Example 3.4.2. 
>
> Let $f:\ (X,d_X)\ \rightarrow\ (Y,d_Y)$ be an isometry, then $f$ is a homeomorphism.

