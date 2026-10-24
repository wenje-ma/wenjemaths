# 微分几何: 期中考试

**定义 1.1 (曲面与单位法向)**

若映射 $\boldsymbol r:D\to\mathbb E^{3}$, $\left(u,v\right)\mapsto\boldsymbol r\left(u,v\right)$, 的分量函数可微且 $\boldsymbol r_u,\boldsymbol r_v$ 线性无关 (即 $\boldsymbol r_u\wedge\boldsymbol r_v\neq\boldsymbol0$), 则称 $\boldsymbol r$ 是 $\mathbb E^{3}$ 的一个曲面(片); $\boldsymbol r_u\wedge\boldsymbol r_v$ 是曲面在该点的法向量, $\boldsymbol n=\frac{\boldsymbol r_u\wedge\boldsymbol r_v}{\left|\boldsymbol r_u\wedge\boldsymbol r_v\right|}$ 是该点的单位法向量.

**定义 1.1 (极小曲面)**

$\mathbb E^{3}$ 中平均曲率处处恒为零的曲面称为极小曲面.

**例 1.1 (螺旋面)**

函数 $f\left(x,y\right)=\arctan\frac yx$ 满足极小曲面方程, 相应的极小曲面 $\boldsymbol r\left(x,y\right)=\left(x,y,\arctan\frac yx\right)$ 称为螺旋面, 它是惟一的直纹极小曲面.

**定义 1.2 (切平面)**

$\boldsymbol r_u,\boldsymbol r_v$ 张成的平面 $T_{\boldsymbol r}S=\mathrm{span}\left\{\boldsymbol r_u,\boldsymbol r_v\right\}$ 称为曲面 $S$ 在点 $\boldsymbol r$ 处的切平面(切空间).

**公式 1.2 (函数图的几何量)**

对函数图 $\boldsymbol r\left(x,y\right)=\left(x,y,f\left(x,y\right)\right)$, 记 $p=f_x$, $q=f_y$, $r=f_{xx}$, $s=f_{xy}$, $t=f_{yy}$, $W=\left|\boldsymbol r_x\wedge\boldsymbol r_y\right|=\sqrt{1+p^{2}+q^{2}}$, 则第一基本形式

$$
\mathrm I=\left(1+p^{2}\right)\mathrm dx^{2}+2pq\,\mathrm dx\,\mathrm dy+\left(1+q^{2}\right)\mathrm dy^{2},
$$

单位法向 $\boldsymbol e_3=\frac1W\left(-p,-q,1\right)$, 第二基本形式 $\mathrm{II}=\frac{r\,\mathrm dx^{2}+2s\,\mathrm dx\,\mathrm dy+t\,\mathrm dy^{2}}{W}$, 平均曲率 $H=\frac{\left(1+q^{2}\right)r-2pqs+\left(1+p^{2}\right)t}{2W^{3}}$.

**推导 1.3 (参数变换下法向)**

设 $\left(u,v\right)\to\left(\tilde u,\tilde v\right)$ 是参数变换, 雅可比行列式 $J:=\frac{\partial\left(u,v\right)}{\partial\left(\tilde u,\tilde v\right)}$, 则 $\boldsymbol r_{\tilde u}\wedge\boldsymbol r_{\tilde v}=\det J\,\boldsymbol r_u\wedge\boldsymbol r_v$; 因而同向参数变换 ($\det J>0$) 不改变单位法向 $\boldsymbol n$, 反向参数变换 ($\det J<0$) 使 $\boldsymbol n$ 变号.

**定理 1.3 (极小曲面方程)**

函数图 $\boldsymbol r\left(x,y\right)=\left(x,y,f\left(x,y\right)\right)$ 是极小曲面当且仅当

$$
\left(1+f_y^{2}\right)f_{xx}-2f_xf_yf_{xy}+\left(1+f_x^{2}\right)f_{yy}=0.
$$

**例 1.3 (谢尔克曲面)**

极小曲面方程满足 $f\left(x,y\right)=h\left(x\right)+k\left(y\right)$ 的解为 $f\left(x,y\right)=\ln\frac{\cos x}{\cos y}$, 相应的极小曲面称为谢尔克曲面.

**例 1.5 (等值面)**

等值面 $S_c=\left\{\left(x,y,z\right)\mid F\left(x,y,z\right)=c\right\}$: 当 $\nabla F\left(P\right)\neq\boldsymbol0$ ($\forall P\in S_c$) 时 $S_c$ 是曲面, $\nabla F$ 是 $S_c$ 的法向, 且 $S_c$ 在 $P_0=\left(x_0,y_0,z_0\right)$ 的切平面方程为

$$
F_x\left(P_0\right)\left(x-x_0\right)+F_y\left(P_0\right)\left(y-y_0\right)+F_z\left(P_0\right)\left(z-z_0\right)=0.
$$

**定义 2.1 (弧长与弧长参数)**

曲线 $\boldsymbol r\left(t\right)$, $t\in\left[c,d\right]$, 的弧长为 $\int_c^d\left|\boldsymbol r'\left(t\right)\right|\mathrm dt$; 弧长函数 $s\left(t\right)=\int_c^t\left|\boldsymbol r'\left(u\right)\right|\mathrm du$ 严格单调, 可把参数换为弧长参数 $s$, 此时 $\left|\frac{\mathrm d\boldsymbol r}{\mathrm ds}\right|\equiv1$, 单位切向量 $\boldsymbol t=\dot{\boldsymbol r}$; 反之, 若参数 $t$ 满足 $\left|\frac{\mathrm d\boldsymbol r}{\mathrm dt}\right|\equiv1$, 则 $t$ 是弧长参数.

**定理 2.1 (第一基本形式与参数选取无关)**

曲面的第一基本形式与参数选取无关.

**定义 2.2 (平面曲线的曲率与弗勒内标架)**

对平面曲线 $\boldsymbol r\left(s\right)$, 取单位切向量 $\boldsymbol t$ 与单位法向量 $\boldsymbol n$ 使 $\left\{\boldsymbol t,\boldsymbol n\right\}$ 为右手系, 则 $\left[\boldsymbol r\left(s\right);\boldsymbol t\left(s\right),\boldsymbol n\left(s\right)\right]$ 是沿曲线的弗勒内标架, 且 $\dot{\boldsymbol t}=k\boldsymbol n$, $\dot{\boldsymbol n}=-k\boldsymbol t$; 函数 $k\left(s\right)$ 称为曲线的有向曲率.

**例 2.2 (曲率为常数的曲线)**

(1) $k\left(s\right)\equiv0$ 时 $\boldsymbol r$ 是直线; (2) $k\left(s\right)$ 为非零常数时 $\boldsymbol r$ 是半径 $\frac1{\left|k\right|}$ 的圆 (或它的一部分).

**定义 2.3 (第一基本形式)**

$$
\mathrm I=\left(\mathrm d\boldsymbol r,\mathrm d\boldsymbol r\right)=E\,\mathrm du^{2}+2F\,\mathrm du\,\mathrm dv+G\,\mathrm dv^{2},
$$

其中 $E=\left\langle\boldsymbol r_u,\boldsymbol r_u\right\rangle$, $F=\left\langle\boldsymbol r_u,\boldsymbol r_v\right\rangle$, $G=\left\langle\boldsymbol r_v,\boldsymbol r_v\right\rangle$; 它给出切向量长度的平方.

**定义 3.1 (空间曲线的曲率与弗勒内标架)**

对弧长参数空间曲线 $\boldsymbol r\left(s\right)$, 记曲率 $k\left(s\right)=\left|\dot{\boldsymbol t}\left(s\right)\right|$; 当 $k>0$ 时主法向量 $\boldsymbol n=\dot{\boldsymbol t}/k$, 副法向量 $\boldsymbol b=\boldsymbol t\wedge\boldsymbol n$, $\left[\boldsymbol r;\boldsymbol t,\boldsymbol n,\boldsymbol b\right]$ 是弗勒内标架; 挠率 $\tau=\left\langle\dot{\boldsymbol n},\boldsymbol b\right\rangle$.

**定理 3.1 (平面曲线的充要条件)**

设空间曲线 $\boldsymbol r$ 的曲率 $k>0$, 则 $\boldsymbol r$ 落在某个平面上的充要条件是 $\tau\equiv0$.

**定理 3.2 (弗勒内公式)**

$\dot{\boldsymbol t}=k\boldsymbol n$, $\dot{\boldsymbol n}=-k\boldsymbol t+\tau\boldsymbol b$, $\dot{\boldsymbol b}=-\tau\boldsymbol n$.

**定理 3.3 (弧长参数曲线的三阶渐近展开)**

设 $\boldsymbol r$ 以弧长为参数, 在 $s_0=0$ 处有

$$
\boldsymbol r\left(s\right)=\boldsymbol r\left(0\right)+s\,\dot{\boldsymbol r}\left(0\right)+\frac{s^{2}}2\ddot{\boldsymbol r}\left(0\right)+O\left(s^{3}\right),
$$

其中 $\ddot{\boldsymbol r}\left(0\right)=k\left(0\right)\boldsymbol n\left(0\right)$.

**例 3.3 (球面的第二基本形式)**

半径为 $a$ 的球面在球面坐标参数下的第二基本形式为 $\mathrm{II}=a\left(\mathrm d\theta^{2}+\cos^{2}\varphi\,\mathrm d\varphi^{2}\right)$.

**定义 3.4 (第二基本形式)**

$$
\mathrm{II}=\left\langle\boldsymbol r_{uu},\boldsymbol n\right\rangle\mathrm du^{2}+2\left\langle\boldsymbol r_{uv},\boldsymbol n\right\rangle\mathrm du\,\mathrm dv+\left\langle\boldsymbol r_{vv},\boldsymbol n\right\rangle\mathrm dv^{2}=L\,\mathrm du^{2}+2M\,\mathrm du\,\mathrm dv+N\,\mathrm dv^{2},
$$

其中 $L=\left\langle\boldsymbol r_{uu},\boldsymbol n\right\rangle$, $M=\left\langle\boldsymbol r_{uv},\boldsymbol n\right\rangle$, $N=\left\langle\boldsymbol r_{vv},\boldsymbol n\right\rangle$.

**性质 3.4 (第二基本形式在参数变换下变号)**

设 $\boldsymbol r=\boldsymbol r\left(u,v\right)$ 与 $\boldsymbol r=\boldsymbol r\left(\tilde u,\tilde v\right)$ 是曲面 $S$ 的两个不同参数表示. 当变换 $\left(u,v\right)\to\left(\tilde u,\tilde v\right)$ 是同向参数变换时, $\mathrm{II}\left(\tilde u,\tilde v\right)=\mathrm{II}\left(u,v\right)$; 当它是反向参数变换时, $\mathrm{II}\left(\tilde u,\tilde v\right)=-\mathrm{II}\left(u,v\right)$.

**定理 3.4 (芬切尔不等式)**

设 $C$ 是 $\mathbb E^{3}$ 中的闭曲线, $\kappa$ 是它的曲率函数, 则 $C$ 的全曲率满足 $\int_C\kappa\,\mathrm ds\ge2\pi$.

**定理 3.5 (扭结曲线的全曲率)**

设 $C$ 是 $\mathbb E^{3}$ 中的扭结曲线, 则 $C$ 的全曲率满足 $\int_C\kappa\,\mathrm ds\ge4\pi$.

**性质 4.1 (弧长, 曲率, 挠率的刚体运动不变性)**

$\mathbb E^{3}$ 中曲线的弧长, 曲率和挠率在刚体运动下不变.

**例 4.1 (球面的法曲率)**

半径为 $a$ 的球面上任意一点沿任何方向的法曲率均为 $\frac1a$.

**定义 4.2 (法曲率)**

曲面沿非零切向量 $\boldsymbol w=\lambda\boldsymbol r_u+\mu\boldsymbol r_v$ 的法曲率

$$
k_n\left(\boldsymbol w\right)=\frac{L\lambda^{2}+2M\lambda\mu+N\mu^{2}}{E\lambda^{2}+2F\lambda\mu+G\mu^{2}}=\frac{\mathrm{II}\left(\boldsymbol w,\boldsymbol w\right)}{\mathrm I\left(\boldsymbol w,\boldsymbol w\right)}.
$$

**定理 4.2 (空间曲线基本定理)**

设 $\boldsymbol r_1\left(s\right)$ 和 $\boldsymbol r_2\left(s\right)$ 是 $\mathbb E^{3}$ 的两条弧长参数曲线, 定义在同一参数区间上, 且 $k_1\left(s\right)=k_2\left(s\right)>0$, $\tau_1\left(s\right)=\tau_2\left(s\right)$ 对一切 $s$ 成立, 则存在 $\mathbb E^{3}$ 的一个刚体运动把 $\boldsymbol r_2$ 变为 $\boldsymbol r_1$.

**定义 4.3 (魏因加滕变换)**

线性变换 $\boldsymbol W:=-\mathrm d\boldsymbol n:\ T_{\boldsymbol r}S\to T_{\boldsymbol r}S$, $\boldsymbol W\left(\lambda\boldsymbol r_u+\mu\boldsymbol r_v\right)=-\left(\lambda\boldsymbol n_u+\mu\boldsymbol n_v\right)$ 称为曲面的魏因加滕变换.

**定理 4.3 (给定曲率挠率存在弧长参数曲线)**

设 $k=k\left(s\right)$ 和 $\tau=\tau\left(s\right)$ 是定义在区间 $\left(a,b\right)$ 上的两个连续可微函数, 且 $k\left(s\right)>0$, 则存在以 $s$ 为弧长参数, 以 $k$ 为曲率, 以 $\tau$ 为挠率的空间曲线.

**命题 4.4 (法向微分是切向量场)**

因 $\left\langle\boldsymbol n,\boldsymbol n\right\rangle=1$, 对 $\left\langle\boldsymbol n,\boldsymbol n\right\rangle=1$ 求微分得 $\left\langle\mathrm d\boldsymbol n,\boldsymbol n\right\rangle=0$, 故 $\mathrm d\boldsymbol n$ (从而 $\boldsymbol n_u,\boldsymbol n_v$) 是曲面的切向量.

**定理 4.4 (平面曲线基本定理)**

设 $k\left(s\right)$ 是连续可微函数, 则 (1) 存在平面 $\mathbb E^{2}$ 的曲线 $\boldsymbol r\left(s\right)$, 它以 $s$ 为弧长参数, $k\left(s\right)$ 为曲率; (2) 上述曲线在相差平面的一个刚体运动的意义下是惟一的.

**例 4.5 (曲率挠率均为常数的曲线分类)**

设 $\boldsymbol r$ 是 $\mathbb E^{3}$ 的曲线, 其挠率 $\tau$ 和曲率 $k$ 是常数. 则: (1) $k=0$ 时 $\boldsymbol r$ 是直线; (2) $k>0,\ \tau=0$ 时 $\boldsymbol r$ 是半径 $\frac1k$ 的圆; (3) $k>0,\ \tau\ne0$ 时 $\boldsymbol r$ 是圆柱螺线.

**定义 5.1 (主曲率与主方向)**

魏因加滕变换在点 $P$ 的两个特征值称为曲面在点 $P$ 的主曲率, 对应特征方向称为主方向; 当两个主曲率不等时两主方向相互正交, 当两主曲率相等时任一切向都是主方向.

**引理 5.2**

设 $\boldsymbol e_1,\boldsymbol e_2$ 是曲面在点 $P$ 的单位正交主方向, 则存在曲面在点 $P$ 的参数使得 $\boldsymbol r_u\left(P\right)=\boldsymbol e_1$, $\boldsymbol r_v\left(P\right)=\boldsymbol e_2$.

**公式 5.4 (平均曲率与高斯曲率)**

记曲面在点 $P$ 的两个主曲率为 $k_1,k_2$, 则平均曲率 $H=\frac{k_1+k_2}{2}=\frac{LG-2MF+NE}{2\left(EG-F^{2}\right)}$, 高斯曲率 $K=k_1k_2=\frac{LN-M^{2}}{EG-F^{2}}$; 且 $\boldsymbol n_u\wedge\boldsymbol n_v=K\,\boldsymbol r_u\wedge\boldsymbol r_v$.

**公式 5.5 (面积元与高斯映射面积)**

曲面面积元

$$
\mathrm dA=\left\langle\boldsymbol r_u\wedge\boldsymbol r_v,\boldsymbol n\right\rangle\mathrm du\,\mathrm dv=\sqrt{EG-F^{2}}\,\mathrm du\,\mathrm dv;
$$

在单位法向映射 $g:\boldsymbol r\left(u,v\right)\mapsto\boldsymbol n\left(u,v\right)$ 下, $\mathrm d\sigma=\left\langle\boldsymbol n_u\wedge\boldsymbol n_v,\boldsymbol n\right\rangle\mathrm du\,\mathrm dv=K\,\mathrm dA$, 且若 $D$ 是曲面 $S$ 上含点 $P$ 的区域, 则 $\lim_{D\to P}\frac{\text{面积}\left(g\left(D\right)\right)}{\text{面积}\left(D\right)}=K\left(P\right)$.

**公式 6.1 (旋转曲面的基本量)**

旋转曲面

$$
\boldsymbol r\left(u,v\right)=\left(f\left(u\right)\cos v,\ f\left(u\right)\sin v,\ g\left(u\right)\right)
$$

($f>0$) 的第一, 第二基本形式系数为 $E=\left(f'\right)^{2}+\left(g'\right)^{2}$, $F=0$, $G=f^{2}$, $L=\frac{f'g''-f''g'}{\sqrt{\left(f'\right)^{2}+\left(g'\right)^{2}}}$, $M=0$, $N=\frac{fg'}{\sqrt{\left(f'\right)^{2}+\left(g'\right)^{2}}}$.

**法里-米尔诺定理 (题面给定)**

设 $\gamma:\left[0,L\right]\to\mathbb E^{3}$ 是光滑弧长参数简单闭曲线, 若 $\gamma$ 是非平凡纽结, 则其全曲率积分满足 $\int_\gamma\kappa\left(s\right)\mathrm ds>4\pi$.

**习题 2-5 (一般参数下的曲率与挠率公式)**

$\mathbb E^{3}$ 的正则曲线 $\boldsymbol r\left(t\right)$ 的曲率和挠率分别为 $k\left(t\right)=\frac{\left|\boldsymbol r'\wedge\boldsymbol r''\right|}{\left|\boldsymbol r'\right|^{3}}$, $\tau\left(t\right)=\frac{\left(\boldsymbol r',\boldsymbol r'',\boldsymbol r'''\right)}{\left|\boldsymbol r'\wedge\boldsymbol r''\right|^{2}}$, 其中 $\left(\cdot,\cdot,\cdot\right)$ 为混合积.

**习题 2-8 (距离最近点的向量垂直)**

设平面正则曲线 $C:\boldsymbol r=\boldsymbol r\left(t\right)$ 不过 $P_0$ 点, $\boldsymbol r\left(t_0\right)$ 是 $C$ 与 $P_0$ 距离最近的点, 则向量 $\boldsymbol r\left(t_0\right)-P_0$ 与 $\boldsymbol r'\left(t_0\right)$ 垂直.

**习题 2-9 (切线过定点为直线, 主法线过定点为圆)**

(1) 若 $\mathbb E^{3}$ 的曲线 $C$ 的所有切线过一个定点, 则 $C$ 是直线; (2) 所有主法线过定点的曲线是圆.

**习题 2-10 (反向合同变换下弧长, 曲率不变, 挠率变号)**

设 $T\left(\boldsymbol X\right)=\boldsymbol X\boldsymbol T+P$ 是 $\mathbb E^{3}$ 的一个合同变换, $\det T=-1$, $\boldsymbol r\left(t\right)$ 是 $\mathbb E^{3}$ 的正则曲线, 则曲线 $\tilde{\boldsymbol r}=T\circ\boldsymbol r$ 与曲线 $\boldsymbol r$ 的弧长参数相同, 曲率相同, 挠率变号.

**习题 2-12 (切线像的曲率与挠率)**

设 $\boldsymbol r\left(s\right)$ 的曲率与挠率为 $\kappa,\tau$, 则其切线像 $\boldsymbol t\left(s\right)$ 的曲率, 挠率分别为 $\kappa^{*}=\sqrt{1+\left(\frac{\tau}{\kappa}\right)^{2}}$, $\tau^{*}=\frac1\kappa\cdot\frac{\left(\frac{\tau}{\kappa}\right)'}{1+\left(\frac{\tau}{\kappa}\right)^{2}}$.

**习题 2-15 (球面曲线的刻画)**

满足条件 $\left(\frac1\kappa\right)^{2}+\left[\frac1\tau\frac{\mathrm d}{\mathrm ds}\left(\frac1\kappa\right)\right]^{2}=$ 常数的曲线, 或者是球面曲线, 或者 $\kappa$ 是常数.
