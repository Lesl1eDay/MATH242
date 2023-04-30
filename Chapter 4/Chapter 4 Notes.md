[TOC]

# Chapter 4 Notes

> Overview
> $$
> \begin{equation}
>   \begin{cases}
>     Cauchy\ sequence \\
>     Completeness \\
>     CMT \\
>     Comapact\ metric\ space \\
>     Compactness\ properties \\
>     Compact\ subsets \\
>     Compact\ implies\ complete\\
>   \end{cases}
> \end{equation}
> $$

## 4.0.最小上界定理

> Theorem 4.0.1. — LUB定理
>
> 实数非空子集有上界，则它有最小上界$\implies$实数完备性
>
> 这个定理对于度量空间的推广并不可行，所以用柯西收敛来定义完备.

## 4.1. Cauchy convergence and completeness

### Cauchy sequence and convergence

> 为了用不依赖极限值 $\mathcal{l}\in X$ 的表示法来定义收敛性，遂引入柯西收敛这一只依赖于$(x_n)$序列中元素的表示法.
>
> Definition 4.1.1. 
>
> Let $(X,d)$ be a metric space and let $(x_n)$ be a sequence of $X$. We say that it is *Cauchy convergent* (or just *Cauchy*) if $\forall \epsilon>0$, $\exist N\in\mathbb{N}$  s.t. $d(x_n,x_m)<\epsilon$  $\forall n,m>N$
>
> Lemma 4.1.2.
> $$
> (x_n)\ converges\ \implies\ (x_n)\ is\ Cauchy
> $$
> 然而，反之却不一定成立.
>
> Tips: 前面提到，收敛值 $\mathcal{l}$ 必须满足 $\mathcal{l}\in X$ (<u>收敛值要在集内</u>). 所以柯西收敛有时不一定收敛. 但是，若收敛，则无论收敛值是否在$X$内，一定柯西收敛. 

### Cauchy convergence and completeness

> Definition 4.1.4. — 完备性的定义
>
> A metric space $(X,d)$ is *complete* if <u>every Cauchy sequence</u> *converges*.
>
> Tips: 提到收敛，收敛值必须在$X$中.

> Theorem 4.1.6 — <u>Completeness and closed</u>
>
> Let  $(X,d)$ be a metric space, and $A\subseteq X$ be a subset, and let $d_A$ be the distance induced by $d$ on the subset $A$. 
>
> 1. If $(A,d_A)$ is *complete*, then $A$ is *closed* in $(X,d_X)$
> 2. If $(X,d)$ is *complete* and $A$ is *closed* in $(X,d_X)$, then $(A,d_A)$ is also *complete*.
>
> $(X,d_X)$ is complete and $Y\subset X$, then $(Y,d_X)$ is complete $\iff$ $Y\subset X$ is closed 

> Remark 4.1.7. 
>
> 同胚的两个度量空间，其中一个是完备的不一定意味着另一个也是完备的.
>
> 例如： $((-\pi/2,\pi/2),d_1)$ 与 $(\mathbb{R},d_1)$ 同胚，但后者完备，前者不完备.

## 4.2. Completeness of $\mathbb{R}^N$

> In order to prove $(\mathbb{R}^N,d_p)$ is a complete metric space ($p=\infty$ is accepted).

## 4.3. The contraction mapping theorem (CMT)

> Definition 4.3.1. — ==不动点==
>
> Let $X$ be a set, $f:\ X\rightarrow X$  a function and let $p\in X$. We say that $p$ is a fixed point if $f(p)=p$.

> Definition 4.3.3. — ==压缩映射==
>
> Let $(X,d)$ be a metric space. Then $f:\ X\rightarrow X$  is a *contraction* when $\exist$ $constant\ L\in [0,1)$ s.t. $d(f(x),f(y))\leq L\cdot d(x,y)$ $\forall x,y\in X$.
>
> Theorem 4.3.4. — ==CMT== 
>
> Suppose $(X,d)$ is a *complete* metric space. If $f:\ (X,d)\rightarrow (X,d)$  is a *contraction*, then $f$ has a *unique fixed point*.
>
> Lemma 4.3.7.
>
> 压缩映射 $f$ 是连续的.
>
> Tips: CMT证明过程大致是：
>
> 1. 用反证法来证明不动点的唯一性.
> 2. 为了证明不动点的存在，任取$x_0\in X$, 递归定义$x_{n+1}=f(x_n)$, $n=0,1,2,\cdots$. 后证$d(x_{n+1},x_n)\leq L^nd(x_1,x_0)$, 并推导出 $(x_n)^{\infty}_{n=0}$ 是柯西列，且该柯西列极限为 $f$ 的不动点.
> 3. ==Remark 4.3.9.== 
>    证明过程中，有，
>    $$
>    d(x_n,x_m)\leq d(x_1,x_0)\cdot \frac{L^m}{1-L}
>    $$
>    So, take $n\rightarrow \infty$,
>    $$
>    d(\mathcal{l},x_m)\leq d(x_1,x_0)\cdot\frac{L^m}{1-L}
>    $$
>    $\forall x\in X$, 总有充分大的$m$, s.t.  $\forall \varepsilon>0$,
>    $$
>    d(f(x),x)\cdot\frac{L^m}{1-L}<\varepsilon
>    $$
>    这阐述了 $f^{m}(x)$ 序列向极限值不动点 $\mathcal{l}$ 逼近的性质.
>
> Tips: 4.3.3. 中，是不能有 $L=1$ 的 (有些教材就 $L=1$ 的情况称$f$为压缩映射，就 $L\in [0,1)$ 的情况称$f$为严格压缩映射）.

> Lemma 4.3.6. — ==单变量实值函数是压缩映射的准则==
>
> Let $f:\ [a,b]\rightarrow [a,b]$ be *differentiable* with $ \lvert f'(x)\rvert \leq L<1$  $\forall x\in[a,b]$. Then $f$ is a *contraction* when $[a,b]$ is endowed with the distance $d_1$.
>
> 证明由中值定理所得.

## 4.4. Compactness

> Definition 4.4.1. — subsequence 子列的概念
>
> Let $(X_n)$ be a sequence in $X$. Let $(n_k)_{k\in\mathbb{N}}$ be a strictly increasing sequence of natural numbers. We say that $(x_{n_k})_{k\in\mathbb{N}}$ is a *subsequence* of $(x_n)_{n\in\mathbb{N}}$.
>
> 如果$(X,d)$中的序列$(x_n)$收敛于$\mathcal{l}$，那么其子列也同样收敛于$\mathcal{l}$.

### Compactness Definition

> Definition 4.4.2. — 紧致性的定义
>
> We say that a metric space $(X,d)$ is <u>*compact*</u> if every sequence admits a convergent subsequence.(当且仅当$(X,d)$中的每一个序列都至少有一个收敛子列.)

### Compactness Properties

> Proposition 4.4.5.
>
> If $X\subseteq(\mathbb{R},d_1)$ is s.t. $(X,d_1)$ is *compact*, then $X$ has a *maximum* and a *minimum*.
>
> Tips: 
>
> 1. 先证有界.
> 2. 再利用紧致性证明上确界在 $X$ 中.
>
> Corollary 4.4.8.
>
> Suppose $(X,d_X)$ is *compact*, and that $f:X\rightarrow\mathbb{R}$ is *continuous* (with the distance $d_1$ on $\mathbb{R}$). Then $f$ has a *minimum* and a maximum.

> Theorem 4.4.6. Key Result — 连续映射保持紧致性
>
> If $f:(X,d_X)\rightarrow (Y,d_Y)$ is a *continuous* function, if $(X,d_X)$ is *compact*, then so is $(f(X),d_Y)$.
>
> 证明: $f(x_{n_k})\rightarrow f(\mathcal{l})$, 再用紧致性定义叙述即可.

> Corollary 4.4.7. ==紧致性是一种拓扑性质==
>
> If $(X,d_X)$ is *homeomorphic* to $(Y,d_Y)$ then,
> $$
> (X,d_X)\ is\ compact\iff (Y,d_Y)\ is\ compact
> $$
> 如果这里的‘’*紧致*‘’ 换成 ‘’*完备‘’*，则不成立.

### Compactness for subsets of $\mathbb{R}^N$ 

> Question: 什么样的$(\mathbb{R},d_1)$ 的度量子空间是紧致的？
>
> Lemma 4.4.10 
>
> Let $(X,d)$ be a metric space. Suppose that $C\subseteq X$ and $(C,d)$ is *compact*. Then $C$ is a *closed subset* of $(X,d)$.
>
> 证明: 若不是闭子集，则存在序列不收敛于$C$（序列收敛于$L$, 则其每一子列也收敛于$L$ ), 则其不紧致，与紧致前提矛盾.
>
> Theorem 4.4.11 — Bolzano-Weierstrass Theorem
>
> Let $X\subseteq (\mathbb{R},d_1)$. Then,
> $$
> (X,d_1)\ is\ compact\iff X\ is\ closed\ and\ bounded
> $$
> Proof: 同名定理：每一有界序列都有收敛子列.
>
> Theorem 4.4.12. 上述定理的多维推广
>
> $(\mathbb{R}^N,d_p)$ 的紧致子集是有界闭子集.（if and only if )
>
> Definition 4.4.13. $\mathbb{R}^N$上有界的定义
>
> $X\subseteq\mathbb{R}^N$ is bounded if there exists an $R>0$ s.t. $X\subseteq B_R(0)$.

### Compactness and completeness

> Lemma 4.4.17.
>
> Let $(X,d)$ be a metric space. Suppose $(x_n)$ is a *Cauchy sequence* and a *subsequence* $(x_{n_k})$ *converges* to $\mathcal{l}$ . Then $(x_n)$ *converges* to $\mathcal{l}$ .
>
> Corollary 4.4.18.
>
> A compact metric space is complete.
>
> 相反叙述是错误的.





