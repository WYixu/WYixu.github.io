---
title: 数 · 多项式 · 对称多项式
layout: post
tag: 数
---

**定义** 设$f(x_1,\cdots,x_n)\in R[x_1,\cdots,x_n]$，$\sigma\in S_n$，则$(\sigma f)(x_1,\cdots,x_n):=f(x_{\sigma(1)},\cdots,x_{\sigma(n)})$.

**对称多项式** 若$f\in R[x_1, \cdots, x_n]$满足$\forall\sigma\in S_n$，$(\sigma f)=f$，则称$f$为对称多项式.

例子：$s_r(x_1,\cdots,x_n)=x_1^r+\cdots+x_n^r$是$r$次齐次对称多项式，$p(x_1,\cdots,x_n)=x_1\cdots x_n$也是对称多项式.

**韦达定理** 设$f(x)=x^n+a_1x^{n-1}+\cdots+a_n\in K[x], n\in\mathbb{N}$，不妨设$K$是代数封闭域，$f(x)$有根$\alpha_1,\cdots,\alpha_n$(计重数).
则$a_i=(-1)^i\sum_{1\le j_1<\cdots<j_i\le n} \alpha_{j_1}\cdots\alpha_{j_i}$.

**初等对称多项式** $\sigma_s(x_1,\cdots,x_n)=\sum_{1\le j_1<\cdots<j_s\le n} x_{j_1}\cdots x_{j_s}$称为关于变元$x_1,\cdots,x_n$的第$s$个基础对称多项式.

$\sigma_s$是$s$次齐次对称多项式，有${n\choose s}$项.

**命题** 设$f\in R[x_1,\cdots,x_n]$是对称多项式，则$\exists h\in R[Y_1,\cdots,Y_n]$满足：
$$
f(x_1,\cdots,x_n)=h(\sigma_1(x_1,\cdots,x_n),\cdots,\sigma_n(x_1,\cdots,x_n)).
$$
例如，$x_1^2+\cdots+x_n^2=\sigma_1^2-2\sigma_2$.

**证明**\\
先引入字典排序，$\mathbb{Z_{\ge0}}^n$的字典排序是$(a_1,\cdots,a_n)\ge(b_1,\cdots,b_n)$当且仅当存在$1\le d\le n$使得
$a_i=b_i$对$1\le i < d-1$成立，且$a_d\ge b_d$. 单项式$x_1^{\alpha_1}\cdots x_n^{\alpha_n}$的次数比$x_1^{\beta_1}\cdots x_n^{\beta_n}$高
当且仅当$(\alpha_1,\cdots,\alpha_n)\ge(\beta_1,\cdots,\beta_n)$（有时要求先比较总次数，再比较字典序）.\\
约定：$\underline{\alpha}=(\alpha_1,\cdots,\alpha_n), \underline{x}^\underline{\alpha}=x_1^{\alpha_1}+\cdots+x_n^{\alpha_n}$.
$\underline{\beta}\sim \underline{\alpha}$当且仅当$\underline{\beta}$是$\underline{\alpha}$的重排.
$F_{\underline{\alpha}}=\sum_{\underline{\beta}\sim\underline{\alpha}}\underline{x}^{\underline{\beta}}$.\\
这个问题归结为：存在$g_\alpha\in R[Y_1,\cdots,Y_n]$，$F_\underline{\alpha}=g_\alpha(\sigma_1,\cdots,\sigma_n)$.
因为任何对称多项式都能表示成一系列$F_\underline\alpha$的和.\\
设$g(Y_1,\cdots,Y_n)=Y_1^{r_1}\cdots Y_n^{r_n}$，则$g(\sigma_1,\cdots,\sigma_n)=\sigma_1^{r_1}\cdots \sigma_n^{r_n}$是关于
$x_1,\cdots,x_n$的齐次多项式，其次数为$r_1+2r_2+\cdots+nr_n$. 因此，若$f(x_1,\cdots,x_n)$为$d$次齐次多项式，并且
$f(x_1,\cdots,x_n)=g(\sigma_1,\cdots,\sigma_n)=\sum c_\underline{r} \sigma_1^{r_1}\cdots \sigma_n^{r_n}$，则和式中仅包括
$r_1+2r_2+\cdots+nr_n=d$的项.\\
对于给定的次数，利用字典排序法，在所有的$d$次单项式中，次数最高的是$x_1^d$. 令$\underline{\alpha}=(\alpha_1,\cdots,\alpha_n),\alpha_1\ge\cdots\ge\alpha_n$，
则$\underline{\alpha}$是所有$\underline{\beta}\sim\underline{\alpha}$中次数最高的（称其为*支配*的），因而$F_{\underline{\alpha}}$
的首项$LT(F_{\underline{\alpha}})=\underline{x}^\underline{\alpha}$，
$F_\underline{\alpha}$也是首一的. 设$h_1,h_2\in R[x_1,\cdots,x_n]$首一，则$LT(h_1h_2)=LT(h_1)LT(h_2)$. 特别地，
设$\underline{\alpha}=(\alpha_1,\cdots,\alpha_n),\alpha_1\ge\cdots\ge\alpha_n$，$\underline{\beta}$满足
$\beta_n=\alpha_n, \beta_j=\alpha_j-\alpha_{j-1}$，则$g_\underline{\beta}=\sigma_1^{\beta_1}\cdots \sigma_n^{\beta_n}$
的首项是$\underline{x}^\underline{\alpha}$.\\
综上，设$f(x_1,\cdots,x_n)$是$d$次齐次对称多项式，其首项为$a\underline{x}^\underline{\alpha}$，则存在$\underline{\beta}$
满足$LT(\underline{\sigma}^\underline{\beta})=\underline{x}^\underline{\alpha}$. 则$f-a\underline{\sigma}^\underline{\beta}$的首项次数严格下降.
不断进行此操作，必有终止，且最终得到$f$的一个用基础多项式表示的形式.

**Newton公式** 考察对称多项式$s_r(x_1,\cdots,x_n)=x_1^r+\cdots+x_n^r$，有
$$
s_d+\sum_{j=1}^d (-1)^{j}\sigma_{j}s_{d-j}=0 (1\le d\le n);\\
s_d+\sum_{j=1}^n (-1)^{j}\sigma_{j}s_{d-j}=0 (d\ge n).
$$

**同构性** 考虑$S_n$作用在$R[x_1,\cdots,x_n]$上，则$R[x_1,\cdots,x_n]^{S_n}$是对称多项式的集合，也是$R[x_1,\cdots,x_n]$的子环，
由$\sigma_1,\cdots,\sigma_n$生成（作为$R$子代数）. 实际上，$R[x_1,\cdots,x_n]^{S_n}\cong R[Y_1,\cdots,Y_n],Y_i\mapsto \sigma_i$. （这是一个多元多项式环的自同构）

**交错多项式** 若$f\in R[x_1, \cdots, x_n]$满足$\forall\sigma\in S_n$，$(\sigma f)=sgn(\sigma)f$，则称$f$为斜对称/反对称/交错多项式.

交错多项式的和是交错多项式，交错多项式的积是对称多项式，对称多项式乘交错多项式是交错多项式.

**例** 范德蒙行列式$A(x_1,\cdots,x_n)=\prod_{1\le i<j\le n}(x_j-x_i)$是交错多项式.

设$f(x)=(x-\alpha_1)\cdots(x-\alpha_n)=x^n+\sum_{j=1}^n a_jx^{n-j}$，则$A(\alpha_1,\cdots,\alpha_n)^2=\prod_{1\le i<j\le n}(\alpha_j-\alpha_i)^2$
是对称多项式，因而它可以写成$g(\sigma_1,\cdots,\sigma_n)$的形式，其中$\sigma_i=(-1)^ia_i$（韦达定理）. 记$D(f)=g(-a_1,\cdots,(-1)^na_n)$，它是关于$f$的系数的整系数多项式，称为$f$的*判别式*.

**命题** 反对称多项式总可以写成对称多项式和范德蒙行列式的乘积.\\
**证明** 对于$R=\mathbb{Z}$（或者是UFD）的情况，设$f(x_1,\cdots,x_n)$是交错多项式，则$(x_j-x_i)\mid f(x_1,\cdots,x_n),i<j$，因为把$f$看作关于$x_j$的多项式，
每个$x_i$都是$f$的一个根. 在UFD上，$f$是范德蒙行列式的倍数，$f=f_0A$，则$f_0$显然是对称的.
