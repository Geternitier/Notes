# 二、序列和级数



## 1. 序列

### 序列收敛

度量空间$X$，$E\subset X$，序列是$\mathbb N$一一映射到$E$的函数，$p_n=f(n)$，记为$\{p_n\}$。

序列的研究概念：

1. 收敛：序列$\{p_n\}$收敛，即$\exists p\in X,\forall\varepsilon\gt0,\exists N\in\mathbb N$，当$n\gt N,d(p_n,p)\lt\varepsilon$。称$\{p_n\}$收敛到$p$，或$p$是$\{p_n\}$的极限，记$\lim_{x\rightarrow\infty}p_n=p$。不收敛的序列称为发散序列。
2. 有界：序列有界，即序列的值域有界。
3. 子列：正整数序列$\{n_k\}$，序列$\{p_{n_k}\}$称为$\{p_n\}$的子列。

序列收敛的蕴含性质：

1. 若序列收敛，则$\lim_{x\rightarrow\infty}p_n$唯一。
2. 若序列收敛，则序列有界。
3. 若$E\subset X$且$p$为$E$的聚点，则$E$中存在收敛到$p$的序列。
4. 紧度量空间中的序列必有收敛子列。
   - $\mathbb R^k$中的有界序列必有收敛子列。
5. 度量空间X中序列的所有子列极限构成X中的闭子集。



### 柯西序列

柯西序列：$\forall\varepsilon\gt0,\exists N\in\mathbb N$，当$m,n\gt N,d(p_m,p_n)\lt\varepsilon$。

- 度量空间的收敛序列都是柯西序列。
- 紧度量空间中的柯西序列收敛。
  - 非紧度量空间中，柯西序列可能收敛到不在该度量空间的点。
- 若一个度量空间中所有柯西序列收敛，称该度量空间是完备的。



### 数列

实数列的单调有界收敛：

1. 实数列$\{s_n\}$为单调递增的，当且仅当$s_n\leq s_{n+1},n=1,2,...$。
2. 实数列单调且收敛，当且仅当它是有界的。



实数列的上下极限：实数列$\{s_n\}$，$E$为所有$\{s_n\}$子列的极限构成的集合，可能包含$+\infty,-\infty$。称$\lim\sup_{n\rightarrow\infty}s_n=\sup E$为$\{s_n\}$的上极限，$\lim\inf_{n\rightarrow\infty}s_n=\inf E$为$\{s_n\}$的下极限。

上下极限的蕴含性质：

1. $\sup E,\inf E\in E$。
2. $\forall x\gt\sup E,\exists N\gt0$，当$n\gt N$，$s_n\lt x$。下极限类似。
3. 保序性：当$n\gt N$有$s_n\leq t_n$，则$\lim\sup_{n\rightarrow\infty}s_n\leq\lim\sup_{n\rightarrow\infty}t_n$，且$\lim\inf_{n\rightarrow\infty}s_n\leq\lim\inf_{n\rightarrow\infty}t_n$。



复数列极限的计算性质：复数序列$\{s_n\},\{t_n\}$有$\lim_{n\rightarrow\infty}s_n=s,\lim_{n\rightarrow\infty}t_n=t$。

1. $\lim_{n\rightarrow\infty}(s_n+t_n)=s+t$
2. $\lim_{n\rightarrow\infty}cs_n=cs,\lim_{n\rightarrow\infty}(c+s_n)=c+s$
3. $\lim_{n\rightarrow\infty}s_nt_n=st$
4. $\lim_{n\rightarrow\infty}\frac1{s_n}=\frac1s,s_n\neq0\land s\neq0$

向量序列极限的计算性质：$\vec{x_n},\vec{y_n}\in\mathbb R^k$有$\lim_{n\rightarrow\infty}\vec{x_n}=\vec x,\lim_{n\rightarrow\infty}\vec{y_n}=\vec y$

1. $\lim_{n\rightarrow\infty}(\vec{x_n}+\vec{y_n})=\vec x+\vec y$
2. $\lim_{n\rightarrow\infty}a\vec{x_n}=a\vec x$
3. $\lim_{n\rightarrow\infty}(\vec{x_n}\vec{y_n})=\vec x\vec y$



## 2. 级数

### 级数收敛

数列$\{a_n\}$，$\sum_{n=1}^\infty a_n$称为级数，$\sum_{i=1}^n a_i$称为部分和。若部分和收敛，则称级数收敛，称部分和的极限为级数的极限。

若$\sum|a_n|$收敛，称$\sum a_n$绝对收敛，此时$\sum a_n$收敛；若$\sum a_n$收敛而$\sum|a_n|$发散，称$\sum a_n$条件收敛。

级数收敛的蕴含性质：

1. 级数收敛的必要条件：

   1. 级数收敛，则$\lim_{n\rightarrow\infty}a_n=0$。
   2. 级数收敛，则$\forall\varepsilon\gt0,\exists N\in\mathbb N$，当$m\geq n\geq N$有$|\sum_{k=n}^ma_k|\leq\varepsilon$。
   3. 正项级数收敛当且仅当其部分和有界。

2. 级数收敛的充分条件：

   1. 比较判别法：$\sum c_n$收敛，且$\forall n\in\mathbb N$有$|c_n|\geq|a_n|$，则$\sum a_n$收敛。

   2. 根值判别法：$\sum a_n$，$\alpha=\lim\sup_{n\rightarrow\infty}\sqrt[n]{|a_n|}$，

      当$\alpha\lt1$，$\sum a_n$收敛；当$a\gt1$，$\sum a_n$发散。

   3. 比值判别法：

      当$\lim\sup_{n\rightarrow\infty}|\frac{a_{n+1}}{a_n}|<1$，$\sum a_n$收敛；

      若$\exists N\gt0$，$\forall n\gt N$有$|\frac{a_{n+1}}{a_n}|\geq1$，$\sum a_n$发散。 

3. 级数收敛与级数运算：$A=\sum a_n,B=\sum b_n$

   1. $A+B=\sum(a_n+b_n)$。
   2. 定义级数的积$c_n=\sum_{k=0}^na_kb_{n-k}$
      1. 若$\sum a_n$绝对收敛，则$\sum c_n=AB$。
      2. 若已知$\sum c_n=C$，则$C=AB$。




### 分部求和

序列$\{a_n\},\{b_n\}$，$A_n=\sum_{k=0}^na_k$，设$A_{-1}=0$，则对$0\leq p\leq q$有$\sum_{n=p}^qa_nb_n=\sum_{n=p}^{q-1}A_n(b_n-b_{n+1})+A_qb_q-A_{p-1}b_p$。

分部求和的蕴含性质：

1. $\sum a_n$的部分和有界，$\{b_n\}$单调不增且收敛到0，则$\sum a_nb_n$收敛。
   - Leibnitz判别法：各项正负交替的级数$\sum a_n$，若$a_n$单调不增且收敛到0，则$\sum a_n$收敛。
2. $\sum c_nz^n$的收敛半径为1，$\{c_n\}$单调不增且收敛到0，则$\sum c_nz^n$在单位元$|z|=1$上除了$z=1$外的任一点都收敛，在$z=1$处可能收敛。



### 级数重排

设$\{k_n\}$是$\mathbb N$到$\mathbb N$的双射，$a'_n=a_{k_n}$，则称$\sum a'_n$是$\sum a_n$的一个重排。

重排的蕴含性质：

1. 实级数$\sum a_n$条件收敛，对$-\infty\leq\alpha\leq\beta\leq+\infty$，存在重排级数$\sum a'_n$，其部分和$s'_n$满足$\lim\sup_{n\rightarrow\infty}s_n'=\eta,\lim\inf_{n\rightarrow\infty}s'_n=\alpha$。
2. 复级数$\sum a_n$绝对收敛，则$\sum a_n$的所有重排都收敛，且收敛到相同的和。



### 常见正项级数

1. $\sum_{n=0}^\infty x^n=\frac1{1-x},0\leq x\lt1$。
2. $\sum \frac1{n^p}$收敛，则$p\gt1$。
3. $\sum_{n=2}^\infty \frac1{n(\log n)^p}$收敛，则$p\gt1$。
4. $\mathrm e=\sum_{n=0}^\infty\frac1{n!}=\lim_{n\rightarrow\infty}(1+\frac1n)^n$。
5. $\sum_{n=1}^\infty a_n$收敛当且仅当$\sum_{k=0}^\infty 2^ka_{2^k}$收敛。



## 3. 函数序列和级数

note：本节内容在第三章一元微积分之后。

### 函数序列和级数

$\{f_n\}_{n=1}^\infty$是定义在$E$上的一个函数序列。

- 函数列收敛：设$\forall x\in E$有数列$\{f_n(x)\}$收敛，定义$f(x)=\lim_{n\rightarrow\infty}f_n(x),x\in E$，此时称$\{f_n\}$在$E$收敛，称$f$是$\{f_n\}$的极限或极限函数，称$\{f_n\}$逐点收敛到$f$。
- 函数级数收敛：设$\forall x\in E$有级数$\sum f_n(x)$收敛，定义$f(x)=\sum_{n=1}^\infty f_n(x),x\in E$，称$f$为级数$\sum f_n$的和。



### 一致收敛

$\forall \varepsilon\gt0,\exists N\in\mathbb N$使$\forall n\geq N,\forall x\in E$有$|f_n(x)-f(x)|\leq\varepsilon$，称$f_n$在$E$一致收敛。若函数级数的部分和一致收敛，则称函数级数一致收敛。

一致收敛的蕴含性质：

1. 柯西收敛：$\{f_n\}$一致收敛于$E$，当且仅当$\forall\varepsilon\gt0,\exists N\in\mathbb N$使$\forall m,n\geq N,\forall x\in E$有$|f_m(x)-f_n(x)|\leq\varepsilon$。
2. $M_n=\sup_{x\in E}|f_n(x)-f(x)|$，则$\{f_n\}$一致收敛于$f$当且仅当$\lim_{n\rightarrow\infty}M_n=0$。
3. 若对$x\in E,n\in\mathbb N$有$|f_n(x)|\leq M_n$且$M_n$收敛，则$\sum f_n$一致收敛。

一致收敛和连续性：$\{f_n\}$是$E$上的连续函数序列，若$\{f_n\}$一致收敛于$f$，则$f$在$E$连续。

1. 紧集上的连续函数序列$\{f_n\}$逐点收敛到连续函数$f$，且$f_n(x)\geq f_{n+1}(x)$对$\forall x,\forall n\in\mathbb N$成立，则$\{f_n\}$一致收敛于$f$。



## 4. 幂级数

### 幂级数

形如$f(x)=\sum c_n(x-a)^n$的函数称为解析函数，形如$\sum c_n z^n$的级数称为幂级数。

幂级数的蕴含性质：

1. $\sum c_nx^n$在$|x|\lt R$收敛，设$f(x)=\sum c_nx^n$，则$\forall\varepsilon\gt0$有$\sum c_nx^n$在$[-R+\varepsilon,R-\varepsilon]$一致收敛。$f$在$(-R,R)$任意阶可导，$f^{(k)}(x)=\sum_{n=k}^\infty\frac{n!}{(n-k)!}c_nx^{n-k}$，$f^{(k)}(0)=k!c_k$。
2. 两个收敛到相同函数的幂级数相等。



### 指数函数的定义

$\mathrm e^x$的定义：$E(z)=\sum \frac{z^n}{n!}$，该级数对任意复数$z$收敛。

1. $E(z)E(w)=E(z+w),E'(z)=E(z),E(n)=E(1+...+1)=\mathrm e^n$。
2. $E(\frac nm)^m=E(n)=\mathrm e^n$，故$\forall p\in\mathbb Q$，$E(p)=\mathrm e^p$。
3. $\forall x\in\mathbb R$，定义$E(x)=\sup\mathrm e^p,p\in\mathbb Q\land p\lt x$，可证$E(x)=\mathrm e^x$。

$\log x$的定义：$\mathrm e^x$在$\mathbb R$上严格单增且连续可导，存在反函数$L$，$E(L(y))=y,L(E(x))=x$。

1. $L'(E(x))=\frac1{E'(x)}=\frac1{E(x)}$，因此$L'(x)=\frac1x$。
2. $L(E(x)E(y))=L(E(x+y))=x+y$，故$L(uv)=L(u)+L(v)$。
3. $L(1)=0$，故$L(x)=\int_1^x\frac1tdt$，记为$\log x$。

指数函数的定义：

1. $E(L(x))=x$，故$E(nL(x))=x^n$。
2. $\forall p\in\mathbb Q$，$x^p=E(pL(x))=\mathrm e^{p\log x}$。
3. $\forall \alpha\in\mathbb R$，定义$x^\alpha=\sup\mathrm e^p,p\in\mathbb Q\land p\lt\alpha$，可证$x^\alpha=\mathrm e^{\alpha\log x}$。
4. 进一步有$(x^\alpha)'=\alpha x^{\alpha-1}$。

指数和对数函数的性质：

1. $\lim_{x\rightarrow+\infty}x^n\mathrm e^{-x}=0$。
2. $\lim_{x\rightarrow+\infty}x^{-\alpha}\log x=0$。



### 三角函数的定义

三角函数的定义：$C(x)=\frac12(E(\mathrm ix)+E(-\mathrm ix)),S(x)=\frac12(E(\mathrm ix)-E(-\mathrm ix))$

1. $E(\mathrm ix)=C(x)+\mathrm iS(x)$。
2. $C(0)=1,S(0)=0,C'(x)=-S(x),S'(x)=C(x)$。
3. $\exists x_0$使$C(x_0)=0$，设$x_0$是满足$C(x_0)=0$的最小正数。
4. 定义$\pi=2x_0$，可得$C(\frac\pi2)=0,S(\frac\pi2)=1,E(\frac\pi2\mathrm i)=\mathrm i$，于是$E(\pi\mathrm i)=-1,E(2\pi\mathrm i)=1,E(z+2\pi\mathrm i)=E(z)$。
5. $\cos x=C(x),\sin x=S(x)$。

三角函数的蕴含性质：

1. $\mathrm e^z$有周期$2\pi\mathrm i$，$\sin,\cos$有周期$2\pi$。
2. $\mathrm e^{\mathrm ix},x\in[0,2\pi)$形成复坐标系的单位圆，弧长为$2\pi$。



## 5. 傅立叶级数



