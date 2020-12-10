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
