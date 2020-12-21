---
title: 数 · 多项式 · 根
layout: post
tag: 数
---

在域$K$上的多项式$f(x)\in K[x]$，称$x=\alpha$是$f(x)$的零点/根，若$f(\alpha)=0$. 由除法原理，存在唯一的$q(x)\in K[x]$，
满足$f(x)=(x-\alpha)q(x)$.

多项式方程$f(x)=0$至多有$deg(f)$个根.

**重数**  $\alpha$作为$f(x)\in K[x]$的零点，重数是以下的$m$：$f(x)=(x-\alpha)^mg(\alpha), g(\alpha)\ne 0$.
特别地，规定$\alpha$作为零点的重数为$0$若$f(\alpha)\ne 0$.

在数学分析中，对于无限可导的函数$f(x)$，$x=a$是$f(x)$的$m$重零点，当且仅当$f^{(m)}(a)\ne 0,f(a)=f'(a)=\cdots=f^{(m-1)}(a)=0$.

受以上内容的启发，我们定义如下的形式导数：\\
**（形式）导数**  设$f(x)=c_nx^n+\cdots+c_0$，则$f'(x)=nc_nx^{n-1}+\cdots+a_1$，特别地，$f(x)=cx^n$，则$f'(x)=ncx^{n-1}$.

**命题** $D:K[x]\rightarrow K[x], f(x)\mapsto f'(x)$是满足以下条件的唯一的算子：\\
(1) $D$是$K-$线性的，$D(f+g)=Df+Dg$，$D(af)=aDf$.\\
(2) $D$满足乘法求导原则：$D(fg)=fDg+gDf$.\\
(3) $Dx=1$.\\
**证明** 唯一性：由于$D$是$K-$线性的，只需证明$Dx^n$是唯一的. $D(1)=D(1\times 1)=1D(1)+D(1)1\Rightarrow D(1)=0$.
$Dx^n=D(x^{n-1}x)=xDx^{n-1}+x^{n-1}Dx=(n-1)x^{n-2}x+x^{n-1}=nx^{n-1}$（归纳法）.

这样定义的导数同样有链式法则：$(f(g(x)))'=f'(g(x))g'(x)$. 特别地，$(f(ax+b))'=af'(ax+b)$.

**命题** 设$f(x)$在$x=a$处的阶（即$x=a$作为$f(x)$零点的重数）为$m\in \mathbb{Z}_{\ge0}$，则(1)$f^{(j)}(a)=0(j=0,1,\cdots,m-1)$；
(2)若$m>0$，$char(K)\nmid m!$，则$f^{(m)}(a)\ne 0$，若$m>0$，$char(K)\mid m!$，则$f^{(m)}(a)= 0$.\\
**证明** 由于如此定义的求导和平移是交换的，所以仅讨论$a=0$的情形. 设$f(x)$在$x=a$的阶为$d\ge 0$，不妨设$f(x)=a_0x^n+\cdots+a_{n-d}x^d(a_0,a_{n-d}\ne0)$
（由阶的定义，$x^d\mid f(x)$）.\\
(1) $d=0$，$a_n\ne 0$，$f(0)=a_n\ne0$.\\
(2) $d\in \mathbb{N}$. $f^{(j)}(x)=\* x^{n-j}+\cdots+\* x^{d-j}$，当$0\le j\le d-1$时，$f^{(j)}(0)=0$；当$j=d$时，$f^{(d)}(x)=\* x^{n-d}+\* x+a_{n-d}d!$，
$a_{n-d}\ne 0$，因而$f^{(d)}(0)\ne0\Leftrightarrow d!\ne 0 \Leftrightarrow char(K)\nmid n!$.

特别地，零多项式在任何点上的阶是$+\infty$.

**例** 若$f'(x)=0$，设$f(x)=c_nx^n+\cdots+c_0$，则$f'(x)=nc_nx^n+\cdots+c_1$，$f'(x)=0\Leftrightarrow jc_j=0(\forall j\in \mathbb{N})$.
$char(K)=0$时，$c_j=0$，$f(x)=c_0$是常多项式；$char(K)=p>0$时，$p\nmid j$则$c_j=0$，因而$c_j\ne 0\Rightarrow p\mid j$，因而存在$h(x)\in K[x]$，
$f(x)=h(x^p)$.

**例** 设$K=\mathbb{F_p}(T)$是$\mathbb{F_p}$上的一元有理函数域，$K'\supset K,K'=K(T^{1/p})(=K(T)[Y]/(Y^p-T))$，令$t\in K'$满足$t^p=T$，则
$f(x)=x^p-T$在$K[x]$上不可约，但是$f(x)=(x-t)^p\in K'[x]$，而$f'=0,f^{(n)}=0$.

**推论** 在代数封闭域上，$f(x)$有重零点$\Leftrightarrow(f(x),f'(x))\ne 1$.\\
**证明** $\Rightarrow$：$f(x)=(x-a)^m h(x)$，$h(a)\ne0$，则$f'(x)=m(x-a)^{m-1}h(x)+(x-a)^mh'(x)$，$f'(a)=0$，则$(x-a)\mid (f(x),f'(x))$.\\
$\Leftarrow$：若$(f(x),f'(x))\ne1$，则存在$g(x)\in K[x]$，$deg(g)\ge 1$，$g(x)\mid (f(x),f'(x))$. 令$a$为$g(x)=0$的根，则$(x-a)\mid f(x),f'(x)$，
设$f(x)=(x-a)^mh(x),h(a)\ne0$，则$f'(a)=0$，若$m\ge 2$；$f'(a)=h(a)\ne 0$，若$m=1$.

**推论** 对于一般的$K$，$f(x)\in K[x]$，$(f(x),f'(x))\ne 1$ $\Leftrightarrow$ 要么$f(x)$有重因子，要么$f(x)$的某一不可约因子是不可分多项式.

**不可分多项式** 设$char(K)=p>0$，$f(x)\in K[x],deg(f)\ge 1$，则$f(x)$不可分，若$f(x)$的某一个不可约因子在$\bar{K}$（代数封闭域）中有重根.

**判别式** 设$f(x)\in K[x]$，在$K'\supset K$上分裂（即$f(x)$在$K'[x]$中完全分解），并且$f(x)=a_0(x-\alpha_1)\cdots(x-\alpha_n)$，
则$D(f):=a_0^{2n-2}\prod_{1\le i<j\le n}(a_j-a_i)^2$可以表示成$f(x)$系数的多项式（而且是整系数多项式）.

**例** $ax^2+bx+c$的判别式是$b^2-4ac$，$x^3+px+q$的判别式是$-4p^3-27q^2$.

**结式** 在代数封闭域$K$上，$f(x),g(x)\in K[x]$，$(f,g)\ne 1$，即存在$f_1,g_1$使得$f_1g=g_1f$，$deg(f_1)\le deg(f),deg(g_1)\le deg(g)$.
$f(x)=a_0x^n+\cdots+a_n,g(x)=b_0x^m+\cdots+b_m$，定义：
$$
R(f,g):=\det \left(\begin{aligned}
&a_0\;a_1\;\cdots\;a_n\;0\;\cdots\;0\\
&0\;a_0\;a_1\;\cdots\;a_n\;0\;\cdots\;0\\
&0\;0\;a_0\;a_1\;\cdots\;a_n\;0\;\cdots\;0\\
&\vdots\\
&0\;\cdots\;0\;a_0\;a_1\;\cdots\;a_n\\
&b_0\;b_1\;\cdots\;b_m\;0\;\cdots\;0\\
&0\;b_0\;b_1\;\cdots\;b_m\;0\;\cdots\;0\\
&0\;0\;b_0\;b_1\;\cdots\;b_m\;0\;\cdots\;0\\
&\vdots\\
&0\;\cdots\;0\;b_0\;b_1\;\cdots\;b_m\\
\end{aligned}\right),
$$
其中，矩阵内以$f$的系数为项的行有$m$行，以$g$的系数为项的行有$n$行，则$f,g$有公因子当且仅当$R(f,g)=0$.
