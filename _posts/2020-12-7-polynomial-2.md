---
title: 数 · 多项式 二
layout: post
tag: 数
---

# 整环的整除性

在整环$R$中，$b\mid a\Leftrightarrow a=bc\Leftrightarrow a\in(b)$，$b$称为$a$的**因子**.
例如，在$\mathbb{Z}$中，$\pm 1,\pm n$都是$n$的因子. 1的因子称为**单位**，单位也就是乘法可逆元.
$a$与$b$**相伴**，$a\sim b\Leftrightarrow \exists u\in R^\times a=ub$（对任意的环都有这个定义），
当$R$是整环时，$a\sim b,a,b\ne0\Leftrightarrow a\mid b$且$b\mid a\Leftrightarrow (a)=(b)$.
例如，$K[x]$中，$K[x]^\times=K^\times$，$f$的相伴等价类是$\\{df,d\in K^\times\\}$.
$a$是**不可约元**$\Leftrightarrow$ $a\ne 0$, $a$不是单位，若$a=bc$，则$b$或$c$是单位.
例如，整数环中，素数及其相反数不可约，


**唯一分解整环(UFD)**  整环$R$是UFD，如果$R$满足以下的唯一分解公理：\\
$\forall a\in R$，若$a\ne 0$，$a$不是单位，则$a$可以写成不可约元的乘积，且在相伴意义下是唯一的：
$a=c_1\cdots c_r=d_1\cdots d_s$，$c_i,d_j$不可约，则$r=s$且$\exists\sigma\in S_r,c_i\sim d_{\sigma(i)}$.\\
另一种说法是，假设我们在每一个不可约元的相伴类中定义了一个标准不可约元（素元），则$R$是UFD等价于任意非零元$x$可以
唯一地写成$up_1^{\alpha_1}\cdots p_r^{\alpha_r}$，$p_1,\dots,p_r$为素元，
$\alpha_1,\cdots,\alpha_r\in \mathbb{Z}_{\ge0}$，$u\in R^\times$.

记$\alpha_i=v_{p_i}(x)$，我们还有$v_p(x+y)\ge min(v_p(x),v_p(y))$，$v_p(xy)=v_p(x)+v_p(y)$.

**主理想整环(PID)**  整环$R$是PID，如果$\forall I\subset R$是理想，都$\exists a$使得$I=(a)$.

**欧几里得整环(ED)**  整环$R$是ED，如果$R$上有如下的除法原理：\\
存在一个函数（称为欧式范数）$N:R\rightarrow\mathbb{N}\cup\\{0\\}$使得：$N(x)=0$当且仅当$x=0$；
$\forall a,b\in R, b\ne0,\exists q,r\in R$满足$a=qb+r$且$N(r)<N(b)$.

**例** 高斯整数$\mathbb{Z}[i]=\\{a+bi\mid a,b\in\mathbb{Z}\\}$是ED，PID，UFD. 其范数定义为$N(a+bi)=a^2+b^2$.

## **命题**  ED是PID，PID是UFD.

### ED是PID.

设$R$是ED，$N$是它的欧式范数，则令$\mathcal{A}\subset R$是非零理想，由最小数原理，存在$b\ne0\in\mathcal{A}$，
$N(b)$最小. 则$\forall a\in\mathcal{A}$，由除法原理，存在$q,r\in R,a=qb+r,N(r)<N(b)$，因而$r=a-qb\in\mathcal{A}$.
由于$b$的选取，$N(r)=0$，$r=0$，则$\mathcal{A}=(b)$.

**例** 按照$\mathbb{C}$中的$N=\mid\;\mid^2$，$\mathbb{Z}[\frac{1+\sqrt{-3}}{2}]$是ED，也是PID.
但$\mathbb{Z}[\sqrt{-3}]$不是UFD($(1+\sqrt{-3})(1-\sqrt{-3})=2\times2)$)，因而不是ED.

**正规整环(ND)** 又称整闭整环. $R$是整环，$K$是$R$的分式域（商域），$a\in K$在$R$上整若$a$是$R$上首一多项式方程的根.
$R$是整闭的当且仅当$a\in K$整则$a\in R$. 事实上，UFD是ND，$\mathbb{Z}[\sqrt{-3}]$也不是ND.

**二次扩域** $K=\mathbb{Q}[\sqrt{d}]$.\\
$A$是$\mathbb{Q}[\sqrt{d}]$中在$\mathbb{Z}$上整的元素的集合，则$A=\mathbb{Z}[\sqrt{d}] (d\equiv2,3(mod4))$，
$A=\mathbb{Z}[(1+\sqrt{d})/2] (d\equiv 1(mod4))$.\\
Gauss猜想：当且仅当$d=-1,-2,-3,-7,-11,-19,-43,-67,-163$时，$A$既是UFD也是PID.

### PID是UFD

第一步：分解的存在性

(1) 任何一个非零非单位的元都可以写成不可约元的乘积.

(1-1) 每一个这样的元有一个不可约元做因子.\\
设$a$非零非单位，则$(a)$是非零真理想. 我们寻找这样的序列. $a_1=a$，$a_n\mid a_{n-1}$是$a_{n-1}$真因子.
断言：以上步骤必然终止. 假设不然，考察$I=(a_1,\cdots,a_n,\cdots)$，由于$R$是PID，$\exists c\in R$，$I=(c)$，则
$c$是某个$a_1,\cdots,a_n$的$R$组合，因而，由$a_n$的选取，$a_n\mid c$，而$c\mid a_{n+1}$，$a_n\mid a_{n+1}$.
矛盾！

(1-2) 非零非单位元是不可约元的乘积.\\
构造$a_0=a, a_1,\cdots,a_n,\cdots$满足$a_i\mid a_{i-1}$且$a_{i-1}=a_ic_i$，$c_i$不可约. 以上步骤仍然必终止，
因为若无限，则$I=(a_0,\cdots,a_n,\cdots)=c$，则存在$n$，$a_n\sim a_{n+1}\sim\cdots\sim c$，矛盾.
因而$\exists N, a_N\in R^\times$，$a=a_0=c_1c_2\cdots c_Na_N=c_1c_2\cdots c_{N-1}(c_Na_N)$.

第二步：唯一性

(1)

**定义** 交换幺环$R$，$a\in R$，$I\subset R$是理想，则\\
$a$是**不可约元**（整环中）当且仅当$a=bc\Rightarrow b$或$c\in R^\times$.\\
$a$是**素元**当且仅当$\forall b,c\in R, a\mid bc\Leftrightarrow a\mid b$或$c$.\\
$I$是**素理想**$\Leftrightarrow$ $\forall b,c\in R, bc\in I\Rightarrow b$或$c\in I$ $\Leftrightarrow$
$R/I$是整环.\\
$I$是**极大理想**$\Leftrightarrow$不存在理想$J$，$I\subsetneqq J\subsetneqq R$ $\Leftrightarrow$ $R/I$是域.

**引理** PID中以下命题等价：\\
(1) $a$是不可约元.\\
(2) $a$是素元.\\
(3) $(a)$是素理想.\\
(4) $(a)$是极大理想.\\
**证明** (4)$\Rightarrow$(3)，因为域是整环.\\
(3)$\Leftrightarrow$(2).\\
(2)$\Rightarrow$(1)，$p$是素元，设$p=bc$，$b,c\in R$，则$p|b$或$c$，因而$p$与$b$或$c$之一相伴，另一个是单位.\\
(1)$\Rightarrow$(4)，设$(a)$是不可约元，并假设$(a)\subset J\subset R$，希望证明$J=(a)$或$J=R$.
由于$R$是PID，$J=(c)$，因而$a\in(c)$，$c\mid a$，由于$a$不可约，要么$c\sim a$，此时$J=(a)$，要么$c$是单位，
此时$J=R$.

(2) 设$a=p_1\cdots p_r=q_1\cdots q_s$，对$min(r,s)$归纳，不妨设$r\le s$，
(i) $r=1$，$a=p_1=q_1\cdots q_s$，则$s=1, p_1=q_1$.
(ii) 假设命题对$r=n-1$成立，$r=n$时，$a=p_1\cdots p_n=q_1\cdots q_s$，$p_1$不可约，则$p_1$是素元，
则$p_1\mid q_1,\cdots,q_s$之一，不妨设$p_1\mid q_1$，由于$q_1$不可约，$p_1\sim q_1$，消去后得到$r=n-1$的情形.


**例** $\mathbb{Z}[i]$中的不可约元：\\
$p\equiv3(4)$为素数，则$\pm p,\pm pi$是不可约元.\\
$p=2$或$p\equiv 1(4)$，设$p=a^2+b^2,a,b\in \mathbb{Z}$，则$\pm(a\pm bi),\pm(b\pm ai)$都是不可约元.

若$\pi$是不可约元，则$\pi$必然整除某个素数. 又$\pi\mid N(\pi)=\pi\bar{\pi}$. 所以$\pi$整除$N(\pi)$的某个素因子.

若$p\equiv3(4)$为素数，则$p$为不可约元，否则，$p=\alpha_1\cdots\alpha_r, \alpha_i\in \mathbb{Z}[i]$不是单位.
取$N$，$p^2=N(p)=N(\alpha_1)\cdots N(\alpha_r)$，则$r=2$且$p=\alpha_1\alpha_2, \alpha_2=\bar{\alpha_1}$.
$\alpha_1=a+bi$，则$a^2+b^2=p\equiv3(4)$，不可能.

$p=2$ $2i=(1+i)^2$，所以$(1+i)$不可约（$N(1+i)=2$），与它相伴的也不可约.

$p\equiv 1(4)$ 首先，存在整数$x$，$p\mid x^2+1$，也就是说，$-1(mod p)$是二次剩余，原因：
$\mathbb{F_p}^\times\cong C_{p-1}$，$-1$是二阶元. 其次，考察$(p,x+i)$是主理想，记$(p,x+i)=(a+bi)$，则
$1\notin (p,x+i)$（考察$(p,x+i)(p,x-i)=(p)$），$a+bi\mid p$，由之前的情况，$p=(a+bi)(a-bi)$，若$\pi\mid p$，
$\pi\sim (a\pm b_i)$.
