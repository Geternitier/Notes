# 一、逻辑和空间



## 1. 逻辑

常用逻辑符号：

1. $\land$表示"与"或"且"，$\lor$表示"或"，$\neg$表示"非"。
2. $\forall$表示"对任意"，$\exists$表示"存在"。
3. $\Longrightarrow$表示"蕴含"，$\Longleftrightarrow$表示"当且仅当"或"等价于"。
4. ","按使用场合，可表示"蕴含"或"与"等。



### 集合

**集合**是指一些对象的全体，这些对象称为集合的元素。

- 常用大写字母A、B、C表示集合，用小写字母a、b、c表示集合的元素。
  - $a\in A$表示a是A的元素，$a\notin A$表示a不是A的元素。
  - $a=b$表示a和b是相同元素，$A=B$表示A和B为相同集合。
  - $A\subset B$表示A对所有元素都在B中，称A为B的子集。
    - 有时用$A\subseteq B$表示A是B的子集且A和B可能相等，此时用$A\subset B$表示A是B的子集且A和B不相等，也称A为B的真子集。

集合公理：对集合的一些直觉的显式规定。通过这些规定可以构造出所有集合。

1. 空集公理：存在不含任何元素的集合，称为空集，记为$\varnothing$。
2. 外延公理：具有相同元素的集合是相同的集合。
3. 无序对公理：任意元素x、y，存在集合恰好含有x、y。
4. 并集公理：设F为一族集合，存在A满足$\forall x\in A\Longleftrightarrow \exists X\in F有x\in X$。A称为F的并集。
5. 幂集公理：集合A的所有子集构成一个集合，称为A的幂集。
6. 无穷公理：存在具有无限个元素的集合。
7. 分离公理：可以在集合A中按某种方式挑选一些元素构成一个新的集合。
8. 替换公理：可以按照某种映射关系从集合A构造新集合B。即$B=\{F(x):x\in A\}$。
9. 正则公理：$\forall A\neq\varnothing,\exists a\in A使a\cap A\neq\varnothing$。
10. 选择公理：一族非空且两两不交的集合，可以在其中每个集合选一个元素组成一个集合。



### 关系

两个元素的组合$(x,y)$，满足$(x,y)=(u,v)\Longleftrightarrow x=u\land y=v$，则称其为一个**有序对**，有序对的集合称为**关系**。

- 笛卡尔积：一个集合的元素对应另一个集合的元素构成的关系称为笛卡尔积，即$\{(x,y):x\in A,y\in B\}$。
- 函数：若对关系R中每个有序对的左值x，存在唯一(x,y)属于R，则称该关系为一个函数。

关系的研究性质：

1. 自反性：$\forall x\in A有(x,x)\in R$，称关系R在A上自反。
   - 禁自反性：$\forall x\in A,(x,x)\notin R$。
2. 对称性：$\forall (x,y)\in R有(y,x)\in R$，称关系R有对称性。
   - 反对称性：$\forall x,y\in A$有$(x,y)\in R\land (y,x)\in R\Longleftrightarrow x=y$。
   - 禁对称性：$\forall (x,y)\in R,(y,x)\notin R$。
3. 传递性：$(x,y)\in R\land (y,z)\in R\Longrightarrow (x,z)\in R$，称关系R有传递性。
4. 等价关系：R在A上满足自反性、对称性和传递性，称R在A上为等价关系。
5. 三分性：$\forall x,y\in A$，三种情形$(x,y)\in R;(y,x)\in R;x=y$仅有一种成立，称关系R在A上有三分性。
6. 逆关系：$R^{-1}={(y,x):(x,y)\in R}$称为R的逆关系。
7. 序关系：R在A上满足传递性和三分性，则R在A上为序关系。具备序关系的集合称为有序集。
8. 偏序关系$\leq$：R在A上满足自反性、反对称性和传递性，称R在A上为偏序关系。
   - 严格偏序$\lt$：R在A上满足禁自反性、禁对称性和传递性，称R在A上为严格偏序关系。
   - 全序关系：R在A上为偏序关系，且$\forall x,y\in A有(x,y)\in R\lor (y,x)\in R$，称R在A上为全序关系。
   - 良序关系：具有偏序极小元的全序关系称为良序关系。
     - 偏序极小元：关系R偏序集合A，$\exists b\in A,\forall x\in A\land x\neq b,(b,x)\in R$，称b为A在R偏序下的极小元。
   - 任何集合都可以被良序$\Longleftrightarrow$选择公理。
   - 上界：$E\subset S,\exists x\in S,\forall y\in E有y\lt x$，称x为E的**上界**；进一步，若$\forall z\in S\land z\lt x$有z不是E的上界，则x为E的**上确界**。
   - 上确界性质：$\forall E\subset S,E\neq\varnothing\land E有上界\Longrightarrow E有上确界$，称关系R在S上具有上确界性质。



### 有限和可数

若关系$f$将集合$A$中的每一个元素对应到集合B中的某个元素，称$f$为$A$到$B$的一个函数/映射，称$A$为函数的定义域，设$f(A)=\{f(x):x\in A\}$，称为$f$的值域或$A$在$f$下的像集。

- 若$f(A)=B$，称$f$为满射。
- 若$\forall x,y\in A,x\neq y\Longleftrightarrow f(x)\neq f(y)$，称$f$为单射。
- 若$f$既是单射，也是满射，则称其为一一映射，或一一对应。

等势：若集合A和B上有一一映射，称A和B等势，记为$A\sim B$。

- 有限：和$\{1,2,...,n\}$等势。
- 无限：不和$\{1,2,...,n\}$等势。
- 可数：和$\mathbb N$等势
- 不可数：既不有限，也不可数

序列是$\mathbb N$一一映射的一个像集，$x_n=f(n)$。

- 序列的子列仍然是序列$\Longleftrightarrow$可数集的无限子集仍然可数（可数集是"最小"的无限集）

有理数集可数，实数集不可数。



## 2. 空间

具有一定结构的集合称为空间。

### 域

域是满足域公理（加法公理、乘法公理和乘法分配律）的集合。域公理如下：

1. 加法公理

   - 封闭：$\forall x,y\in F,x+y\in F$。
   - 交换律：$\forall x,y\in F,x+y=y+x$。
   - 结合律：$\forall x,y,z\in F,x+(y+z)=(x+y)+z$。
   - 零元：$\exists 0\in F,\forall x\in F,x+0=x$。（0特指可作为加法零元的元素）

   - 逆元：$\forall x\in F,\exists -x\in F,-x+x=0$。

2. 乘法公理

   - 封闭：$\forall x,y\in F,xy\in F$。
   - 交换律：$\forall x,y\in F,xy=yx$。
   - 结合律：$\forall x,y,z\in F,x(yz)=(xy)z$。
   - 单位元：$\exists 1\in F,\forall x\in F,1x=x$。（1特指可作为乘法单位元的元素）
   - 逆元：$\forall x\in F\land x\neq 0,\exists x^{-1}\in F,x^{-1}x=1$。

3. 分配律：$\forall x,y,z\in F,(x+y)z=xz+yz$。

具备序关系，且满足加法保序（$x+y\lt x+z\Longleftrightarrow y\lt z$）和乘法保正（$x\gt0\land y\gt0\Longrightarrow xy\gt0$）的域称为有序域。

有理数集$\mathbb Q$是不具有上确界性质的有序域。



### 实数域

实数域的构造：

1. 定义$\mathbb Q$的一个分割$\alpha$，满足：

   1. $\alpha\subseteq\mathbb Q$
   2. $\alpha\neq\varnothing$
   3. 若$p\in\alpha,q\in\mathbb Q$且$q\lt p$则$q\in\alpha$。
   4. 若$p\in\alpha$则$\exists r\in\alpha$使$p\lt r$。（分割无最大元）

   $\mathbb R$是$\mathbb Q$的所有分割的集合。

2. $\mathbb R$的序关系：$\forall\alpha,\beta\in\mathbb R,\alpha<\beta\Longleftrightarrow\alpha\subset\beta$。

3. $\mathbb R$的加法：$\forall\alpha,\beta\in\mathbb R\Longrightarrow\alpha+\beta=\{r+s:r\in\alpha,s\in\beta\}$。

4. $\mathbb R$的乘法：

   - $\alpha=0\lor\beta=0\Longrightarrow\alpha\beta=0$
   - $\forall\alpha,\beta\in\mathbb R,\alpha,\beta\gt0\Longrightarrow\alpha\beta=\{rs:r\in\alpha,s\in\beta\}$
   - $\forall\alpha,\beta\in\mathbb R,\alpha\lt0,\beta\gt0\Longrightarrow\alpha\beta=(-\alpha)\beta$
   - $\forall\alpha,\beta\in\mathbb R\land\alpha\lt0,\beta\lt0\Longrightarrow\alpha\beta=(-\alpha)(-\beta)$
   - $\forall\alpha,\beta\in\mathbb R\land\alpha\gt0,\beta\lt0\Longrightarrow\alpha\beta=\alpha(-\beta)$

5. 于是$\mathbb R$作为有序域，包含$\mathbb Q$且具有上确界性质。

实数域的蕴含性质：

1. 阿基米德Archimedean性质：$x\in\mathbb R^+,y\in\mathbb R\Longrightarrow \exists n\in\mathbb N,nx>y$。

2. 实数域上有理数的稠密性：$\forall x,y\in\mathbb R,x\lt y\Longrightarrow \exists p\in\mathbb Q,x\lt p\lt y$。

3. 可构造实数幂运算，并满足$a^{x+y}=a^xa^y,a^{xy}=(a^x)^y,(ab)^x=a^xb^x$：

   1. 整数次幂和整数次根：$m,n\in\mathbb N^+,a\in\mathbb R$

      - $a^n$ 即n个a的积。由乘法封闭性，$a^n\in\mathbb R$。
      - $a^{-n}=(a^n)^{-1}$。由乘法单位元性质，$a^{-n}\in\mathbb R$。

      - $a^{\frac1n}=\{x\in\mathbb Q:\exists y\in\mathbb Q,y\gt x,y^n<a\}$。

   2. 有理数次幂：$m,n\in\mathbb N,a\in\mathbb R$。$a^{\frac mn}=(a^m)^{\frac1n}$。

   3. 实数次幂：$x,y,a\in\mathbb R$。$a^x=\{t\in\mathbb Q:\exists p\in x,t\lt a^p\}$

实数域的扩充：添加符号$-\infty$和$+\infty$。

1. $\forall x\in\mathbb R,-\infty<x<+\infty$。
2. $x+\infty=+\infty,x-\infty=-\infty$。
3. $x\gt0,x\cdot+\infty=+\infty,x\cdot-\infty=-\infty$。
4. $\frac x{+\infty}=\frac x{-\infty}=0$



### 复数域

复数域的构造：

1. 复数是实数的有序对。
2. 定义复数加法$(a,b)+(c,d)=(a+c,b+d)$，零元$(0,0)$
3. 定义复数乘法$(a,b)\cdot(c,d)=(ac-bd,ad+bc)$，单位元$(0,1)$。
4. 于是复数构成一个域。

定义$i=(0,1)$，则$\forall a,b\in\mathbb R,z=(a,b)=a+bi$。称a为实部，记为$\Re(z)$，b为虚部，记为$\Im(z)$。称$\overline z=a-bi$为z的共轭复数。

复数的蕴含性质：

1. $\overline{z+w}=\overline z+\overline w,\overline{zw}=\overline z\cdot\overline w$。
2. $z+\overline z=2\operatorname{Re}(z),z-\overline{z}=2\operatorname{Im}(z)$。
3. $z\cdot\overline z=a^2+b^2>0$。定义复数的绝对值$|z|=\sqrt{z\cdot\overline z}$。
4. 复数的施瓦茨不等式：$|\sum_{i=1}^na_i\overline{b_i}|^2\leq\sum_{i=1}^n|a_i|^2\sum_{i=1}^n|b_i|^2$



### 欧氏空间

$\forall k\in\mathbb N$，设$\mathbb R^k$为有序$k$元序列$\vec x=(x_1,...,x_k)$的集合，其中$x_1,...,x_k\in\mathbb R$，称为$\vec x$的坐标。$\mathbb R^k$的元素称为点或向量。

设$\vec x=(x_1,...,x_k),\vec y=(y_1,...,y_k)$，定义

- $\vec x+\vec y=(x_1+y_1,...,x_k+y_k)$
- $a\vec x=(ax_1,...,ax_k)$
- $\vec x\cdot\vec y=\sum_{i=1}^kx_iy_i$，称为$\vec x,\vec y$的内积。
- $|\vec x|=(\sum_{i=1}^kx_i^2)^{\frac12}$，称为$\vec x$的模。

称向量空间$\mathbb R^k$为$k$维欧氏空间。

欧氏空间的蕴含性质：

1. $|\vec x|\geq 0$；
2. $|a\vec x|=|a||\vec x|$；
3. $|\vec x\cdot\vec y|\leq|\vec x||\vec y|$；
4. $|\vec x+\vec y|\leq|\vec x|+|\vec y|,|\vec x-\vec z|\leq|\vec x-\vec y|+|\vec y-\vec z|$（三角不等式）。

欧氏空间的基本概念：

1. 开区间segment：$(a,b)=\{x:a<x<b,x\in\mathbb R\}$
2. 闭区间interval：$[a,b]=\{x:a\leq x\leq b,x\in\mathbb R\}$
3. k维闭区间/方体/胞腔，k-cell：$\{\vec x:\forall i=1,...,k,a_i\leq x_i\leq b_i,x_i\in\mathbb R\}$
4. 凸集convex：$\forall x,y\in E,0\lt\lambda\lt1$有$\lambda x+(1-\lambda)y\in E$，称$E$为凸集。



### 度量空间

集合X和以X中任意两点为参数的距离函数d，若满足

- $d(p,q)\geq0$且仅当$p=q$取等
- $d(p,q)=d(q,p)$
- $d(p,q)+d(q,r)\geq d(p,r)$

称这样的空间为度量空间。

度量空间的研究概念：度量空间$X$，集合$E\subset X$。

1. 邻域：点p的半径为r的邻域$N_r(p)=\{q:d(p,q)\lt r\}$。
2. 聚点：点p的所有邻域都含有满足$q\in E\land q\neq p$的点q，称p为E的聚点。
   - 孤立点：$p\in E$且p不是E的聚点，称p为E的孤立点。
   - 闭集：E的所有聚点属于E，称E为闭集。
   - 闭包closure：设$E'$为$E$在$X$中聚点的集合，则$E\cup E'$称为$E$的闭包。
   - 完备集perfect：E为闭集且E的所有点为聚点，称E为完备集。
   - 稠密：E在X稠密表示X的每个点是E的聚点或属于E。
3. 内点：$\exists r$使$N_r(p)\subset E$，称p为E的内点。
   - 开集：E的所有点是内点，称E为开集。
4. 有界：$\exists M\in\mathbb R,\forall p,q\in E$有$d(p,q)\lt M$，称E有界。
   - $\{d(x,y):x,y\in E\}$的上确界称为集合的直径。
5. 分离和连通：
   - 分离：度量空间的两个子集A和B，若$\overline A\cap B=\varnothing\land A\cap\overline B=\varnothing$，称A和B分离。
   - 连通：E为连通集，则E不是两个分离集合的并。

度量空间的蕴含性质：

1. 邻域都是开集。
2. 有限集没有聚点，有聚点的集合都是无限集。
3. $E$为开集当且仅当$E$在$X$的补集为闭集。
   - $E$为闭集当且仅当$E$在$X$的补集为开集。
4. 开集的并是开集，闭集的交是闭集。
   - 有限个开集的交是开集，有限个闭集的并是闭集。
5. 设$E\subset Y\subset X$，E为开集当且仅当存在开集$G\subset X,E=Y\cap G$。
   - $E$对$Y$为开集，意味着E的所有点在Y的邻域为E的内点，但在X中可能不是
   - E是否为开集或者闭集取决于它嵌入的集合，E可以对Y开而对X不开，闭也是类似的。这就引出了对集合紧致性的讨论。



### 紧致性

集合E在度量空间X上的开覆盖是满足$E\subset\bigcup_\alpha G_\alpha$的集合$\{G_\alpha\},G_\alpha\subset X$。

度量空间X的子集K的任意开覆盖包含有限子覆盖，称K是**紧致**的，也称紧的。

紧致性的蕴含性质：

1. $K\subset Y\subset X$，$K$对$X$紧致当且仅当$K$对$Y$紧致。
2. 度量空间的紧致子集为闭集。
3. 紧集的闭子集是紧集。
4. 闭集和紧集的交是紧集。
5. 度量空间的子集族$\{K_\alpha\}$，$K_\alpha$紧且$\{K_\alpha\}$的任意有限子集族的交非空，则$\bigcup_\alpha\{K_\alpha\}\neq\varnothing$。
6. 紧集的无限子集在紧集中有聚点。

欧氏空间和紧致性的蕴含性质：

1. $E\subset\mathbb R$是紧集$\Longleftrightarrow E$是有界闭集。
   - 非紧集包含无界集（无穷区间、无限点集如$\mathbb Z$）、有界开集。
2. 闭区间套原理：
   - $\mathbb R$的闭区间序列$\{I_n\}$有$I_{n-1}\subset I_n$，则$\bigcap_{n=1}^\infty I_n\neq\varnothing$。
   - $\mathbb R^k$的闭k方体序列$\{I_n\}$有$I_{n-1}\subset I_n$，则$\bigcap_{n=1}^\infty I_n\neq\varnothing$。
3. k维闭区间是紧集。
4. $\mathbb R^k$中的集合E具有下述的某两条性质，那么它也具备第三条：
   1. E闭且有界
   2. E紧
   3. E的每个无限子集在E中有聚点
5. $\mathbb R^k$的每个有界无限子集都在$\mathbb R^k$中有聚点。
6. $\mathbb R^k$的非空完备子集不可数。