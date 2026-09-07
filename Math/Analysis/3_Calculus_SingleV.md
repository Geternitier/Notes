# 三、一元微积分



## 1. 函数连续

### 极限与连续

函数极限：度量空间X和Y，$E\subset X$，$f$映射$E$到$Y$，$p$是$E$的聚点。若$\exists q\in Y$，满足$\forall\varepsilon\gt0,\exists\delta\gt0$使得$\forall x\in N_\delta(p)$有$d(f(x),q)\lt\varepsilon$，称$q$为$f$在$p$的极限，记为$\lim_{x\rightarrow p}f(x)=q$，或$x\rightarrow p$时$f(x)\rightarrow q$。

函数极限的蕴含性质：

1. 若函数在一点的极限存在，那么该极限的值唯一。
2. 极限运算法则：$\lim_{x\rightarrow p} f=A,\lim_{x\rightarrow p} g=B$
   - $\lim_{x\rightarrow p}(f+g)=A+B$
   - $\lim_{x\rightarrow p}fg=AB$
   - $\lim_{x\rightarrow p}\frac fg=\frac AB,B\neq0$

函数连续：度量空间X和Y，$E\subset X$，$f$映射$E$到$Y$，$\forall\varepsilon\gt0,\exists\delta\gt0$使得$\forall x\in N_\delta(p)$有$d(f(x),f(p))\lt\varepsilon$，称$f$在$p$连续。若$f$在$E$的每一点连续，称$f$在$E$连续。

函数连续的蕴含性质：

1. $f$在$E$的聚点连续，当且仅当$\lim_{x\rightarrow p}f(x)=f(p)$。
   - 孤立点显然完全满足连续的定义。
2. $f$映射$X$到$Y$，则$f$在$X$连续的充要条件为：
   - 对$y$的每个开子集V，$f^{-1}(V)$为X的开子集，或者
   - 对$y$的每个闭子集U，$f^{-1}(U)$为X的闭子集
3. 复合函数的连续性：
   - 度量空间$X,Y,Z$，$E\subset X$，$f$映射$E$到$Y$，$g$映射$f(E)$到$Z$，$h(x)=g(f(x))$，若$f$和$g$连续，则$h$连续。
   - $\mathbb R$上函数$f_1,...,f_k$，$\vec f(x)=(f_1(x),...,f_k(x))$连续当且仅当$f_1,...,f_k$连续。
4. 函数连续性和运算：
   - 度量空间上的连续函数$f,g$有$f+g,fg,\frac fg(g\neq0)$均连续。
   - $\mathbb R^k$上的连续函数$f,g$有$f+g,fg$连续。

 函数有界：即函数的值域有界。



### 连续性和紧致性

连续性与紧致性的蕴含性质：紧度量空间$X$，度量空间$Y$。

1. $f:X\rightarrow Y$，则$f(X)$是紧致的。
2. $f:X\rightarrow\mathbb R^k$，则$f(X)$是有界闭集。
   - 闭区间连续函数的最值定理（有界性定理）。

一致连续：度量空间$X,Y$，$f:X\rightarrow Y$。$\forall\varepsilon\gt0,\exists\delta\gt0$使得$\forall p,q\in X$，若$d(p,q)\lt\delta$，有$d(f(p),f(q))\lt\varepsilon$。

- 紧致集上的连续函数是一致连续的。

$\mathbb R$上非紧集的蕴含性质：

1. 存在无界连续函数。
2. 存在连续有界且无最值的函数。
3. 如果非紧集有界，则存在不一致连续的连续函数。
   - 无界非紧集可能不存在不一致连续的函数，例如$\mathbb Z$上所有函数都一致连续。



### 连续性和连通性

若$f:X\rightarrow Y$在$X$的连通子集$E$上连续，则$f(E)$连通。

- 闭区间连续函数的介值定理：连续实函数$f$，闭区间$[a,b]$，$f(a)\lt c\lt f(b)$，则$\exists x\in(a,b)$有$f(x)=c$。



### 间断点

函数不连续的点称为间断点。

$\mathbb R$上函数的间断点分类：

1. 第一类间断：$f(x)$在$x_0$的左右极限都存在。
   - 左极限不等于右极限：跳跃间断点。
   - 左极限等于右极限：可去间断点。
2. 第二类间断：$f(x)$在$x_0$的左右极限至少有一个不存在。
   - 一侧极限为无穷：无穷间断点。
   - 极限振荡不存在：振荡间断点。



## 2. 导数

### 导数

导数：$f$在$[a,b]$有定义，$\forall x\in[a,b],\phi(t)=\frac{f(t)-f(x)}{t-x},t\neq x\land t\in(a,b)$，若$f'(x)=\lim_{t\rightarrow x}\phi(x)$存在，则称$f$在$x$可导，记$f$在$x$的导数为$f'(x)$。

若$f$在$[a,b]$每一点可导，则$f$在$[a,b]$可导。类似地，可以定义$f$在$(a,b)$的导数，此时$f'(a),f'(b)$是未定义的。

导数的蕴含性质：

1. 连续性：$f$在$x$可导，则$f$在$x$连续。
2. 复合函数：$f$在$[a,b]$可导，$g$在$f([a,b])$可导，则$h(x)=g(f(x))$在$[a,b]$可导，且$h'(x)=g'(f(x))f'(x)$。
3. 函数运算：$f,g$在$[a,b]$有定义且在$x\in[a,b]$可导，则有
   - $f+g$在$x\in[a,b]$可导，$(f+g)'(x)=f'(x)+g'(x)$
   - $fg$在$x\in[a,b]$可导，$(fg)'(x)=f'(x)g(x)+g'(x)f(x)$
   - $\frac fg$在$x\in[a,b]$可导（$g\neq 0$），$(\frac fg) '(x)=\frac{f'(x)g(x)-g'(x)f(x)}{g(x)^2}$
4. 高阶导数：$f^{(n)}(x)$称为$f$的$n$阶导数，$f^{(n)}(x)$存在，即$f^{(n-1)}$在$x$的某邻域可导。
   - 莱布尼茨公式$(uv)^{(n)}=\sum_{k=1}^n C_n^ku^{(n-k)}v^{(k)}$

向量函数的导数：即对每一维坐标函数求导数。



### 微分中值定理

导数的中值定理：

1. $f$在$[a,b]$可导，则$\exists x\in(a,b)$有$f(b)-f(a)=f'(x)(b-a)$；
2. $f,g$在$[a,b]$可导，则$\exists x\in(a,b)$有$f'(x)[g(a)-g(b)]=g'(x)[f(a)-f(b)]$。

中值定理的蕴含性质：

1. 洛必达法则：$f,g$在$[a,b]$可导，$\forall x\in(a,b)$有$g'(x)\neq0$，其中$-\infty\leq a\leq b\leq+\infty$。设$\frac{\lim_{x\rightarrow a}f'(x)}{\lim_{x\rightarrow a}g'(x)}=A$，若$x\rightarrow a$时，$f(x)\rightarrow0\land g(x)\rightarrow 0$或者$g(x)\rightarrow+\infty$，则$\frac{\lim_{x\rightarrow a}f(x)}{\lim_{x\rightarrow a}g(x)}=A$。

2. 泰勒展开：$f$在$[a,b]n$阶可导，$x,t,x_0\in[a,b]$，$t$在$x$和$x_0$之间，有$f(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)^2+...\\+\frac{f^{(n-1)}}{(n-1)!}(x_0)(x-x_0)^{(n-1)}+\frac{f^{(n)}(t)}{n!}(x-x_0)^n$。

   常用泰勒展开式总结：$x_0=0$

   - $\mathrm e^x=1+x+\frac1{2!}x^2+\frac1{3!}x^3+...+\frac1{n!}x^n+\mathcal o(x^n)$
   - $\ln(x+1)=x-\frac{x^2}2+\frac{x^3}3-...+\frac{(-1)^{n-1}}{n}x^n+\mathcal o(x^n)$
   - $(1+x)^a=1+ax+\frac{a(a-1)}{2!}x^2+\frac{a(a-1)(a-2)}{3!}x^3+...+\frac{a(a-1)...(a-n+1)}{n!}x^n+\mathcal o(x^n)$
     - $\frac1{1-x}=1+x+x^2+...+x^n+\mathcal o(x^n)$
     - $\frac1{1+x}=1-x+x^2+...+(-1)^nx^n+\mathcal o(x^n)$
   - $\sin x=x-\frac1{3!}x^3+...+\frac{(-1)^n}{(2n+1)!}x^{2n+1}+\mathcal o^{x^{2n+1}}$
   - $\cos x=1-\frac1{2!}x^2+\frac1{4!}x^4+...+\frac{(-1)^n}{(2n)!}x^{2n}+\mathcal o(x^{2n})$
   - $\tan x=x+\frac13x^3+\mathcal o(x^3)$
   - $\arcsin x=x+\frac16x^3+...+\frac{(2n-1)!!}{(2n)!!(2n+1)!!}2^{2n+1}+\mathcal o(x^{2n+1})$
   - $\arctan x=x-\frac13x^3+\frac{(-1)^n}{2n+1}x^{2n+1}+\mathcal o(x^{2n+1})$



### 导数的几何性质

极值/局部极值：度量空间上的实函数$f$，若在点$p$，$\exists\delta\gt0$使$\forall q\in N_\delta(p)$有$f(q)\leq f(p)$，称$p$为极大值点或局部极大值点。类似地可以定义极小值点。

极值点的蕴含性质：

1. 极值点的导数若存在，则其值为0。
2. 极值点判定的充分条件：
   1. $f$在$x_0$处可导，$f'(x_0)=0$且$\exists\delta\gt0$，当$x\in(x_0-\delta,x_0)$有$f'(x)\lt0$，$x\in(x_0,x_0+\delta)$有$f'(x)>0$，则$f$在$x_0$取极小值。类似地可判定极大值。
   2. $f$在$x$处$n$阶可导$f^{n}(x)\neq0$，且对$m=1,2,...,n-1$有$f^{(m)}(x)=0$。$n$为偶数，则当$f^{n}(x)\gt0$，$f$在$x$处取极小值；当$f^{n}(x)\lt0$，$f$在$x$处取极大值。



凹凸性和拐点：$f$在区间$I$连续，$\forall x_1,x_2\in I$，若总有$f(\frac{x_1+x_2}2)\gt\frac{f(x_1)+f(x_2)}2$，称$f$为凸的；若总有$f(\frac{x_1+x_2}2)\lt\frac{f(x_1)+f(x_2)}2$，称$f$为凹的。函数凹的部分和凸的部分的分界点称为拐点。

当函数二阶可导，拐点即一阶导数的极值点。此时拐点的二阶导数为0，继承导数极值点的判别充分条件。其中，凹函数的二阶导数大于0，凸函数的二阶导数小于0。

极值点和拐点的蕴含性质：

1. 二阶可导点不同时为极值点和拐点。
2. $f(x)=(x-a)^ng(x),g(x)\neq0\land n\gt1$，当$n$为偶，$a$为极值点，$n$为奇，$a$为拐点。
3. 多项式函数$f(x)=(x-a_1)^{n_1}...(x-a_k)^{n_k},n_i\gt0$，$k_1$为$n_i=1$的个数，$k_2$为$n_i$为偶数的个数，$k_3$为$n_i$是大于1的奇数的个数，则极值点有$k_1+2k_2+k_3-1$个，拐点有$k_1+2k_2+3k_3-2$个。



曲率$k=\frac{|y''|}{(1+y'^2)^{\frac32}}$，曲率半径$r=\frac1k$。



## 3. 积分

### RS积分

区间$[a,b]$的一个划分$P$是满足$a=x_0\leq x_1\leq...\leq x_n=b$的有限点集$x_0,...,x_n$，$\Delta x_i=x_i-x_{i-1}$。设$[a,b]$上的有界实函数$f$对$P$有$M_i=\sup f(x),x\in[x_i-1,x_i]$，$m_i=\inf f(x),x\in[x_i-1,x_i]$，称Riemann上积分为$\overline{\int_a^b}fdx=\inf\{\sum M_i\Delta x_i\}$，Riemann下积分为$\underline{\int_a^b}fdx=\sup\{\sum m_i\Delta x_i\}$。若上下积分相等，称$f$在$[a,b]$上Riemann可积，记$\int_a^bfdx=\overline{\int_a^b}fd x$为Riemann积分，又称定积分。

设$g$是$[a,b]$上的单调递增函数，对划分$P$有$\Delta g_i=g(x_i)-g(x_{i-1})$，类似地定义$\overline{\int_a^b}fdx=\inf\{\sum M_i\Delta g_i\}$，$\underline{\int_a^b}fdx=\sup\{\sum m_i\Delta g_i\}$。当两者相等，称$f$在$[a,b]$上对$g$可积，记为$f\in\mathcal R(g)$。记$\int_a^bfdg=\overline{\int_a^b}fdg$为Riemann-Stieltjes积分，简称RS积分。

RS积分的蕴含性质：

1. 计算性质：

   1. $f_1\in\mathcal R(g)\land f_2\in\mathcal R(g)$，则$f_1+f_2\in\mathcal R(g)$。
      - 常数c，有$cf_1\in\mathcal R(g)$。
   2. $f\in\mathcal R(g_1)\land f\in\mathcal R(g_2)$，则$f\in\mathcal R(g_1+g_2)$，$\int_a^b fdg(g_1+g_2)=\int_a^b fdg_1+\int_a^b fdg_2$。
      - 常数c，有$f\in\mathcal R(cg_1)$。
   3. $c\in(a,b)$，有$\int_a^cfdg+\int_c^bfdg=\int_a^bfdg$。
   4. $f\in\mathcal R(h)\land g\in\mathcal R(h)$，则$fg\in\mathcal R(h)$。

2. 比较性质：

   1. $f_1\leq f_2$，则$\int_a^b f_1dg\leq\int_a^bf_2dg$。
   2. $M$为$f$上界，则$|\int_a^b fdg|\leq M(g(b)-g(a))$。
   3. $f\in\mathcal R(g)$，则$|f|\in\mathcal R(g)$，且$|\int_a^bfdg|\leq\int_a^b|f|dg$。

3. RS积分化为R积分：若$g'$在$[a,b]$可积，$\int_a^bfdg=\int_a^bfg'dx$。

4. 变量代换：

   $\alpha$在$[a,b]$单调，$f\in\mathcal R(\alpha)$，严格单调连续函数$\phi$将$[A,B]$映射到$[a,b]$，设$\beta(x)=\alpha(\phi(x)),g(x)=f(\phi(x))$，则$g\in\mathcal R(\beta)$且$\int_A^Bgd\beta=\int_a^bfd\alpha$。

5. 积分化为级数：单位阶跃函数$I(x)=\begin{cases}0,x\leq0\\1,x\gt0\end{cases}$。

   设$s\in(a,b),\alpha(x)=I(x-s)$，则$\int_a^bfdx=f(s)$。

   于是设$c_n\geq0$且$\sum c_n$收敛，$s_n\in(a,b)$为一些离散点，$\alpha(x)=\sum c_nI(x-s_n)$，

   $f$在$(a,b)$连续，则$\int_a^bfd\alpha=\sum_{n=1}^\infty f(s_n)c_n$。



### 导数和积分

导数与RS积分的蕴含性质：

1. $f:[a,b]\rightarrow R$黎曼可积，对$x\in[a,b]$有$F(x)=\int_a^xf(t)dt$，则$F$在$[a,b]$连续。若$f$在$x_0$连续，则$F$在$x_0$可导，$F'(x_0)=f(x_0)$。

2. 微积分基本定理：

   $f:[a,b]\rightarrow R$黎曼可积且存在可导函数$F$使$F'=f$，则$\int_a^bfdx=F(b)-F(a)$。

3. 分部积分定理：$F,G$在$[a,b]$可导，$F'=f,G'=g$均黎曼可积，则有

   $\int_a^bf(x)G(x)dx=F(b)G(b)-F(a)G(a)-\int_a^bF(x)g(x)dx$。
