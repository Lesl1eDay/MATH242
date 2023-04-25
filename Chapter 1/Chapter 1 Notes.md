[TOC]

# Chapter 1 Notes

## 1.1. Starting out

> <u>4 axioms for metric:</u>
>
> (M0): non-negative
>
> (M1): $\forall x,y\in X$, $d(x,y)=0$ if and only if $x=y$
>
> (M2): Symmetry
>
> (M3): Triangle inequality: $\forall x,y,z\in X$, $d(x,z)\leq d(x,y)+d(y,z)$

> Lemma 1.1.6
>
> $\max(a+b,c+d)\leq \max(a,c)+\max(b,d)$

> ==Cauchy-Schwarz Inequality==
>
> $\forall a_{1},\cdots,a_{n},b_{1},\cdots,b_{n}$$\in \mathbb{R}$, the following inequality holds:
> $$
> (\sum_{i=1}^{n}a_{i}b_{i})^{2}\leq \sum_{i=1}^{n}a_{i}^{2}\cdot \sum_{i=1}^{n}b_{i}^{2}
> $$

> $d_{\infty}$ for $\mathbb{R}^{n}$: 
> $$
> d_{\infty}(x,y)=\underset{1\leq i\leq n}{max}\lvert x_{i}-y_{i}\rvert
> $$
> $d_{p}$ for $\mathbb{R}$: 
> $$
> d_{p}(x,y)=(\sum_{i=1}^{n}\lvert x_{i}-y_{i}\rvert^{p})^{\frac{1}{p}}
> $$

> *discrete distance*
> $$
> d_{discr}(x,y)=
> \left\{
>    \begin{array}{lc}
>        0 & x=y \\
>        1 & x\neq y \\
>    \end{array}
> \right.
> $$

## 1.2. Subspace distance

> We can just measure distances on the subset using the global distance defined on the larger metric space

## 1.3. Spaces of real sequences

> To extend our definition of distance $d_{p}$ to spaces whose elements are sequences,
> $$
> d_{p}(A,B)=(\sum_{n=0}^{\infty}\lvert A_{n}-B_{n}\rvert^{p})^{\frac{1}{p}}=\underset{N\rightarrow \infty}{lim}(\sum_{n=0}^{N}\lvert A_{n}-B_{n}\rvert^{p})^{\frac{1}{p}}
> $$
> and
> $$
> d_{\infty}((A_{n}),(B_{n}))=\underset{n\in\mathbb{N}}{sup}\lvert A_{n}-B_{n}\rvert
> $$

> By definition, a distance is required to be a non-negative real number, which $+\infty$ is not.
>
> Thus, we define $\mathcal{l}^{p}$ and $\mathcal{l}^{\infty}$ sequence space:
> $$
> \mathcal{l}^{p}=\set{(A_{n})\vert\ \sum_{n=0}^{\infty}\lvert A_{n}\rvert^{p}<\infty}
> $$
>
> $$
> \mathcal{l}^{\infty}=\set{(A_{n})\vert \ (A_{n})\ is\ bounded}
> $$
>
> We say $(A_{n})$ is bounded if $\exist M\in \mathbb{R}$ s.t. $\lvert A_{n}\rvert \leq M$$,\ \forall n\in \mathbb{N}$

> <u>Theorem 1.3.4.</u>
>
> $\forall p\geq 1$ ( and also for $p=\infty$) the function $d_{p}$ defines a distance on the set $\mathcal{l}^{p}$

> <u>Proposition 1.3.5.</u>
>
> For $p\leq q$, the inclusion $\mathcal{l}^{p}\subseteq \mathcal{l}^{q}$ holds ( and this inclusion also holds when  $q=\infty$)
>
> <u>Corollary 1.3.6.</u>
>
> $(\mathcal{l}^{p},d_{q})$ is a metric space ( a metric subspace of $(\mathcal{l}^{q},d_{q})$) whenever $p\leq q$

> ==Theorem 1.3.10 — 闵可夫斯基不等式==
> $$
> (\sum_{n=0}^{\infty}\lvert A_{n}+B_{n}\rvert^{p})^{\frac{1}{p}}\leq(\sum_{n=0}^{\infty}\lvert A_{n}\rvert^{p})^{\frac{1}{p}}+(\sum_{n=0}^{\infty}\lvert B_{n}\rvert^{p})^{\frac{1}{p}}\tag{1}
> $$
> where $p\geq 1$
>
> Tips: when p=2, (1) is Cauchy-Schwarz inequality

## 1.4. Spaces of functions 

> Definition 1.4.1 
> $$
> C[0,1]:=\set{f:[0,1]\rightarrow \mathbb{R}\quad s.t.\ f\ is\ continuous}
> $$

> Metric on $C[0,1]$
>
> Definition 1.4.2.
> $$
> d_{L^{1}}(f,g)=\int_{0}^{1}\lvert f(x)-g(x)\rvert dx
> $$
>
> $$
> d_{L^{\infty}}(f,g)=\underset{x\in [0,1]}{max}\lvert f(x)-g(x)\rvert
> $$

## 1.5. Product metrics

> <img src="C:\Users\Alienware\OneDrive\桌面\Typora\MATH242\Chapter 1\Product Spaces Metric.jpg" style="zoom: 40%;" />

## 1.6. Isometries 

> Definition 1.6.1.
>
> An *isometry* from $(X,d_{x})$ to $(Y,d_{Y})$ is a function $\phi:X\rightarrow Y$ s.t. 
>
> (1) $\forall x_{1},x_{2}\in X, d_{Y}(\phi(x_{1}),\phi(x_{2}))=d_{x}(x_{1},x_{2})$
>
> (2) $\phi\ is\ surjective$

> Lemma 1.6.2
>
> An isometry is *injective*

> Definition 1.6.3.
>
> Two metric spaces $(X,d_{x}),(Y,d_{Y})$ are *isometric* if there <u>exists an isometry</u> $\phi:(X,d_{x})\rightarrow(Y,d_{Y})$

