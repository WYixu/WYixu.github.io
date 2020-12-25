---
title: 数 · 代数封闭域
layout: post
tag: 数
---

**例** $\mathbb{C}$是代数封闭域.

**代数闭包** 设$L\supset K$是域扩张，\\
(1) $\alpha\in L$在$K$上*代数*，若$\alpha$是某个首一多项式方程的根（即存在$f\in K[x]$首一，$f(\alpha)=0$）.\\
(2) $L/K$是*代数扩张*，若$\forall \alpha\in L$，$\alpha$在$K$上代数.\\
(3) $L$是$K$的*代数闭包*，若$L/K$是代数的且$L$是代数封闭的.

**例** $\mathbb{C}$是$\mathbb{R}$的代数闭包，但$\mathbb{C}$不是$\mathbb{Q}$的代数闭包.
而$\mathbb{Q}$的代数闭包是$\\{\alpha\in\mathbb{C}\mid \alpha$ 在$\mathbb{Q}$上代数$\\}$.

为了说明$\mathbb{Q}$的代数闭包确实如此，我们需要许多准备工作.

**命题** (1) $L\supset K$，且$L$中$K$上的代数元构成一个域，即：若$\alpha,\beta\in L$在$K$上代数，
则$\alpha\pm\beta,\alpha\beta,\alpha^{-1}$都是代数元.\\
(2) 若$K\subset L\subset L'$是域扩张，$L/K,L'/L$都是代数扩张，那么$L'/K$也是代数扩张.\\
**证明** **(I)** 定义：$L/K$是*有限扩张*，若$\dim_K L(=:[L:K])<+\infty$.\\
**(II)** 如果$[L:K]<+\infty,[L':L]<+\infty$，那么$[L':K]=[L':L][L:K]<+\infty$. 实际上，若$\alpha_1,\cdots,\alpha_n$
是$L/K$的一组基，$\beta_1,\cdots,\beta_m$是$L'/L$的一组基，则$a_ib_j(i=1,\cdots,n,j=1,\cdots,m)$是$L'/K$的一组基，
因为，$\forall x\in L$，$x=\sum_{j=1}^m y_j\beta_j,y_j\in L$，$y_j=\sum_{i=1}^n c_{ij}\alpha_i,c_{ij}\in K$，
则$x=\sum_{i=1}^n\sum_{j=1}^m c_{ij}\alpha_i\beta_j$. 而$\\{\alpha_i\beta_j\\}$在$K$上线性无关，因为设
$\sum_{i=1}^n\sum_{j=1}^m c_{ij}\alpha_i\beta_j=0$，即$\sum_{j=1}^m(\sum_{i=1}^nc_{ij}\alpha_i)\beta_j=0$，
则$\sum_{i=1}^nc_{ij}\alpha_i=0$，则$c_{ij}=0$.\\
**(III)** (2)的证明.\\
(a) $L\in K,\alpha\in L$，则$\alpha$在$K$上代数，当且仅当$K(\alpha)/K$是有限扩张. 原因：(i) 若$\alpha$在$K$上代数，
则$K(\alpha)\cong K[\alpha]\cong K[T]/(f(T))$，$f(T)$是$\alpha$在$K$上的极小多项式，则$[K(\alpha):K]=\dim_K(K[T]/(f(T)))=\deg(f)=n$.
(ii) 若$\alpha$是超越元，则$K(\alpha)\cong K(T)\supseteq K[T]$，但$\dim_KK[T]=\infty$.\\
(b) 若$\alpha_1,\cdots,\alpha_r\in L$是$K$上的代数元，则$K(\alpha_1,\cdots,\alpha_r)=K(\alpha_1)(\alpha_2)\cdots(\alpha_r)$
是$K$的有限扩张. 原因：$[K(\alpha_1,\cdots,\alpha_l):K(\alpha_1,\cdots,\alpha_{l-1})]<\infty$，因为$\alpha_l$在
$K(\alpha_1,\cdots,\alpha_{l-1})$上代数（因为$\alpha_l$在$K$上代数，所以$\alpha_l$满足$K$上的一个多项式方程，
自然是$K(\alpha_1,\cdots,\alpha_{l-1}$上的多项式方程）.
则$[K(\alpha_1,\cdots,\alpha_r):K]=[K(\alpha_1,\cdots,\alpha_r):K(\alpha_1,\cdots,\alpha_{r-1})]\cdots[K(\alpha_1):K]<\infty$.\\
(c) (2)的证明：$\forall x\in L'$，设$x$在$L$上的极小多项式$f(x)=x^n+a_1x^{n-1}+\cdots+a_n,a_1,\cdots,a_n\in L$，则$x$在
$K(a_1,\cdots,a_n)$上代数，由于$a_i\in L$在$K$上代数，由(b)，$[K(a_1,\cdots,a_n):K]<\infty$，所以
$[K(x):K]\le [K(x,a_1,\cdots,a_n):K]=[K(x,a_1,\cdots,a_n):K(a_1,\cdots,a_n)][K(a_1,\cdots,a_n):K]<\infty$，即$x$在$K$上代数. \\
**(IV)** (1)的证明：由于$\alpha\pm\beta,\alpha\beta,\alpha^{-1}$在$K(\alpha,\beta)$上代数，所以$\alpha\pm\beta,\alpha\beta,\alpha^{-1}$在
$K$上也代数.

**命题** 设$K\in E$，$E$是代数封闭域，则$E_0=\\{x\in E, x$在$K$上代数$\\}$为$K$的代数闭包.\\
**证明** 由上个命题知道，$E_0\subset E$是子域，$E_0/K$是代数扩张. 现在希望说明$E_0$是代数封闭的，原因：
设$f(x)\in E_0[x]$，$\alpha\in E$是$f(x)$的根，则$E_0(\alpha)/E_0$是代数扩张，而$E_0/K$是代数扩张，故$E_0(\alpha)/K$也是代数扩张，
则$\alpha$在$K$上代数，则$\alpha\in E_0$.

至此，$\mathbb{Q}$的代数闭包讨论完成.

关于代数闭包，还有一个重要的命题：\\
**命题** 代数闭包存在且唯一，即对任意域$K$，存在域扩张$E/K$，$E$是$K$的代数闭包；$E,E'$都是代数闭包，则存在域同构$E\cong E'$（作为$K$代数同构）.\\
**证明** （参考柯斯特利金《代数学引论》第三卷，暂略）
