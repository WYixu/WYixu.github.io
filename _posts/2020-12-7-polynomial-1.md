---
title: 数 · 多项式 · 一元多项式
layout: post
tag: 数
---

设$K$是域，形式上的变元$X$，则多项式可以形式上表示为：$a_0X^n+\cdots+a_{n-1}X+a_n, a_i\in K$，
单项式：$cX^n, n=0,1,\dots$，注意，$n=0$时，$c$本身也是单项式.

例子：$K=\mathbb{R}: x^2+1$，$K=\mathbb{F}_p: x^p-x$.

**例**  多项式函数.  设$K$是域，$f:K\rightarrow K$是多项式函数$(=:"f(x)=a_0x^n+\cdots+a_n")$.
$Poly(K):=K$上的多项式函数的集合是一个交换幺环. (是$Fun(K, K)$（函数环）的子环).

在无限域上，任意非零多项式只有有限多的解，因此多项式函数足以决定多项式的项.

$K=\mathbb{F}_q$时，$f(x)=x^q-x$是零函数.

插值公式(Lagrange)  假设$a_1,\cdots, a_n \in K$两两不同，则任何一个次数小于等于$n-1$的多项式完全由它在
$a_1, \cdots, a_n$的值决定，设$b_1, \cdots, b_n\in K$，则
$F(x)=\sum_{i=1}^n b_i\prod_{j\ne i}\frac{x-a_j}{a_i-a_j}=
\sum_{i=1}^n \frac{b_i}{F(a_i)}\prod_{j\ne i}(x-a_j)$
满足$F(a_i)=b_i$.

更一般的多项式是定义在一个交换幺环$R$上的，$f=c_0+c_1x+\cdots+c_nx^n$. $f$对应$x^i$的*系数*是$c_i$. 设$d$是
最大的非负整数使得$c_d\ne0$，称$f$的*首项*$LT(f)=c_dx^d$，*首项系数*$LC(f)=c_d$，$f$的*次数*$deg_x(f)=d$.

例子：$f=x^q-x, LT(f)=x^q, LC(f)=1, deg(f)=q$. $deg(c)=0(c\ne0), deg(0)=-\infty$.

$f=c_0+c_1x+\cdots+c_nx^n, g=d_0+d_1x+\cdots+d_mx^m$，视$c_i(f)=0$若$i>n$. 则$f$完全由其系数决定，若
若任意$i$，$f$和$g$他们在$x^i$的系数相同，则$f=g$，给定一组数$c_0,\cdots,c_n,\cdots\in R$，满足
$\exists N, n>N\Rightarrow c_n=0$，则存在唯一的多项式，其$i$次项系数为$c_i$.

$R[x]:=R$上的多项式环\代数$=\\{c_0+c_1X+\cdots+c_NX_N\mid c_i\in R\\}$，其上有如下资料：\\
零元：零多项式，记为$0$，幺元：常数多项式$1$.\\
加法$+:c_n(f+g)=c_n(f)+c_n(g)$，乘法$\cdot:c_n(f\cdot g)=\sum_{l=0}^n c_l(f)c_{n-l}(g)$.

$R[x]$是交换幺环，也是一个$R$代数，且满足如下的泛性质：对任意$R$代数$A$，$\forall a\in A, \exists!R$代数同态
$\phi:R[x]\rightarrow A, \phi(x)=a$.

> **定义**  设$R$是交换幺环，则$A$是$R$代数若：$A$是一个环，且我们有环同态（称为结构同态）
> $\phi_0:R\rightarrow Z(A)=A$的中心$=\\{x\in A\mid xy=yx, \forall y\\}$.
> 或者$A$上有一个运算数乘：$R\times A\rightarrow A, (a,x)\mapsto ax$满足
> $(a+b)x=ax+bx$,$a(x+y)=ax+ay$,$(ab)x=a(bx)$（现在$A$是一个$R$模）,$a(xy)=(ax)y=x(ay)$.

例子：当$R=K$是域时，$K$代数$A$是环，也是$K$线性空间.\\
多项式函数的的解释————取值：设$A$是$R$代数，$a\in A$，$f(x)=c_0+c_1x+\cdots+c_nx^n\in R[x]$，则
$f(a)=c_0+c_1a+\cdots+c_na^n$就是$f(x)$在前述泛性质下的像.\\
任何加法群都是$\mathbb{Z}$代数.

称$f$为*首一的*若$LC(f)=1$.

$f,g\in R[x]$，则$deg(f+g)\le max(deg(f),deg(g))$，等号成立若$deg(f)\ne deg(g)$.\\
$deg(fg)\le deg(f)+deg(g)$，等号成立若$R$是整环或$f$或$g$首一.

**命题**  $R$是整环$\Rightarrow$ $R[x]$是整环.\\
**证明**  设$f,g\in R[x]$$f,g\ne 0$，则$fg\ne0$因为$deg(fg)=deg(f)+deg(g)\ne 0$.\\
例子：$K[x], \mathbb{Z}[x]$都是整环.

**除法原理**  设$R$是交换幺环，$g\in R[x]$首一，$deg(g)=d$，$f\in R[x]$，则存在唯一的
$q,r\in R[x]$满足$f(x)=q(x)g(x)+r(x)$且$deg(r)<d$.\\
**证明**  *唯一性*：设$q_2,r_2\in R$也满足条件，则$f=qg+r=q_2g+r_2$ $\Rightarrow$ $(q-q_2)g=r_2-r$
$\Rightarrow$ $deg(r_2-r)=deg(q-q_2)+deg(g)<deg(g)$ $\Rightarrow$ $q=q_2,r=r_2$.\\
*存在性*：考察$\Omega:=\\{f-qg\mid q\in R[x]\\}$，则$\Omega\ne \emptyset$. 若$0\in\Omega$则$g\mid f$，
$f=qg$. 若$0\notin\Omega$则由最小数原理，存在$r=f-qg$次数最小，断言$deg(r)<d$，假设不然，
记$r=c_0+\cdots+c_mx^m=f-qg, g=b_0+\cdots+x^d$，则令$\tilde{q}=q+c_mx^{m-d}, \tilde{r}=r-c_mx^{m-d}g$，
则$f=\tilde{q}g+\tilde{r}$，$\tilde{r}\in \Omega$但$deg(\tilde{r})<deg(r)$，矛盾！

**例** 设$g(x)=x-a$，则由除法原理，$f(x)=q(x)(x-a)+f(a)$，特别地，$f(a)=0\Leftrightarrow(x-a)\mid f(x)$.

在域$K$的多项式环$K[x]$上，除法原理对$g$的要求弱化为$deg(g)\ne 0$.

**命题** $K[x]$是主理想整环(PID)
（$R$是主理想整环即$\forall I\subset R$是理想，$\exists a$使得$I=(a)$即$I={ax|x\in R}$），
即设$I$是$K[x]$的非零理想，则$\exists!$首一多项式$g(x)\in I$使得$I=(g(x))$.\\
**证明** *存在性*：由最小数原理，$I$中存在次数最小的首一多项式，记为$g(x)$，现断言：$I=(g(x))$以及$g$唯一.
$\forall f\in I$，$\exists(!)q,r\in K[x]$，$f=qg+r$ $\Rightarrow$ $r=f-qg\in I$，若$r\ne 0$，则
$LC(r)^{-1}r\in I$首一且次数严格小于$g$，矛盾！\\
*唯一性*：设$g(x),h(x)$首一且$I=(g(x))=(h(x))$，则$g(x)\mid h(x), h(x)\mid g(x)$，由于均首一，$h=g$.

**推论** $K[x]$是唯一分解整环(UFD)，更强地，$\forall f\ne0\in K[x]$可以唯一地写成$f(x)=cg_1(x)\cdots g_r(x)$，
$g_i(x)\in K[x]$为首一的不可约多项式.

> **定义** 不可约多项式. f可约当且仅当存在$g,h$，$f=gh$且$deg(g),deg(h)<deg(f)$.\\
> 例子：$\mathbb{C}$中，首一不可约多项式只有$x-c,c\in\mathbb{C}$.\\
> $\mathbb{R}$中，首一不可约多项式只有$x-a,x^2+ax+b(a^2-4b<0)$.\\
> $\mathbb{Q}$中，$x^3-2$不可约.\\
> $x^2+x+1$在$\mathbb{F}_2$中不可约，但在$\mathbb{F}_3$中可约.

**例** 设$V=K^n,A\in End_K(V)\cong M_n(K)$. 考察$I=\\{f(x)\in K[x]\mid f(A)=0\\}$称为$A$的零化子.
则$I$是$K[x]$的理想，$I\ne 0$.（原因：$I=\ker (\phi:K[x]\rightarrow M_n(K), x\mapsto A)$
或者哈密尔顿-凯莱定理）\\
$\chi_A(T):=\det(T\cdot I_n-A)$($T\cdot I_n-A\in M_n(K[T])$)称为$A$的特征多项式，则$\chi_A(A)=0$.
极小多项式$P_A(T)$是A的零化子的首一多项式生成元.\\
例子 $A=diag(a_1, \cdots, a_n)$，$\chi_A(T)=(T-a_1)\cdots(T-a_n)$，
$P_A(T)=\prod_{a\in \\{a_1\cdots a_n\\}}(T-a)$.
