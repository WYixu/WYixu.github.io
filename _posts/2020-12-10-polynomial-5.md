---
title: 数 · 多项式 · 多元多项式代数
layout: post
tag: 数
---

**定义** 多元多项式代数\\
设$R$是交换幺环，$x_1,\cdots,x_n$是变元，则$R[x_1,\cdots,x_n]\cong R[x_1,\cdots,x_{n-1}][x_n]$.\\
方幂形式：$x_1^{\alpha_1}\cdots x_n^{\alpha_n}$；单项式$cx_1^{\alpha_1}\cdots x_n^{\alpha_n}$.

例子 $x+y,xy$都是$R$上的多元多项式.

单项式$cx_1^{\alpha_1}\cdots x_n^{\alpha_n}$的次数是$(\alpha_1,\cdots,\alpha_n)\in\mathbb{Z_{\ge0}}^n$，
其中它对变元$x_i$的次数$deg_{x_i}=\alpha_i$，它的总次数$deg=\alpha_1+\cdots+\alpha_n$，$c$是在$(\alpha_1,\cdots,\alpha_n)$次上的系数.

设$f(x)=a_0(x_1,\cdots,x_n-1)x_n^d+\cdots+a_n(x_1,\cdots,x_n-1)$，则$f$对变元$x_n$的次数是$d$.

另外一种定义（可以推广为幂级数）是$f\in R[x_1,\cdots,x_n]$可看成是$c:\mathbb{Z_{\ge 0}}^n\rightarrow R, \underline{d}=(d_1,\cdots,d_n)\mapsto c_{\underline{d}}$，
并且$c$只在有限个点上不为零.

**命题** 若$R$是整环，则$R[x_1,\cdots,x_n]$也是整环.\\
$deg(f+g)\le max(deg(f),deg(g))$对一般的$R$都成立；$deg(fg)\le deg(f)+deg(g)$，当$R$是整环的时候等号成立. （$deg$在这里既代表总次数也代表各项次数）

**定义** 齐次多项式. $d$次齐次多项式是$d$次单项式的组合，
$f=\sum_{i=1}^r c_ix_1^{\alpha_1,i}\cdots c_ix_r^{\alpha_r,i},\alpha_{1,i}+\cdots+\alpha_{r,i}=d$.

任何$f$都可以唯一地写成以下形式：$f=f_0+\cdots+f_d,d=deg(f)$，$f_i$是$i$次齐次多项式，称为$f$的$i$次齐次部分.

**泛性质** 设$R$是交换幺环，$A$是$R$代数，$a_1,\cdots,a_n\in A$两两交换，则存在唯一的$R$代数同态$\phi:R[x_1,\cdots,x_n]\rightarrow A$，
满足$\phi(x_i)=a_i$.

**多元有理函数域**$K(x_1,\cdots,x_n)$是$K[x_1,\cdots,x_n]$的商域.

$K[x_1,\cdots,x_n]$不是PID，ED，但仍是UFD.

设$A=(a_{ij})\_{m\times n}$，$det(A)$看作$a_{ij}$的多项式，$det(A)$对每个变元的次数都是一，是$n$次齐次多项式且不可约.

$f,g\in K[x_1,\cdots,x_n]$，$g$$m$次齐次，则$g\mid f\Rightarrow g\mid f_d(\forall d\in \mathbb{Z})$.

**命题** 齐次多项式的不可约因子仍是齐次多项式.\\
**证明**  首先，$g\mid f\Rightarrow g_{deg(g)}\mid f_{deg(f)}$. 这样，若$f$齐次可约，则$f$必有一次数更低的齐次因子.

设$R$是交换幺环，$A$是交换的$R$代数，$S\subset A$，则$S$生成的$R$子代数$R\<S\>=\\{f(a_1,\cdots,a_r),f\in R[x_1,\cdots x_r],r\in\mathbb{N},a_i\in S\\}$.
特别地，若$\mid S\mid=r$，则$R\<S\>=\\{f(a_1,\cdots,a_r),f\in R[x_1,\cdots x_r]\\}$.

设$L\supset K$是域扩张，$S\subset L$，则在$L$中，$K[S]:=K\<S\>=$包含$K\cup S$的最小子环$=\\{f(a_1,\cdots,a_r),f\in K[x_1,\cdots x_r],r\in\mathbb{N},a_i\in S\\}$，
$K(S)=$包含$K\cup S$的最小子域$=\\{p(a_1,\cdots,a_r)/q(a_1,\cdots,a_r),p,q\in K[x_1,\cdots x_r],r\in\mathbb{N},a_i\in S,q(a_1,\cdots,a_r)\ne0\\}$.

**单扩张** 设$L\supset K$是域扩张，$\alpha\in L$，则$K(\alpha)=\\{p(\alpha)/q(\alpha),p,q\in K[x]\\}$，
$K[\alpha]=\\{f(\alpha),f\in K[x]\\}$. 特别地，若$\alpha$在$K$上代数，即$\alpha$是$K$上某个首一不可约多项式方程$f(x)=0$的根，
则$K[\alpha]=K(\alpha)\cong K[T]/(f(T))$；若$\alpha$在$K$上超越，则$K[\alpha]\cong K[T]$，$K(\alpha)\cong K(T)$.
