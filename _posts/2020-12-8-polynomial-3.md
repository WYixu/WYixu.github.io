---
title: 数 · 多项式 · 整系数多项式
layout: post
tag: 数
---

**例** $\mathbb{Z}[x]$\\
$\mathbb{Z}[x]$不是PID，其素理想有三大类：\\
极大理想$(p,f(x))$，$p$为素数，$f(x)(mod p)$不可约.\\
$(p)$，$p$为素数，$(f(x))$，$f(x)$是$\mathbb{Z}[x]$中不可约多项式.\\
$(0)$.

令$\mathcal{M}=(p,f(x))$，$\mathbb{Z}[x]/\mathcal{M}\cong \mathbb{F}_p[x]/(\bar{f}(x))$，由于$\bar{f}(x)$不可约，
$\mathbb{F}_p[x]$是PID，则$(\bar{f}(x))$是极大理想，故$\mathbb{Z}[x]/\mathcal{M}$是域，$(p,f(x))$是极大理想.

$\mathbb{Z}[x]/(p)\cong \mathbb{F}_p[x]$是整环，则$(p)$是素理想.

$f(x)$不可约，由高斯引理（下述），$\mathbb{Z}[x]$是UFD，故$f(x)$是素元，$(f(x))$是素理想.

为什么$\mathbb{Z}[x]$的理想只有以上几种？\\
$\mathcal{P}$是$\mathbb{Z}[x]$的极大理想，则存在素数$p\in\mathcal{P}$，否则$\mathbb{Z}[x]/\mathcal{P}$包含
$\mathbb{Z}$，因而包含$\mathbb{Q}$，因而$\mathbb{Q}$作为$\mathbb{Z}[x]$的商环，也是有限生成的$\mathbb{Z}$代数，
但是$\mathbb{Q}$不是有限生成的.

**命题** 设$R$是整环，并且满足每个非零非单位元是不可逆元的乘积，则$R$是UFD当且仅当$R$中每个不可约元都是素元.\\
证明见PID是UFD的最后部分.

**Guass引理** $R$是UFD$\Rightarrow$ $R[x]$是UFD.\\
**推论** $R$是UFD，$K$是其商域，$f(x)\in R[x]$，则$f(x)$在$R[x]$中不可约等价于$f(x)$在$K[x]$中不可约且$f(x)$是本原的（系数没有公因子）.

**例** 设$f(x)=a_0x^n+\cdots+a_n\in \mathbb{Z}[x]$是本原的，若$\alpha\in\mathbb{Q}$是$f(x)$的根，则$\alpha$的分母整除$a_0$，分子整除$a_n$.
特别的，如果$f(x)$首一，则$f(x)$的有理根必是整根，因此$\mathbb{Z}$是整闭的.

**证明**

第一步：任何非零、非单位的多项式是是不可约元的乘积.

对次数归纳，次数$=0$，由于$R$是UFD，$R$中的不可约元在$R[x]$中也不可约.
次数$>0$，设$f\in R[x]$，$deg(f)=n$. \\
(1) $f$不可约，成立.\\
(2-1) $f(x)$是本原的，则若$f=gh$，则要么$deg(g),deg(h)<deg(f)$，要么$g(x),h(x)$之一为常数，必为单位，两种情况+
归纳法，得出$f$要么可分解，要么不可约.\\
(2-2) 一般地，$f(x)=cf_0(x)$，$f_0$本原，$c=gcd(f$的因子$)$.

第二步：关于本原多项式：\\
(1) 本原多项式的乘积也是本原多项式；\\
(2) 任何$f\in K[x]$都可以写成$cg(x)$，$c\in K^\times$，$g(x)\in R[x]$本原，并且$g(x)$在相伴意义下唯一.

(1) $f,g\in R[x]$本原，$h=fg\in R[x]$，设$\pi$是其系数的不可约的公因子，则取$(mod \pi)$，令$\bar{R}=R/(\pi)$，
他是整环，$\bar{h}=\bar{f}\bar{g}\ne 0$，矛盾.\\
(2) $f(x)=c_1g_1(x)=c_2g_2(x)$，$g_1,g_2$本原，$\exists r\in R$，$\tilde{c_1}=rc_1,\tilde{c_2}=rc_2\in R$，
$\tilde{c_1}g_1(x)=\tilde{c_2}g_2(x)$，他们系数的$GCD$既是$\tilde{c_1}$又是$\tilde{c_2}$，因此$\tilde{c_1}\sim \tilde{c_2}$.

第三步：推论的描述性证明.

若$f(x)\in R[x]$不可约，但$f(x)=g(x)h(x)$在$K[x]$中可约，$g(x)=cg_0(x), h(x)=dh_0(x)$，$g_0(x),h_0(x)$本原，且$c,d\in K^\times$.
在$K[x]$中，$f(x)=cdg_0(x)h_0(x)$，$g_0h_0$也是本原的，则$cd\in R^\times$. $f(x)=(cdg_0(x))h_0(x)$在$R[x]$中可约，矛盾！

第四步：不可约元是素元.

(1) 设$a\in R$在$R[x]$中不可约，则$a\in R$自己不可约，由于$R$是$UFD$，$a$是素元.
$R[x]/(a)\cong (R[x]/(a))[x]$是整环，所以$a$在$R[x]$中也是素元.\\
(2) $f(x)\in R[x]$，$deg(f)\ge 1$不可约，由第三步，$f$本原且在$K[x]$中不可约. 由于$K[x]$是PID，也是UFD，则$f(x)$是$K[x]$中的素元.
设$g,h\in R[x]$使得$f\mid gh$，则$f\mid gh$在$K[x]$中也成立. 因而，$f\mid g,h$之一，不妨设$g(x)=q(x)f(x), q(x)\in K[x]$，
欲证$q(x)\in R[x]$. 实际上，设$q(x)=cq_0(x)$，$q_0$本原，则$g(x)=cq_0(x)f(x)$，则$c^{-1}g(x)$本原. 又$g(x)\in R[x]$，
$g(x)=c_1g_1(x)$，$g_1$本原，则$c_1\sim c$，$c\in R$.

**推论** 设$R$是UFD，$f\in R[x]$本原，$g\in R[x]$，则$R[x]$中$f\mid g$当且仅当$K[x]$中$f\mid g$.

**例** $R$是UFD则$R$上的$n$元多项式环$R[x_1,\cdots,x_n]\cong(R[x_1,\cdots,x_{n-1}])[x_n]$也是UFD.

**例** $R$是UFD，则$R$是ND，即若$c\in K$是某个首一$R$系数多项式方程的根则$c\in R$.\\
**证明** 设$f(x)=a_0x^n+\cdots+c_n$，若$f(p/q)=0$，则$q^nf(p/q)=0$，则$a_0p^n+\cdots+a_nq^n=0$，
则$p\mid a_n, q\mid a_0$. 特别地，$R$是整闭的.

**Eisenstein判别法** 设$R$是UFD，$f(x)\in R$首一，若存在$\pi\in R$不可约，满足$f$的其他系数都是$\pi$的倍数且$\pi^2\nmid$常数项，
则$f(x)$在$K[x]$中不可约.

**例** 分圆多项式$\Phi_p(x)=x^(p-1)+\cdots+x+1$在$p$是素数的时候在$\mathbb{Z}[x]$不可约.\\
实际上，$\Phi_p(x+1)$满足Eisenstein判别法（对$p$），$\Phi_p(x+1)=\frac{(x+1)^p-1}{x}=x^{p-1}+\sum_{j=1}^{p-1}{p\choose j}x^{p-1-j}$.
