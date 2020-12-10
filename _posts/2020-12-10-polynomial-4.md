---
title: 数 · 多项式 · 有理函数域
layout: post
tag: 数
---

设$K$是域（为了方便，这里令$K$是无限域）
设$A$为$K$上的多项式函数环，也就是在$Fun(K,K)=Map(K,K)$中的由$id$生成的子环.

> $Fun(K,K):=\\{f:K\rightarrow K\\}$是一个$K$代数，$K$甚至可以看成它的子代数（常函数）.
> 恒同映射$id:f(x)=x$. 单项式函数$f(x)=ax^n$. 多项式函数$f(x)=a_0x^n+\cdots+a_n$.
> $(f+g)(x)=f(x)+g(x)$，$(fg)(x)=f(x)g(x)$.

$Q$是$A$上的有理函数域，\\
(1) 若$f\in Q$，则$f$是定义在$K$上除去最多有限个点之后的集合上的$K$值函数.\\
(2) 存在多项式函数$P,Q$，使得$f(x)=P(x)/Q(x)$在$f$的定义域上成立.\\
结论：$Q$是$A$的商域，$Q$是包含$A$的最小的域，在同构意义下是唯一的.

**定义** 一元有理函数域$K(x)$是$K[x]$的商域，$f\in K(x)$可以写成$P(x)/Q(x)$的形式，$Q(x)$非零.

$K[x]\subset K(x)$.

设$R$是PID，$K$是$R$的商域，则：若$f\in K$，$f=a/s$，则由于$R$也是UFD，$s=up_1^{\alpha_1}\cdots p_r^{\alpha_r}$，
$u\in R^{\times}$，$P_i$是两两不相伴的（标准）不可约元，则存在$b_1,\cdots,b_r$，$f=b_1/p_1^{\alpha_1}+\cdots+b_r/p_r^{\alpha_r}$，
特别地，如果$R$是$ED$，例如$R=K[x]$，$f=q+a'/s$，$N(a')<N(s)$，$f=q+\sum_{j=1}^r\sum_{l=1}^{\alpha_j}\frac{a_{j,l}}{p_j^l}$，
$N(a_{j,l})<N(p_j)$.

**例** 有理函数可积.\\
$\mathbb{R}[x]$中首一不可约多项式只有$x-a$和$x^2+ax+b(a^2-4b<0)$两种（更高次的多项式由于复根成对，必然有一次或二次因子）.\\
设$f(x)$的分母为以下的分解：$Q(x)=\prod_{i=1}^{r_1}(x-a_i)^{\alpha_i}\prod_{j=1}^{r_2}(x^2+b_jx+c_j)^{\beta_j}$.
则任何有理函数都可以唯一地写成以下形式：
$$
f(x)=f_0(x)+\sum_{i=1}^{r_1}\sum_{l=1}^{\alpha_i}\frac{A_{i,l}}{(x-a_i)^l}+\sum_{j=1}^{r_2}\sum_{l=1}^{\beta_j}\frac{B_{j,l}x+C_{j,l}}{(x^2+b_jx+c_j)^l}.
$$
