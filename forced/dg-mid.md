# 微分几何 — 期中考试

## 定义 1.3.2 (合同变换的结构)

设 $T$ 是 $\mathbb E^n$ 上的合同变换, 则 $T\left(\boldsymbol x\right)=\boldsymbol xT+P$, 其中 $T\in O\left(n\right)$, $P\in\mathbb E^n$; 当 $\det T=1$ 时称为刚体运动, 当 $\det T=-1$ 时称为反向刚体运动.

## 定义 2.1.1 (正则曲线)

曲线 $\boldsymbol r:\left(a,b\right)\to E^2\left(E^3\right)$ 称为正则曲线, 是指 (1) 每一个分量都是 $C^{\infty}$ 函数; (2) $\left|\boldsymbol r'\left(t\right)\right|> 0$, $\forall\,t\in\left(a,b\right)$ 成立.

## 定义 2.2.1 (弧长与弧长参数)

曲线 $\boldsymbol r\left(t\right)$, $t\in\left[c,d\right]$, 的弧长为 $\int_c^d\left|\boldsymbol r'\left(t\right)\right|\mathrm dt$; 弧长函数 $s\left(t\right)=\int_c^t\left|\boldsymbol r'\left(u\right)\right|\mathrm du$ 严格单调, 可把参数换为弧长参数 $s$, 此时 $\left|\frac{\mathrm d\boldsymbol r}{\mathrm ds}\right|\equiv1$; 反之, 若参数 $t$ 满足 $\left|\frac{\mathrm d\boldsymbol r}{\mathrm dt}\right|\equiv1$, 则 $t$ 是弧长参数.

## 定义 2.2.2 (平面曲线的曲率与弗勒内标架)

对平面曲线 $\boldsymbol r\left(s\right)$, 取单位切向量 $\boldsymbol t$ 与单位法向量 $\boldsymbol n$ 使 $\left\{\boldsymbol t,\boldsymbol n\right\}$ 为右手系, 则 $\left[\boldsymbol r\left(s\right);\boldsymbol t\left(s\right),\boldsymbol n\left(s\right)\right]$ 是沿曲线的弗勒内标架, 且 $\dot{\boldsymbol t}=k\boldsymbol n$, $\dot{\boldsymbol n}=-k\boldsymbol t$; 函数 $k\left(s\right)$ 称为曲线的有向曲率.

## 例 2.2.2 (曲率为常数的曲线)

(1) $k\left(s\right)\equiv0$ 时 $\boldsymbol r$ 是直线;

(2) $k\left(s\right)$ 为非零常数时 $\boldsymbol r$ 是半径 $\frac1{\left|k\right|}$ 的圆 (或它的一部分).

## 定义 2.2.3 (弧长参数化)

固定起点 $a$, 定义 $s\left(t\right):=\int_a^t\left|\boldsymbol r'\left(u\right)\right|\,\mathrm du$; 因 $s'\left(t\right)=\left|\boldsymbol r'\left(t\right)\right|> 0$, $s$ 是 $t$ 的严格单调增函数, 故 $t$ 可反解为 $t=t\left(s\right)$, 得到弧长参数化 $\boldsymbol r\left(s\right):=\boldsymbol r\left(t\left(s\right)\right)$, 此时 $\left|\frac{\mathrm d\boldsymbol r}{\mathrm ds}\right|\equiv1$.

## 命题 2.2.4 (弧长参数的判别)

在曲线 $\boldsymbol r$ 的所有同定向参数中, 使曲线速度为 $1$ 的参数是唯一的, 即弧长参数; 故参数 $t$ 是弧长参数当且仅当 $\left|\frac{\mathrm d\boldsymbol r}{\mathrm dt}\right|\equiv1$.

## 定义 2.3.1 (法平面)

与 $\boldsymbol t\left(s\right)$ 垂直的向量称为曲线在该点的法向量; 法向量全体构成过该点并与 $\boldsymbol t$ 垂直的平面, 称为曲线在该点的法平面.

## 定义 2.3.1 (空间曲线的曲率与弗勒内标架)

对弧长参数空间曲线 $\boldsymbol r\left(s\right)$, 记曲率 $k\left(s\right)=\left|\dot{\boldsymbol t}\left(s\right)\right|$; 当 $k0$ 时主法向量 $\boldsymbol n=\dot{\boldsymbol t}/k$, 副法向量 $\boldsymbol b=\boldsymbol t\wedge\boldsymbol n$, $\left[\boldsymbol r;\boldsymbol t,\boldsymbol n,\boldsymbol b\right]$ 是弗勒内标架; 挠率 $\tau=\left\langle\dot{\boldsymbol n},\boldsymbol b\right\rangle$.

## 定理 2.3.1 (挠率为零 $\Leftrightarrow$ 平面曲线)

设空间曲线 $\boldsymbol r$ 的曲率 $k> 0$, 则 $\boldsymbol r$ 落在某个平面上的充要条件是 $\tau\equiv0$.

## 定义 2.3.2 (曲率)

记 $k\left(s\right)=\left|\dot{\boldsymbol t}\left(s\right)\right|$, 称 $k\left(s\right)$ 为曲线 $\boldsymbol r$ 的曲率.

## 例 2.3.2 (圆柱螺线)

圆柱螺旋线 $\boldsymbol r\left(t\right)=\left(a\cos t,a\sin t,bt\right)$ ($a> 0$) 的曲率和挠率都是常数.

## 定义 2.3.3 (主法向量)

当 $k\left(s\right)> 0$ 时, 由 $\dot{\boldsymbol t}\left(s\right)$ 决定的单位向量 $\boldsymbol n\left(s\right):=\frac{\dot{\boldsymbol t}\left(s\right)}{\left|\dot{\boldsymbol t}\left(s\right)\right|}$ 称为曲线 $\boldsymbol r$ 的主法向量.

## 定理 2.3.3 (弧长参数曲线的二阶渐近展开)

设 $\boldsymbol r$ 以弧长为参数, 在 $s_0=0$ 处有

$$
\boldsymbol r\left(s\right)=\boldsymbol r\left(0\right)+s\,\dot{\boldsymbol r}\left(0\right)+\frac{s^{2}}2\ddot{\boldsymbol r}\left(0\right)+O\left(s^{3}\right),
$$

其中 $\dot{\boldsymbol r}=\boldsymbol t\left(0\right)$, $\ddot{\boldsymbol r}\left(0\right)=k\left(0\right)\boldsymbol n\left(0\right)$.

## 定义 2.3.4 (副法向量)

令 $\boldsymbol b\left(s\right):=\boldsymbol t\left(s\right)\wedge\boldsymbol n\left(s\right)$, 称 $\boldsymbol b$ 为曲线 $\boldsymbol r$ 的副法向量.

## 定义 2.3.5 (弗雷内标架)

$\left\{\boldsymbol r\left(s\right);\boldsymbol t\left(s\right),\boldsymbol n\left(s\right),\boldsymbol b\left(s\right)\right\}$ 称为空间曲线的弗雷内标架.

## 定义 2.3.6 (密切平面)

弗雷内标架的三根坐标轴分别称为曲线的切线、主法线和副法线; 三个坐标平面分别称为曲线在该点的法平面 (以 $\boldsymbol t$ 为法向量)、密切平面 (以 $\boldsymbol b$ 为法向量) 和从切平面 (以 $\boldsymbol n$ 为法向量).

## 定义 2.3.7 (挠率)

记 $\tau=\left\langle\dot{\boldsymbol n},\boldsymbol b\right\rangle$, 称函数 $\tau$ 为曲线 $\boldsymbol r$ 的挠率.

## 定理 2.3.10 (弗雷内公式)

弗雷内标架随弧长 $s$ 的变化满足 $\dot{\boldsymbol t}=k\boldsymbol n$, $\dot{\boldsymbol n}=-k\boldsymbol t+\tau\boldsymbol b$, $\dot{\boldsymbol b}=-\tau\boldsymbol n$.

## 性质 2.4.1 (弧长, 曲率, 挠率的刚体运动不变性)

$\mathbb E^{3}$ 中曲线的弧长, 曲率和挠率在刚体运动下不变.

## 定理 2.4.2 (空间曲线基本定理)

(1) 设 $\boldsymbol r_1,\boldsymbol r_2$ 是 $\mathbb E^3$ 的两条弧长参数曲线, 定义在同一参数区间上, 且 $k_1=k_2> 0$, $\tau_1=\tau_2$, 则存在 $\mathbb E^3$ 的一个刚体运动把 $\boldsymbol r_2$ 变为 $\boldsymbol r_1$; (2) 设 $k=k\left(s\right)$, $\tau=\tau\left(s\right)$ 是连续可微函数且 $k\left(s\right)> 0$, 则存在以 $s$ 为弧长参数、以 $k$ 和 $\tau$ 为曲率和挠率的弧长参数曲线.

## 定理 2.4.3 (给定曲率挠率存在弧长参数曲线)

设 $k=k\left(s\right)$ 和 $\tau=\tau\left(s\right)$ 是定义在区间 $\left(a,b\right)$ 上的两个连续可微函数, 且 $k\left(s\right)0$, 则存在以 $s$ 为弧长参数, 以 $k$ 为曲率, 以 $\tau$ 为挠率的空间曲线.

## 定理 2.4.4 (平面曲线基本定理)

设 $k\left(s\right)$ 是连续可微函数, 则 (1) 存在平面 $E^2$ 的曲线 $\boldsymbol r\left(s\right)$, 它以 $s$ 为弧长参数、以 $k\left(s\right)$ 为曲率; (2) 上述曲线在相差平面的一个刚体运动的意义下是唯一的.

## 例 2.4.5 (曲率挠率均为常数的曲线分类)

设 $\boldsymbol r$ 是 $\mathbb E^3$ 的曲线, 它的挠率 $\tau$ 和曲率 $\kappa$ 是常数: (1) $\kappa=0$, 这时 $\boldsymbol r$ 是直线; (2) $\kappa> 0$, $\tau=0$ 时, $\boldsymbol r$ 是圆; (3) $\kappa> 0$, $\tau\ne0$, 由空间曲线基本定理及圆柱螺线例知 $\boldsymbol r$ 是圆柱螺旋线.

## 习题 2.4.5 (一般参数下的曲率与挠率公式)

设 $\boldsymbol r\left(t\right)$ 是 $\mathbb E^3$ 的正则曲线, 则其曲率和挠率分别为 $k\left(t\right)=\frac{\left|\boldsymbol r'\wedge\boldsymbol r''\right|}{\left|\boldsymbol r'\right|^{3}}$, $\tau\left(t\right)=\frac{\left(\boldsymbol r',\boldsymbol r'',\boldsymbol r'''\right)}{\left|\boldsymbol r'\wedge\boldsymbol r''\right|^{2}}$, 其中 $\left(\cdot,\cdot,\cdot\right)$ 为混合积.

## 定义 3.1.1 (参数曲面)

设 $D\subset\mathbb R^{2}$ 是平面区域, 映射 $\boldsymbol r:D\to E^{3}$, $\boldsymbol r\left(u,v\right)=\left(x\left(u,v\right),y\left(u,v\right),z\left(u,v\right)\right)$ 满足: (1) 每个分量函数是无限阶连续可微的; (2) 向量 $\boldsymbol r_{u}=\left(x_{u},y_{u},z_{u}\right)$, $\boldsymbol r_{v}=\left(x_{v},y_{v},z_{v}\right)$ 线性无关, 即 $\boldsymbol r_{u}\wedge\boldsymbol r_{v}\ne\boldsymbol0$. 此时称 $\boldsymbol r$ 是 $E^{3}$ 的一个曲面 (片), $\left(u,v\right)$ 称为曲面的 (坐标) 参数.

## 定义 3.1.2 (切平面)

$\boldsymbol r_{u}\left(a,b\right)$ 和 $\boldsymbol r_{v}\left(a,b\right)$ 张成与曲面 $S$ 相切于 $P_{0}$ 点的一张平面, 称为曲面 $S$ 在 $P_{0}$ 点的切平面, 记为 $T_{P_{0}}S$; $\boldsymbol r_{u}\left(a,b\right)$ 和 $\boldsymbol r_{v}\left(a,b\right)$ 称为曲面在 $P_{0}$ 点的坐标切向量.

## 推导 3.1.2 (参数变换下法向)

设 $\left(u,v\right)\to\left(\widetilde u,\widetilde v\right)$ 是参数变换, 雅可比行列式 $J:=\frac{\partial\left(u,v\right)}{\partial\left(\widetilde u,\widetilde v\right)}$, 则 $\boldsymbol r_{\widetilde u}\wedge\boldsymbol r_{\widetilde v}=\det J\,\boldsymbol r_u\wedge\boldsymbol r_v$; 因而同向参数变换 ($\det J> 0$) 不改变单位法向 $\boldsymbol n$, 反向参数变换 ($\det J< 0$) 使 $\boldsymbol n$ 变号.

## 定义 3.1.3 (单位法向量)

$\boldsymbol r_{u}\wedge\boldsymbol r_{v}$ 是与 $\boldsymbol r_{u}$ 和 $\boldsymbol r_{v}$ 均正交的向量, 是曲面 $S$ 在该点的一个法向量; 由正则性 $\boldsymbol r_{u}\wedge\boldsymbol r_{v}\ne\boldsymbol0$, 每点有确定的单位法向量 $\boldsymbol n=\frac{\boldsymbol r_{u}\wedge\boldsymbol r_{v}}{\left|\boldsymbol r_{u}\wedge\boldsymbol r_{v}\right|}$, 且 $\left\{P;\boldsymbol r_{u},\boldsymbol r_{v},\boldsymbol n\right\}$ 构成 $E^{3}$ 的一个自然定向的标架.

## 例 3.1.5 (等值面)

等值面 $S_c=\left\{\left(x,y,z\right)\mid F\left(x,y,z\right)=c\right\}$: 当 $\nabla F\left(P\right)\neq\boldsymbol0$ ($\forall P\in S_c$) 时 $S_c$ 是曲面, $\nabla F$ 是 $S_c$ 的法向, 且 $S_c$ 在 $P_0=\left(x_0,y_0,z_0\right)$ 的切平面方程为

$$
F_x\left(P_0\right)\left(x-x_0\right)+F_y\left(P_0\right)\left(y-y_0\right)+F_z\left(P_0\right)\left(z-z_0\right)=0.
$$

## 定义 3.2.1 (第一基本形式)

设 $E=\left\langle\boldsymbol r_{u},\boldsymbol r_{u}\right\rangle$, $F=\left\langle\boldsymbol r_{u},\boldsymbol r_{v}\right\rangle$, $G=\left\langle\boldsymbol r_{v},\boldsymbol r_{v}\right\rangle$, 二次微分式

$$
I=E\,\mathrm du\,\mathrm du+2F\,\mathrm du\,\mathrm dv+G\,\mathrm dv\,\mathrm dv=\left\langle\mathrm d\boldsymbol r,\mathrm d\boldsymbol r\right\rangle
$$

称为曲面 $S$ 的第一基本形式; 它给出曲面上曲线的弧长微元的平方以及切向量长度的平方.

## 定理 3.2.1 (第一基本形式与参数选取无关)

曲面 $S$ 的第一基本形式与参数选取无关.

## 定义 3.3.1 (第二基本形式)

设 $\boldsymbol n=\frac{\boldsymbol r_{u}\wedge\boldsymbol r_{v}}{\left|\boldsymbol r_{u}\wedge\boldsymbol r_{v}\right|}$ 是 $S$ 的单位法向量, $L=\left\langle\boldsymbol r_{uu},\boldsymbol n\right\rangle$, $M=\left\langle\boldsymbol r_{uv},\boldsymbol n\right\rangle$, $N=\left\langle\boldsymbol r_{vv},\boldsymbol n\right\rangle$, 二次微分式

$$
II=-\left\langle\mathrm d\boldsymbol r,\mathrm d\boldsymbol n\right\rangle=L\,\mathrm du\,\mathrm du+2M\,\mathrm du\,\mathrm dv+N\,\mathrm dv\,\mathrm dv=\left\langle\boldsymbol r_{\alpha\beta},\boldsymbol n\right\rangle\,\mathrm du^{\alpha}\,\mathrm du^{\beta}
$$

称为曲面 $S$ 的第二基本形式.

## 定义 3.3.1 (椭圆点、双曲点与抛物点)

设 $\boldsymbol r\left(u_{0}\right)\in S$, 主曲率为 $k_{1}\left(u_{0}\right)\le k_{2}\left(u_{0}\right)$. 若 $k_{1}k_{2}> 0$ (即 $K> 0$), 则称 $\boldsymbol r\left(u_{0}\right)$ 为椭圆点; 若 $k_{1}k_{2}< 0$ (即 $K< 0$), 则称其为双曲点; 若 $k_{1}k_{2}=0$ (即 $K=0$), 则称其为抛物点; 特别若 $k_{1}=k_{2}=0$, 则称其为平点.

## 定义 3.3.1 (渐近方向与渐近线)

曲面上一个切向称为渐近方向, 是指沿此方向的法曲率为 $0$; 双曲点恰有两个不同的渐近方向. 渐近方向的积分曲线称为曲面的渐近线; $C$ 是渐近线当且仅当其切向量处处是渐近方向.

## 性质 3.3.2 (第二基本形式在参数变换下的变化)

设 $\left(u,v\right)$ 与 $\left(\overline u,\overline v\right)$ 是曲面 $S$ 的两个不同参数表示. 当参数变换是同向时, 第二基本形式不变, 即 $\widetilde{II}=II$; 当参数变换是反向时, 第二基本形式改变符号, 即 $\widetilde{II}=-II$.

## 定义 3.4.1 (法曲率)

曲面 $S$ 上曲线 $\boldsymbol c\left(s\right)=\boldsymbol r\left(u\left(s\right)\right)$ 的法曲率为 $k_{n}=b_{\alpha\beta}\dot u^{\alpha}\dot u^{\beta}$; 对一般参数, $k_{n}=\frac{b_{\alpha\beta}\,\mathrm du^{\alpha}\,\mathrm du^{\beta}}{g_{\alpha\beta}\,\mathrm du^{\alpha}\,\mathrm du^{\beta}}=\frac{II}{I}$.

## 定义 3.4.1 (魏因加滕变换)

切平面到自身的线性变换 $W:T_{P}S\to T_{P}S$,

$$
\lambda\boldsymbol r_{u}+\mu\boldsymbol r_{v}\mapsto W\left(\lambda\boldsymbol r_{u}+\mu\boldsymbol r_{v}\right)=-\left(\lambda\boldsymbol n_{u}+\mu\boldsymbol n_{v}\right)
$$

称为曲面的魏因加滕变换.

## 命题 3.4.1 (图形式曲面的基本量)

对图形式曲面 $\boldsymbol r\left(x^{1},x^{2}\right)=\left(x^{1},x^{2},f\left(x^{1},x^{2}\right)\right)$, 有 $g_{\alpha\beta}=\delta_{\alpha\beta}+f_{\alpha}f_{\beta}$, $h_{\alpha\beta}=\frac{f_{\alpha\beta}}{\sqrt{1+f_{1}^{2}+f_{2}^{2}}}$.

## 定理 3.4.1 (魏因加滕变换的自共轭性)

魏因加滕变换 $W$ 是曲面切平面到自身的自共轭变换, 即对任意 $\boldsymbol v,\boldsymbol w\in T_{P}S$, 有 $\left\langle W\left(\boldsymbol v\right),\boldsymbol w\right\rangle=\left\langle\boldsymbol v,W\left(\boldsymbol w\right)\right\rangle$.

## 命题 3.4.2 (法曲率只依赖切方向)

曲面 $S$ 上在一点相切的两条曲线在该点有相同的法曲率.

## 命题 3.4.4 (法向微分是切向量场)

因 $\left\langle\boldsymbol n,\boldsymbol n\right\rangle=1$, 对 $\left\langle\boldsymbol n,\boldsymbol n\right\rangle=1$ 求微分得 $\left\langle\mathrm d\boldsymbol n,\boldsymbol n\right\rangle=0$, 故 $\mathrm d\boldsymbol n$ (从而 $\boldsymbol n_u,\boldsymbol n_v$) 是曲面的切向量.

## 定义 3.5.1 (主曲率与主方向)

魏因加滕变换 $W$ 在点 $P$ 的两个实特征值 $k_{1}\left(u\right)\le k_{2}\left(u\right)$ 称为曲面在 $\boldsymbol r\left(u\right)$ 的主曲率, 相应的实特征方向 $\boldsymbol v_{1},\boldsymbol v_{2}$ 称为主方向; 当 $k_{1}\ne k_{2}$ 时主方向完全确定且相互正交, 当 $k_{1}=k_{2}$ 时任意切向都是主方向.

## 定理 3.5.1 (曲率线网参数)

在曲面非脐点附近, 存在曲率线网参数 $\left(u^{1},u^{2}\right)$ 使坐标曲线是曲率线; 此时第一、第二基本形式均对角: $I=g_{11}\left(\mathrm du^{1}\right)^{2}+g_{22}\left(\mathrm du^{2}\right)^{2}$, $II=k_{1}\left(\mathrm du^{1}\right)^{2}+k_{2}\left(\mathrm du^{2}\right)^{2}$.

## 引理 3.5.2

设 $\boldsymbol e_1,\boldsymbol e_2$ 是曲面在点 $P$ 的单位正交主方向, 则存在曲面在点 $P$ 的参数使得 $\boldsymbol r_u\left(P\right)=\boldsymbol e_1$, $\boldsymbol r_v\left(P\right)=\boldsymbol e_2$.

## 性质 3.5.2 (欧拉公式)

设 $k_{1},k_{2}$ 是曲面在点 $P$ 的主曲率, $\boldsymbol e_{1},\boldsymbol e_{2}$ 是相应的单位正交主方向. 设 $\boldsymbol v\in T_{P}S$ 是单位向量, 与 $\boldsymbol e_{1}$ 的夹角为 $\theta$, 则曲面沿 $\boldsymbol v$ 的法曲率为 $k_{n}\left(\boldsymbol v\right)=k_{1}\cos^{2}\theta+k_{2}\sin^{2}\theta$.

## 推论 3.5.3 (法曲率的范围)

对任意单位切向量 $\boldsymbol v$, $k_{1}\le k_{n}\left(\boldsymbol v\right)\le k_{2}$.

## 命题 3.5.4 (主曲率的特征方程)

$k$ 是主曲率当且仅当它是方程 $\det\left(b_{\alpha\beta}-k g_{\alpha\beta}\right)=0$ 的根; 对应的主方向 $\boldsymbol v_{i}=v_{i}^{\beta}\boldsymbol r_{\beta}$ 的分量满足 $\left(b_{\alpha\beta}-k_{i}g_{\alpha\beta}\right)v_{i}^{\beta}=0$.

## 公式 3.5.4 (平均曲率与高斯曲率)

记曲面在点 $P$ 的两个主曲率为 $k_1,k_2$, 则平均曲率 $H=\frac{k_1+k_2}{2}=\frac{LG-2MF+NE}{2\left(EG-F^{2}\right)}$, 高斯曲率 $K=k_1k_2=\frac{LN-M^{2}}{EG-F^{2}}$; 且 $\boldsymbol n_u\wedge\boldsymbol n_v=K\,\boldsymbol r_u\wedge\boldsymbol r_v$.

## 定义 3.5.5 (脐点、圆点与平点)

使主曲率 $k_{1}\left(u\right)=k_{2}\left(u\right)$ 成立的点 $\boldsymbol r\left(u\right)$ 称为曲面的脐点; 脐点处公共主曲率 $k\ne0$ 时也称圆点, $k=0$ 即 $b_{\alpha\beta}\equiv0$ 时也称平点.

## 公式 3.5.5 (面积元与高斯映射面积)

曲面面积元

$$
\mathrm dA=\left\langle\boldsymbol r_u\wedge\boldsymbol r_v,\boldsymbol n\right\rangle\mathrm du\,\mathrm dv=\sqrt{EG-F^{2}}\,\mathrm du\,\mathrm dv;
$$

在单位法向映射 $g:\boldsymbol r\left(u,v\right)\mapsto\boldsymbol n\left(u,v\right)$ 下, $\mathrm d\sigma=\left\langle\boldsymbol n_u\wedge\boldsymbol n_v,\boldsymbol n\right\rangle\mathrm du\,\mathrm dv=K\,\mathrm dA$, 且若 $D$ 是曲面 $S$ 上含点 $P$ 的区域, 则 $\lim_{D\to P}\frac{\text{面积}\left(g\left(D\right)\right)}{\text{面积}\left(D\right)}=K\left(P\right)$.

## 定义 3.5.6 (平均曲率与总曲率)

$H\left(u\right):=\frac1{2}\left(k_{1}\left(u\right)+k_{2}\left(u\right)\right)$ 称为曲面在该点的平均曲率, $K\left(u\right):=k_{1}\left(u\right)k_{2}\left(u\right)$ 称为曲面在该点的总曲率 (高斯曲率).

## 命题 3.5.7 (特征方程与平均曲率、总曲率)

主曲率 $k_{1},k_{2}$ 是方程 $\det\left(b_{\alpha\beta}-k g_{\alpha\beta}\right)=0$ 的根, 该方程等价于 $k^{2}-2Hk+K=0$.

## 引理 3.5.8 (同时对角化)

存在可逆矩阵 $Q$ 使 $Q^{\top}\left(g_{\alpha\beta}\right)Q=I_{2}$, $Q^{\top}\left(b_{\alpha\beta}\right)Q=\operatorname{diag}\left(k_{1},k_{2}\right)$; 即经过坐标变换可在一点取 $g_{\alpha\beta}=\delta_{\alpha\beta}$, $b_{\alpha\beta}=k_{\alpha}\delta_{\alpha\beta}$, 此时单位主方向 $\boldsymbol e_{1},\boldsymbol e_{2}$ 相互正交.

## 命题 3.5.9 (曲面的二阶近似)

在取 $\boldsymbol r_{u}\left(P\right)=\boldsymbol e_{1}$, $\boldsymbol r_{v}\left(P\right)=\boldsymbol e_{2}$ 为主方向的参数下, 曲面在点 $P$ 附近满足

$$
\boldsymbol r\left(u_{0}+\Delta u,v_{0}+\Delta v\right)-\boldsymbol r\left(u_{0},v_{0}\right)=\Delta u\,\boldsymbol e_{1}+\Delta v\,\boldsymbol e_{2}+\frac1{2}\left(k_{1}\Delta u^{2}+k_{2}\Delta v^{2}\right)\boldsymbol n\left(P\right)+o\left(\Delta u^{2}+\Delta v^{2}\right).
$$

## 命题 3.5.9 (曲面的二阶近似)

在取 $\boldsymbol r_{u}\left(P\right)=\boldsymbol e_{1}$, $\boldsymbol r_{v}\left(P\right)=\boldsymbol e_{2}$ 为主方向的参数下, 曲面在点 $P$ 附近相对切平面的形状由二次型 $\frac1{2}\left(k_{1}\Delta u^{2}+k_{2}\Delta v^{2}\right)\boldsymbol n\left(P\right)$ 决定: 椭圆点近似椭圆抛物面, 双曲点近似双曲抛物面, 抛物点近似抛物柱面.

## 定义 3.6.1 (旋转面)

设 $x^{2}Ox^{3}$ 平面内的正则曲线 $\left(f\left(u\right),g\left(u\right)\right)$ ($f> 0$) 绕 $Ox^{3}$ 轴旋转, 所得曲面 $\boldsymbol r\left(u,v\right)=\left(f\left(u\right)\cos v,f\left(u\right)\sin v,g\left(u\right)\right)$ 称为旋转面; 取 $f\left(t\right)=t$, $g\left(t\right)=\varphi\left(t\right)$ 时写成图形式 $\boldsymbol r\left(t,\theta\right)=\left(t\cos\theta,t\sin\theta,\varphi\left(t\right)\right)$.

## 定义 3.6.1 (曲率线)

曲面 $S$ 上的一条曲线 $C$ 称为曲率线, 是指 $C$ 在每点的切向量都是曲面 $S$ 在该点的一个主方向.

## 命题 3.6.2 (旋转面的基本量与主曲率)

旋转面 $\boldsymbol r\left(u,v\right)=\left(f\left(u\right)\cos v,f\left(u\right)\sin v,g\left(u\right)\right)$ 的第一、第二基本形式系数为 $E=\left(f'\right)^{2}+\left(g'\right)^{2}$, $F=0$, $G=f^{2}$, $L=\frac{f'g''-f''g'}{\sqrt{\left(f'\right)^{2}+\left(g'\right)^{2}}}$, $M=0$, $N=\frac{fg'}{\sqrt{\left(f'\right)^{2}+\left(g'\right)^{2}}}$, 主曲率为 $k_{1}=\frac{L}{E}=\frac{f'g''-f''g'}{\left[\left(f'\right)^{2}+\left(g'\right)^{2}\right]^{\frac3{2}}}$, $k_{2}=\frac{N}{G}=\frac{g'}{f\sqrt{\left(f'\right)^{2}+\left(g'\right)^{2}}}$.

## 命题 3.6.3 (常高斯曲率的旋转曲面)

当选取 $u$ 为母线 $\left(f\left(u\right),g\left(u\right)\right)$ 的弧长参数时, 旋转面的高斯曲率 $K=-\frac{f''}{f}$. 于是: 当 $K> 0$ 时曲面是球面; 当 $K=0$ 时曲面是圆柱面、平面或圆锥面; 当 $K< 0$ 时曲面称为伪球面, 由 $\frac1{1+g'^{2}}=C+\left(x^{2}\right)^{2}$ 确定.

## 定义 3.6.4 (直纹面与直母线)

直纹面是指由单参数直线族构成的曲面, 其参数表达式为 $\boldsymbol r\left(u,v\right)=\boldsymbol a\left(u\right)+v\boldsymbol b\left(u\right)$, $\left|\boldsymbol b\right|=1$; 对固定的 $u$, 直线 $v\mapsto\boldsymbol r\left(u,v\right)$ 称为直纹面的一条直母线.

## 命题 3.6.4 (常平均曲率的旋转曲面)

令旋转面平均曲率 $H\equiv0$, 得 $\frac{\varphi''}{1+\varphi'^{2}}+\frac{\varphi'}{t}=0$, 即 $t\varphi''+\varphi'\left(1+\varphi'^{2}\right)=0$; 取 $c=1$ 时 $\varphi'\left(t\right)=\frac1{\sqrt{t^{2}-1}}$, 积分得 $\varphi\left(t\right)=\ln\left(t+\sqrt{t^{2}-1}\right)=\operatorname{arcosh}t$, 它是悬链线绕轴旋转所得的悬链面.

## 例 3.6.5 (柱面、锥面与切线面)

若 $\boldsymbol b\left(u\right)$ 为常向量, 直母线互相平行, 曲面是柱面; 若 $\boldsymbol a\left(u\right)$ 为常向量, 所有直母线过同一固定点, 曲面是锥面; 若 $\boldsymbol b\left(u\right)=\frac{\boldsymbol a'\left(u\right)}{\left|\boldsymbol a'\left(u\right)\right|}$, 直母线沿准线的切线方向, 曲面是切线面.

## 定义 3.6.6 (可展曲面)

高斯曲率恒为零的直纹面称为可展曲面.

## 性质 3.6.7 (可展曲面的等价条件)

直纹面 $\boldsymbol r\left(u,v\right)=\boldsymbol a\left(u\right)+v\boldsymbol b\left(u\right)$ 是可展曲面, 当且仅当它满足下列等价条件之一: (1) $M\equiv0$; (2) 沿着直母线, 直纹面的法向量不变; (3) $\left(\boldsymbol a',\boldsymbol b,\boldsymbol b'\right)\equiv0$.

## 定理 3.6.8 (可展曲面的分类)

可展曲面恰为柱面、锥面和切线面三类.

## 定义 3.6.9 (全脐曲面)

若曲面上每一个点都是脐点 (即主曲率 $k_{1}=k_{2}$ 处处成立), 则称该曲面为全脐曲面.

## 定理 3.6.10 (全脐曲面必为平面或球面)

曲面是全脐曲面当且仅当它是平面或球面的一部分.

## 习题 3.6.12 (正交参数系)

使 $F=\left\langle\boldsymbol r_{u},\boldsymbol r_{v}\right\rangle=0$ 的参数 $\left(u,v\right)$ 称为曲面的正交参数系; 对曲面 $S$ 上任一点 $P_{0}$, 存在 $P_{0}$ 的邻域及其新参数, 使该新参数是曲面的正交参数系.

## 习题 3.6.26 (主曲率的光滑性)

当 $P$ 不是脐点时, 曲面 $S$ 的主曲率 $k_{1},k_{2}$ 是 $P$ 附近的光滑函数; 当 $P$ 是脐点时, 主曲率是 $P$ 附近的连续函数.

## 习题 3.6.29 (曲率线网参数)

曲面 $S$ 的参数曲线 $u=$ 常数和 $v=$ 常数是曲率线的充要条件是 $F=M=0$.

## 定义 4.2.1 (克里斯托费尔符号)

$\Gamma^{\gamma}{}_{\alpha\beta}=\frac1{2}g^{\gamma\varepsilon}\left(\partial_{\alpha}g_{\beta\varepsilon}+\partial_{\beta}g_{\alpha\varepsilon}-\partial_{\varepsilon}g_{\alpha\beta}\right)$ 称为曲面的第二类克里斯托费尔符号, 完全由第一基本形式的系数以及它们的一阶偏导数确定, 且关于下指标对称: $\Gamma^{\gamma}{}_{\alpha\beta}=\Gamma^{\gamma}{}_{\beta\alpha}$.

## 定理 4.2.1 (自然标架的运动方程)

自然标架 $\left\{\boldsymbol r;\boldsymbol r_{1},\boldsymbol r_{2},\boldsymbol n\right\}$ 随参数的运动方程为 $\partial_{\beta}\boldsymbol r=\boldsymbol r_{\beta}$, $\partial_{\beta}\boldsymbol r_{\alpha}=\Gamma^{\varepsilon}{}_{\alpha\beta}\boldsymbol r_{\varepsilon}+b_{\alpha\beta}\boldsymbol n$, $\partial_{\beta}\boldsymbol n=-b_{\alpha\beta}g^{\alpha\varepsilon}\boldsymbol r_{\varepsilon}$, 其中 $\Gamma^{\varepsilon}{}_{\alpha\beta}$ 是克里斯托费尔符号, $b_{\alpha\beta}$ 是第二基本形式的系数.

## 命题 4.3.1 (高斯方程与科达齐方程)

由自然标架的二阶混合偏导可交换, 运动方程给出高斯方程

$$
\partial_{\gamma}\Gamma^{\delta}{}_{\alpha\beta}-\partial_{\beta}\Gamma^{\delta}{}_{\alpha\gamma}+\Gamma^{\varepsilon}{}_{\alpha\beta}\Gamma^{\delta}{}_{\varepsilon\gamma}-\Gamma^{\varepsilon}{}_{\alpha\gamma}\Gamma^{\delta}{}_{\varepsilon\beta}-b_{\alpha\beta}b^{\delta}{}_{\gamma}+b_{\alpha\gamma}b^{\delta}{}_{\beta}=0
$$

与科达齐方程

$$
\partial_{\gamma}b_{\alpha\beta}-\partial_{\beta}b_{\alpha\gamma}+\Gamma^{\varepsilon}{}_{\alpha\beta}b_{\varepsilon\gamma}-\Gamma^{\varepsilon}{}_{\alpha\gamma}b_{\varepsilon\beta}=0,
$$

二者合称高斯-科达齐方程组, 即曲面的结构方程.

## 定理 4.3.2 (曲面的基本定理)

设 $\varphi=g_{\alpha\beta}\,\mathrm du^{\alpha}\,\mathrm du^{\beta}$ 和 $\psi=b_{\alpha\beta}\,\mathrm du^{\alpha}\,\mathrm du^{\beta}$ 是参数区域 $D$ 上的两个二次微分式, 其中 $\left(g_{\alpha\beta}\right)$ 对称正定, $\left(b_{\alpha\beta}\right)$ 对称. 则存在曲面 $\boldsymbol r:D\to E^{3}$ 以 $\varphi,\psi$ 分别为其第一、第二基本形式, 当且仅当 $\left(g_{\alpha\beta}\right),\left(b_{\alpha\beta}\right)$ 满足高斯-科达齐方程组; 且这样的曲面在 $E^{3}$ 的刚体运动意义下唯一.

## 定理 4.3.3 (高斯绝妙定理)

曲面的总曲率 (高斯曲率) $K=\frac{\det\left(b_{\alpha\beta}\right)}{\det\left(g_{\alpha\beta}\right)}$ 只依赖于第一基本形式 $I$ 的系数 $\left(g_{\alpha\beta}\right)$, 与第二基本形式无关; 换言之, 总曲率是曲面的内蕴量.

## 定义 5.1.1 (法曲率与测地曲率)

曲面上弧长参数曲线 $\boldsymbol r=\boldsymbol r\left(s\right)$ 的测地曲率 $k_{g}$ 定义为 $\ddot{\boldsymbol r}$ 在曲面切平面上的投影长度 (带符号), 法曲率 $k_{n}=b_{\alpha\beta}\dot u^{\alpha}\dot u^{\beta}$ 是 $\ddot{\boldsymbol r}$ 的法向分量系数; 测地曲率只与曲面的第一基本形式有关, 是内蕴几何量.

## 命题 5.1.2 (曲面上曲线的二阶分解)

曲面上的曲线满足

$$
\ddot{\boldsymbol c}\left(s\right)=\left(\ddot u^{\alpha}+\Gamma^{\alpha}{}_{\varepsilon\tau}\dot u^{\varepsilon}\dot u^{\tau}\right)\boldsymbol r_{\alpha}+b_{\varepsilon\tau}\dot u^{\varepsilon}\dot u^{\tau}\,\boldsymbol n,
$$

即 $\ddot{\boldsymbol c}$ 分解为测地曲率向量 (切向部分) 与法曲率向量 (法向部分), 且 $\kappa=\left|\ddot{\boldsymbol c}\right|=\sqrt{k_{g}^{2}+k_{n}^{2}}$.

## 定义 5.1.3 (测地线)

曲面上测地曲率等于 $0$ 的曲线称为曲面的测地线; 曲线是测地线当且仅当它的测地曲率向量等于零.

## 命题 5.1.4 (测地线方程)

曲线 $\left(u^{1}\left(s\right),u^{2}\left(s\right)\right)$ 是测地线, 当且仅当 $\ddot u^{\alpha}+\Gamma^{\alpha}{}_{\varepsilon\tau}\left(u\left(s\right)\right)\dot u^{\varepsilon}\dot u^{\tau}=0$, $\alpha=1,2$; 该方程组称为曲面的测地线方程, 只含第一基本形式的系数及其导数.

## 命题 5.1.5 (正交参数网下的测地曲率)

在正交参数网 $I=g_{11}\left(\mathrm du^{1}\right)^{2}+g_{22}\left(\mathrm du^{2}\right)^{2}$ 下, 若曲线单位切向量与 $\boldsymbol e_{1}$ 的夹角为 $\theta$, 则测地曲率

$$
k_{g}=\theta'\left(s\right)-\frac{\partial_{2}g_{11}}{2g_{11}\sqrt{g_{22}}}\cos\theta+\frac{\partial_{1}g_{22}}{2g_{22}\sqrt{g_{11}}}\sin\theta
$$

(刘维尔公式).

## 推论 5.1.6 (正交参数网下的测地线方程)

在正交参数网下, 曲线是测地线当且仅当 $\theta'\left(s\right)=\frac{\partial_{2}g_{11}}{2g_{11}\sqrt{g_{22}}}\cos\theta-\frac{\partial_{1}g_{22}}{2g_{22}\sqrt{g_{11}}}\sin\theta$.

## 例 5.1.7 (球面上的测地线)

单位球面 $S^{2}$ 上的测地线就是过球心的平面与球面的交线, 即大圆.

## 定理 5.5.1 (高斯-博内公式)

设 $D$ 是曲面 $S$ 上的一块单连通区域, $\partial D$ 是分段光滑闭曲线, $\alpha_{i}$ 是 $\partial D$ 顶点的外角, 则 $\int_{\partial D}k_{g}\,\mathrm ds+\int_{D}K\,\mathrm dA+\sum_{i}\alpha_{i}=2\pi$.

## 定理 6.1.1 (旋转指数定理)

设 $C$ 为平面 $E^{2}$ 上的简单闭曲线, 则 $C$ 的旋转指数为 $\pm1$.

## 引理 6.1.2 (方向角的连续分支)

设 $\overline\theta\left(s\right)$ 是单位切向量与 $x$ 轴的方向角, 则存在连续函数 $\theta\left(s\right)$ 使得 $\theta\left(s\right)\equiv\overline\theta\left(s\right)\left(\bmod 2\pi\right)$, $\forall s\in\left[0,l\right]$, 且这样的连续函数在 $\bmod 2\pi$ 意义下唯一.

## 命题 6.1.2 (曲率与方向角)

设单位切向量 $\boldsymbol t=\left(\cos\theta,\sin\theta\right)$, 法向量 $\boldsymbol n=\left(-\sin\theta,\cos\theta\right)$, 则曲率 $k\left(s\right)=\frac{\mathrm d\theta}{\mathrm ds}$, 即方向角的导数等于 (带符号的) 曲率.

## 定理 6.1.3 (等周不等式)

设平面简单闭曲线 $C$ 的长度为 $L$, 界定的区域面积为 $A$, 则有 $L^{2}-4\pi A\ge0$, 且等号成立当且仅当 $C$ 是一个圆.

## 引理 6.1.4 (维尔丁格不等式)

设 $f$ 是周期为 $2\pi$ 的连续可微函数, 若 $\int_0^{2\pi}f\left(t\right)\mathrm dt=0$, 则 $\int_0^{2\pi}\left[f'\left(t\right)\right]^{2}\mathrm dt\ge\int_0^{2\pi}\left[f\left(t\right)\right]^{2}\mathrm dt$, 且等号成立当且仅当 $f\left(t\right)=a\cos t+b\sin t$, $a,b$ 是常数.

## 定义 6.2.1 (凸曲线)

平面简单闭曲线的曲率 $k> 0$ 时称为凸曲线.

## 定理 6.2.1 (凸曲线的高斯映射)

凸曲线的高斯映射是一一对应; 等价地, 曲线是凸的当且仅当方向角 $\theta\left(s\right)$ 是严格单调增的.

## 定理 7.3.4 (芬切尔定理)

设 $C$ 是 $E^{3}$ 中的闭曲线, $\kappa$ 是它的曲率函数, 则 $C$ 的全曲率满足 $\int_{\boldsymbol r}\kappa\,\mathrm ds\ge2\pi$.

## 定理 7.3.5 (扭结曲线的全曲率)

设 $C$ 为 $E^{3}$ 中的扭结曲线, 则 $C$ 的全曲率 $\int_{\boldsymbol r}\kappa\,\mathrm ds\ge8\pi$.

## 定理 7.3.5 (扭结曲线的全曲率)

设 $C$ 是 $\mathbb E^{3}$ 中的扭结曲线, 则 $C$ 的全曲率满足 $\int_C\kappa\,\mathrm ds\ge4\pi$.

## 定义 10.1.1 (极小曲面)

$\mathbb E^{3}$ 中平均曲率处处恒为零的曲面称为极小曲面.

## 例 10.1.1 (螺旋面)

函数 $f\left(x,y\right)=\arctan\frac yx$ 满足极小曲面方程, 相应的极小曲面 $\boldsymbol r\left(x,y\right)=\left(x,y,\arctan\frac yx\right)$ 称为螺旋面, 它是唯一的直纹极小曲面.

## 公式 10.1.2 (函数图的几何量)

对函数图 $\boldsymbol r\left(x,y\right)=\left(x,y,f\left(x,y\right)\right)$, 记 $p=f_x$, $q=f_y$, $r=f_{xx}$, $s=f_{xy}$, $t=f_{yy}$, $W=\left|\boldsymbol r_x\wedge\boldsymbol r_y\right|=\sqrt{1+p^{2}+q^{2}}$, 则第一基本形式

$$
\mathrm I=\left(1+p^{2}\right)\mathrm dx^{2}+2pq\,\mathrm dx\,\mathrm dy+\left(1+q^{2}\right)\mathrm dy^{2}$, 单位法向 $\boldsymbol e_3=\frac1W\left(-p,-q,1\right),
$$

第二基本形式 $\mathrm{II}=\frac{r\,\mathrm dx^{2}+2s\,\mathrm dx\,\mathrm dy+t\,\mathrm dy^{2}}{W}$, 平均曲率 $H=\frac{\left(1+q^{2}\right)r-2pqs+\left(1+p^{2}\right)t}{2W^{3}}$.

## 定理 10.1.3 (极小曲面方程)

函数图 $\boldsymbol r\left(x,y\right)=\left(x,y,f\left(x,y\right)\right)$ 是极小曲面当且仅当

$$
\left(1+f_y^{2}\right)f_{xx}-2f_xf_yf_{xy}+\left(1+f_x^{2}\right)f_{yy}=0.
$$

## 例 10.1.3 (谢尔克曲面)

极小曲面方程满足 $f\left(x,y\right)=h\left(x\right)+k\left(y\right)$ 的解为 $f\left(x,y\right)=\ln\frac{\cos x}{\cos y}$, 相应的极小曲面称为谢尔克曲面.

## 讲义: 定义 12.1 (包络)

设 $\boldsymbol r:J_{t}\times I_{\alpha}\to E^{2}$ 是 $C^{k}$ 映射 ($k\ge1$), 记 $\boldsymbol r_{\alpha}\left(t\right):=\boldsymbol r\left(t;\alpha\right)$, $\alpha\in I$, 得一族平面曲线 $\left\{\boldsymbol r_{\alpha}\right\}_{\alpha\in I}$. 若存在曲线 $\Gamma$, 使 $\Gamma$ 与每个 $\boldsymbol r_{\alpha}$ 都相切于某点 $\boldsymbol r\left(t\left(\alpha\right);\alpha\right)$, 则称 $\Gamma$ 是曲线族 $\left\{\boldsymbol r_{\alpha}\right\}$ 的一条包络曲线.

## 讲义: 命题 12.2 (包络的参数方程)

若 $\Gamma$ 是包络, 则 $\Gamma\left(\alpha\right)=\boldsymbol r\left(t\left(\alpha\right);\alpha\right)$, $\alpha\in I$, 给出 $\Gamma$ 的参数表示, 其中 $t=t\left(\alpha\right)$ 满足 $\det\left(\frac{\partial\boldsymbol r}{\partial t},\frac{\partial\boldsymbol r}{\partial\alpha}\right)\Big|_{t=t\left(\alpha\right)}=0$, 即 $\frac{\partial\gamma^{1}}{\partial t}\frac{\partial\gamma^{2}}{\partial\alpha}-\frac{\partial\gamma^{1}}{\partial\alpha}\frac{\partial\gamma^{2}}{\partial t}\Big|_{t=t\left(\alpha\right)}=0$.

## 讲义: 命题 12.3 (脊线)

上述行列式方程的解或者是包络曲线, 或者是曲线族 $\left\{\boldsymbol r_{\alpha}\right\}$ 的起点组成的曲线 (脊线).

## 讲义: 定义 16.1 (凸闭曲线)

正则简单闭曲线 $\boldsymbol r$ 称为凸闭曲线, 若对任意 $p\in\boldsymbol r$, $\boldsymbol r$ 都完全位于 $p$ 处的切线 $l_{p}$ 的同一侧.

## 讲义: 引理 17.2 (闭半球中的切线像)

对正则闭曲线 $\boldsymbol r$, 若其切线像

$$
\boldsymbol r^{*}\subset H_{+}\left(\boldsymbol n_{0}\right):=\left\{\boldsymbol x\in S^{2}\left(1\right):\left\langle\boldsymbol x,\boldsymbol n_{0}\right\rangle\ge0\right\},
$$

则 $\boldsymbol r^{*}$ 包含于赤道 $\partial H_{+}\left(\boldsymbol n_{0}\right)$.

## 讲义: 引理 17.3 (大圆与切线像相交)

对任意 $\boldsymbol n_{0}\in S^{2}\left(1\right)$, 大圆 $\partial H_{+}\left(\boldsymbol n_{0}\right)$ 与切线像 $\boldsymbol r^{*}$ 至少相交两个点.

## 讲义: 定理 18.1 (芬切尔定理的分段光滑推广)

设 $\boldsymbol r$ 是分段有限段光滑的空间闭曲线, $P_{1},\dotsc,P_{k}$ 是 $\boldsymbol r$ 的角点, 沿参数增加方向依次排列. 在 $P_{i}=\boldsymbol r\left(s_{i}\right)$ 处, 令转向角 $\theta_{i}:=\angle\left(\dot{\boldsymbol r}\left(s_{i}^{-}\right),\dot{\boldsymbol r}\left(s_{i}^{+}\right)\right)$ (即角点两侧切向量之间的夹角, 其中 $P_{k+1}=P_{1}$). 则 $\sum_{j=1}^{k}\int_{P_{j}}^{P_{j+1}}\kappa\,\mathrm ds+\sum_{i=1}^{k}\theta_{i}\ge2\pi$.

## 讲义: 引理 26.1 (同时对角化)

设 $A,B$ 是 $n$ 阶实对称矩阵, 且 $A$ 正定. 则存在可逆矩阵 $Q$ 使 $Q^{\top}AQ$ 与 $Q^{\top}BQ$ 同时为对角矩阵.

## 讲义: 引理 30.1 (积分因子)

设 $\omega=P\,\mathrm du^{1}+Q\,\mathrm du^{2}$ 是参数区域 $D$ 上的一阶微分形式, 其中 $P,Q$ 光滑且不同时为零. 则局部存在处处非零的光滑函数 $\sigma$, 使得 $\sigma\omega$ 是恰当形式.

## 讲义: 命题 31.4 (非脐点附近的光滑主方向场)

在曲面 $S$ 的非脐点附近, 总存在两个光滑的单位向量场 $\left\{\boldsymbol v_{i}\right\}_{i=1,2}$, 使得 $\boldsymbol v_{i}\left(u\right)$ 是 $\boldsymbol r\left(u\right)$ 处的第 $i$ 个主方向.

## 讲义: 定义 44.1 (曲面的包络)

设 $\left\{\Sigma_{\lambda}\right\}_{\lambda\in I}$ 是一族正则曲面, $\Sigma_{\lambda}=\left\{x\in\mathbb R^{3}:F\left(x;\lambda\right)=0\right\}$, $F\in C^{1}$, $\nabla F\ne0$ 对一切 $x\in\Sigma_{\lambda}$. 若曲面 $S$ 满足: 对任意 $\lambda\in I$, $S$ 与 $\Sigma_{\lambda}$ 相切, 或对任意 $x\in S$, 存在 $\lambda\left(x\right)\in I$ 使 $\Sigma_{\lambda\left(x\right)}$ 与 $S$ 在 $x$ 点相切, 则称 $S$ 是曲面族 $\left\{\Sigma_{\lambda}\right\}_{\lambda\in I}$ 的包络.

## 讲义: 定义 45.1 (可展曲面——一族平面的包络)

一族平面的包络称为可展曲面.

## 讲义: 定理 54.1 (旋转面的经线是测地线)

设 $\Sigma$ 是平面 $Ox^{2}x^{3}$ 内正则曲线 $\gamma$ 绕 $Ox^{3}$ 轴旋转所得的旋转面. 则 $\Sigma$ 的所有经线 (即 $\gamma$ 旋转所得的像) 都是测地线; 且 $\Sigma$ 的经纬线构成曲率线网.

## 讲义: 命题 56.1 (正交相交曲面的渐近性与测地性传递)

设 $\Sigma_{1},\Sigma_{2}$ 是两个曲面, $C=\Sigma_{1}\cap\Sigma_{2}$ 是光滑曲线, 且 $\Sigma_{1},\Sigma_{2}$ 沿 $C$ 处处正交. 若 $C$ 是 $\Sigma_{1}$ 的渐近线 (测地线), 则 $C$ 也是 $\Sigma_{2}$ 的渐近线 (测地线).

## 讲义: 例 57.1 (锥面上过每点恰有一条闭测地线)

对半顶角为 $45^{\circ}$ 的圆锥面 $\Sigma=\left\{\left(x^{3}\right)^{2}=\left(x^{1}\right)^{2}+\left(x^{2}\right)^{2}\right\}\setminus\left\{\boldsymbol0\right\}$, 过任意 $p\in\Sigma$ 有且仅有一条闭测地线.

## 法里-米尔诺定理 (题面给定)

设 $\gamma:\left[0,L\right]\to\mathbb E^{3}$ 是光滑弧长参数简单闭曲线, 若 $\gamma$ 是非平凡纽结, 则其全曲率积分满足 $\int_\gamma\kappa\left(s\right)\mathrm ds4\pi$.
