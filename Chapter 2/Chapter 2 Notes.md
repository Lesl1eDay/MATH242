[TOC]

# Chapter 2 Notes

## Overview

$$
\begin{equation}
    \begin{cases}
     Convergence\ for\ sequence\ elements  \\
     Continuity\ for\ function\  \\
     Continuity\ relates\ with\ Convergence
    \end{cases}
\end{equation}
$$

## 2.1. Convergence in metric space

> Definition 2.1.1. — <u>Convergence</u>: $\epsilon$ language
>
> $(X_{n})_{n\in \mathbb{N}}$ converges to $\mathcal{l}\in\mathbb{R}$ if $\forall \epsilon >0$,$\exist N\in\mathbb{N}$, s.t. $\lvert \mathcal{l}-x_{n}\rvert <\epsilon$  $\forall n>\mathbb{N}$

> Definition 2.1.3. 
>
> A sequence of elements of a set ==$X$== is a function $x:\ \mathbb{N}\rightarrow X$ wrote as $x=(x_{n})$

> Definition 2.1.4. — <u>Convergence</u>: metric language
>
> $(X_{n})$ converges to $\mathcal{l}$ in $X$ if $\forall \epsilon>0$, $\exist N\in\mathbb{N}$ s.t. $d(x_{n},\mathcal{l})<\epsilon$ $\forall n>\mathbb{N}$

> Definition 2.1.7. — Ball
>
> Let $(X,d)$ be a metric space, $p\in X$, $R\in\mathbb{R}_{>0}$
>
> Open ball:
> $$
> B_{R}^{\ d}(p)=\set{x\in X:\ d(x,p)<R}
> $$
> Closed ball:
> $$
> \bar{B}_{R}^{\ d}(p)=\set{x\in X:\ d(x,p)\leq R}
> $$
>  Tips: $x\in X$ in both open ball and closed ball

> Definition 2.1.13. — <u>Convergence</u>: Ball language
>
> $(X_{n})$ converges to $\mathcal{l}\in X$ if $\forall \epsilon>0$, $\exist N\in\mathbb{N}$  s.t. $x_{n}\in B_{\epsilon}^{d}(\mathcal{l})$ $\forall N>\mathbb{N}$

> Definition 2.1.15
>
> A sequence $(x_{n})$ in $X$ is *eventually constant* if $\exist \mathcal{l}\in X$ and $\exist N\in\mathbb{N}$ s.t. $x_{n}=\mathcal{l}$ $\forall n>N$

## 2.2. Continuity in metric spaces

> Definition 2.2.1. — <u>Continuity</u>:  $\epsilon-\var$  language
>
> Let $f:\ \mathbb{R}\rightarrow\mathbb{R}$. $f$ is continuous ==at $x_{0}$== if $\forall \epsilon>0$ $\exist\var>0$ s.t.
> $$
> \lvert f(x)-f(x_{0})\rvert=d_{1}(f(x),f(x_{0}))<\epsilon
> $$
> Whenever $\lvert x-x_0\rvert=d_1(x,x_0)<\var$
>
> We say that $f$ is continuous if $f$ is continuous if $f$ is continuous at every $x_0\in\mathbb{R}$
>
> 
>
> Using $lim$,
>
> If $\forall \epsilon>0$, $\exist \var>0$ s.t. 
> $$
> \lvert f(x)-\mathcal{l}\rvert=d_1(f(x),\mathcal{l})<\epsilon
> $$
> Whenever $0<\lvert x-x_0\rvert<\var$, we say that 
> $$
> \underset{x\rightarrow x_0}{lim}f(x)=\mathcal{l}
> $$

> Now extend these definitions to the general case of functions between metric spaces
>
> Definition 2.2.2. — <u>Continuity</u>: functions between metric spaces
>
> Let $(X,d_X)$, $(Y,d_Y)$ be metric spaces. Let $f:\ X\rightarrow Y$ be a function, and let $x_0\in X$. Then we say that $f$ is continuous at $x_0$ if $\forall \epsilon>0$, $\exist\var>0$ s.t.
> $$
> d_Y(f(x),f(x_0))<\epsilon
> $$
> whenever $d_X(x,x_0)<\var$. We say that $f$ is continuous if it is continuous $\forall x_0\in X$ 
>
> Similarly using $lim$,
>
> If $\forall \epsilon>0$, $\exist \var>0$ s.t.
> $$
> d_Y(f(x),\mathcal{l})<\epsilon
> $$
> whenever $0<d_X(x,x_0)<\var$, we say that 
> $$
> \underset{x\rightarrow x_0}{lim}f(x)=\mathcal{l}
> $$

> $f$ is continuous at $x_0$ $\iff$ $\underset{x\rightarrow x_0}{lim}f(x)=f(x_0)$ 

> Remark 2.2.3. — Direct images and Inverse images of a function notation
>
> We have $f: X\rightarrow Y$ and $f(x)\in Y$
>
> Define that for a subset $A\subseteq X$, its <u>direct image</u> (像集):
> $$
> f(A):=\set{y\in Y:\ \exist x\in A\quad s.t.\ f(x)=y}
> $$
> Similarly for a subset $B\subseteq Y$ we define its <u>inverse image/preimage</u> (原像集):
> $$
> f^{-1}(B):=\set{x\in X:\quad s.t.\ f(x)\in B}
> $$
> 由此我们可以==用ball语言来重写连续性的定义==
>
> $f$ is continuous at $x_0$ $\iff$ $\forall \epsilon>0\ \exist\var>0$ s.t. $f(B_{\var}^{d_X}(x_0))\subseteq B_{\epsilon}^{d_Y}(f(x_0))$ 
>
> Where the latter is $d_x(X,X_0)<\var$  $\rightarrow$  $d_Y(f(x),f(x_0))<\epsilon$ 

> Corollary 2.2.6.
>
> If $f$ and $g$ are both continuous, then so is $g\circ f$ 
>
> Tips: 先$f$ 再 $g$

> ==<u>Recast continuity in terms of convergence</u>==(class test 1考过)
>
> Lemma 2.2.7.
>
> Let $(X,d_X)$ and $(Y,d_Y)$ be metric spaces, $f:\ X\rightarrow Y$ a function and $p\in X$. The following are equivalent
> $$
> \begin{equation}
>   \begin{cases}
>     f\ is\ continuous\ at\ p \\
>     \forall (x_n)\subseteq X\ s.t.\ x_n\xrightarrow[]{d_X}p,\ f(x_n)\xrightarrow[]{d_Y}f(p)
>   \end{cases}
> \end{equation}
> $$
> Remark: 这将收敛性与连续性联系了起来

> Remark 2.2.8.
>
> If $f$ is continuous at $p$, by the above we have 
> $$
> f(\underset{n}{lim}\ x_{n})=\underset{n}{lim}f(x_{n})
> $$

