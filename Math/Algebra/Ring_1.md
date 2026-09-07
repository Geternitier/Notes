# Ring_1



## 1. 引论

### 代数定义

**环**$R$是一个集合以及定义在集合上的基本运算$+$和$\times$，称为加法和乘法，满足

1. $(R,+)$构成交换群；
2. $\times$ 满足结合律：$(a\times b)\times c=a\times(b\times c)$；
3. $\times$对$+$满足左右分配律：
   1. $(a+b)\times c=(a\times c)+(b\times c)$；
   2. $a\times(b+c)=(a\times b)+(a\times c)$。

环称为**交换环**，当$\times$满足交换律，即$a\times b=b\times a$。

环称为**有单位元的环**，或**含1环**，当存在$1\in R$满足$\forall a\in R$有$1\times a=a\times1=a$。

1. 通常，简写$a\times b$为$ab$。
2. 加法单位元用$0$表示，$a$的加法相反数记为$-a$。

环的基本性质：

1. $\forall a\in R$有$0a=a0=0$；
2. $\forall a,b\in R$有$(-a)b=a(-b)=-(ab)$；
3. $\forall a,b\in R$有$(-a)(-b)=ab$；
4. 若$R$含1，则1是唯一的，且$\forall a\in R$有$-a=(-1)a$。

环的示例：

1. 任意交换群$R$，附加乘法$\forall a,b\in R,ab=0$所定义的交换环称为**平凡环**；
2. 平凡群构造的平凡环$R=\{0\}$称为**零环**，记为$R=0$，是唯一满足$1=0$的环。
3. $\mathbb Z,\mathbb Q,\mathbb R,\mathbb C$都是含1交换环。$2\mathbb Z$是不含1交换环。



环引申的定义：

1. $1\ne0$的含1环$R$，且$\forall a\in R$存在$b\in R$使$ab=ba=1$，称$R$为**除环**；交换除环称为**域**。
2. 非零元$a\in R$称为$R$的**零因子**，当存在非零元$b\in R$使$ab=0$或$ba=0$。
3. $1\ne0$的含1环$R$，$u\in R$称为**单元**，当存在$v\in R$满足$uv=vu=1$，$R$的单元集记为$R^\times$。
   1. $R^\times$的乘法构成群，域是所有非零元都为单元的含$1\ne0$交换环。
   2. 零因子一定不是单元，域不含零因子。
4. 无零因子的含$1\ne0$交换环称为**整环**。
5. 环$R$的**子环**是$R$满足乘法封闭的子群。