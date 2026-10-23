# 泛函分析 — 第 1 次月考

## 定义 1.1.1 (度量空间)

设 $X$ 是一个非空集合, 若对于 $X$ 中任意两个元素 $x,y$, 都有一个实数 $d\left(x,y\right)$ 与它们对应, 而且满足下面条件:

(i) (非负性与正定性) 对任意 $x,y\in X$, $d\left(x,y\right)\ge0$, 并且 $d\left(x,y\right)=0$ 的充要条件是 $x=y$;

(ii) (对称性) 对任意 $x,y\in X$, $d\left(x,y\right)=d\left(y,x\right)$;

(iii) (三角不等式) 对任意 $x,y,z\in X$, $d\left(x,y\right)\le d\left(x,z\right)+d\left(z,y\right)$, 则称 $\left(X,d\right)$ 是一个度量空间, $d$ 为 $X$ 上的度量.

## 定义 1.1.2 (极限)

设 $\left(X,d\right)$ 是度量空间, $\left\{x_n\right\}_{n=1}^\infty$ 是 $X$ 中点列, $x_0\in X$, 若 $\lim_{n\to\infty}d\left(x_n,x_0\right)=0$, 则称点列 $\left\{x_n\right\}$ 按照度量 $d$ 收敛于 $x_0$, 记为 $\lim_{n\to\infty}x_n=x_0$.

## 例 1.1.2 ($n$ 维欧几里得空间)

在 $n$ 个有序实数组 $x=\left(x_1,x_2,\cdots,x_n\right)$ 全体组成的集合 $X$ 中, 定义 $d\left(x,y\right)=\sqrt{\sum_{i=1}^{n}\left(x_i-y_i\right)^2}$, 则 $\left(X,d\right)$ 是度量空间, 称为 $n$ 维欧几里得空间, 通常记为 $\mathbb R^n$.

## 例 1.1.10 (一致收敛与度量收敛)

由例 1.1.6 的讨论可知, $C\left[a,b\right]$ 中点列按度量 $d\left(f,g\right)=\max_{x\in\left[a,b\right]}\left|f\left(x\right)-g\left(x\right)\right|$ 收敛等价于区间 $\left[a,b\right]$ 上的函数列一致收敛.

## 例 1.1.11 (等价度量)

设 $\left(X,d\right)$ 是度量空间, 在 $X$ 上定义新的度量 $d'\left(x,y\right)=\frac{d\left(x,y\right)}{1+d\left(x,y\right)}$, $d''\left(x,y\right)=\ln\left(1+d\left(x,y\right)\right)$, $\forall x,y\in X$, 它们是不同的度量; 且对于空间 $X$ 中的点列 $\left\{x_n\right\}$,

$$
\lim_{n\to\infty}x_n\overset d=x_0\Leftrightarrow\lim_{n\to\infty}x_n\overset{d'}=x_0\Leftrightarrow\lim_{n\to\infty}x_n\overset{d''}=x_0.
$$

## 例 1.1.12 (可测函数等价类空间)

对于有限区间 $\left[a,b\right]$, 记

$$
\mathfrak G=\left\{\left[a,b\right]\text{ 上几乎处处有限的勒贝格可测函数}\right\},
$$

$f,g\in\mathfrak G$ 等价是指 $f\overset m= g$, 仍以 $f$ 表示 $f$ 在 $\mathcal S=\mathfrak G/\sim$ 中对应的等价类; 对于 $f,g\in\mathcal S$, 定义 $d\left(f,g\right)=\int_{\left[a,b\right]}\frac{\left|f\left(t\right)-g\left(t\right)\right|}{1+\left|f\left(t\right)-g\left(t\right)\right|}\,\mathrm dm\left(t\right)$, 这是一个度量, 且 $d\left(f,g\right)=0$ 当且仅当 $f\overset m= g$.

## 定义 1.2.1 (哈梅尔基与维数)

线性空间 $X$ 上的一个极大线性无关组称为 $X$ 的一组哈梅尔基; 若哈梅尔基中只有有限个元素, 则称 $X$ 是有限维线性空间.

## 定义 1.2.2 (半范数与范数)

记 $\mathbb K$ 是实数域 $\mathbb R$ 或复数域 $\mathbb C$. 对于 $\mathbb K$ 上的线性空间 $X$, 若每个向量 $x$ 都对应一个实数 $\left\|x\right\|$, 满足: (i) $\left\|x\right\|\ge0$;

(ii) $\left\|\alpha x\right\|=\left|\alpha\right|\left\|x\right\|$;

(iii) $\left\|x+y\right\|\le\left\|x\right\|+\left\|y\right\|$, 则称 $\left\|\cdot\right\|$ 为半范数.

若还满足 $\left\|x\right\|=0$ 当且仅当 $x=0$, 则称 $\left\|\cdot\right\|$ 为范数, $\left(X,\left\|\cdot\right\|\right)$ 称为赋范线性空间. 范数诱导度量 $d\left(x,y\right)=\left\|x-y\right\|$.

## 定理 1.2.2 (勾股定理, 毕达哥拉斯定理)

对内积空间 $H$ 中两个元素 $x,y$, 若 $x\perp y$, 则 $\left\|x+y\right\|^2=\left\|x\right\|^2+\left\|y\right\|^2$.

## 定义 1.2.3 (内积空间)

记 $\mathbb K$ 是实数域 $\mathbb R$ 或复数域 $\mathbb C$. 对于 $\mathbb K$ 上的线性空间 $H$, 如果任何两个向量 $x,y$ 都对应一个数 $\left\langle x,y\right\rangle\in\mathbb K$, 满足: (i) 共轭对称性 $\left\langle x,y\right\rangle=\overline{\left\langle y,x\right\rangle}$;

(ii) 对第一变元的线性性 $\left\langle\alpha x+\beta y,z\right\rangle=\alpha\left\langle x,z\right\rangle+\beta\left\langle y,z\right\rangle$;

(iii) 正定性 $\left\langle x,x\right\rangle\ge0$ 且 $\left\langle x,x\right\rangle=0$ 当且仅当 $x=0$,

则称 $\left\langle\cdot,\cdot\right\rangle$ 是 $H$ 中的内积, 称 $H$ 是内积空间.

## 引理 1.2.3 (柯西-施瓦茨不等式)

设 $x,y\in H$ ($H$ 为内积空间), 则 $\left|\left\langle x,y\right\rangle\right|^2\le\left\langle x,x\right\rangle\left\langle y,y\right\rangle$, 特别地当 $\left\|x\right\|=\left\|y\right\|=1$ 时 $\left|\left\langle x,y\right\rangle\right|\le1$.

## 引理 1.2.4 (内积的连续性)

设 $H$ 是内积空间, 则内积关于两个变元是连续的: 当 $x_n\to x$, $y_n\to y$ 时, 有 $\left\langle x_n,y_n\right\rangle\to\left\langle x,y\right\rangle$.

## 例 1.2.8 ($L^p\left(E\right)$ 是巴拿赫空间)

设 $E$ 是 Euclid 空间 $\mathbb R^k$ 的 Lebesgue 可测集, $1\le p< \infty$, 则 $L^p\left(E\right)$ 按范数 $\left\|f\right\|_p=\left(\int_E\left|f\right|^p\,\mathrm dm\right)^{1/p}$ 是赋范线性空间, 且该范数诱导的度量是完备的, 即 $L^p\left(E\right)$ 是巴拿赫空间.

## 例 1.2.12 ($C\left[a,b\right]$ 是巴拿赫空间)

有限闭区间 $\left[a,b\right]$ 上的连续函数空间 $C\left[a,b\right]$ 按范数 $\left\|f\right\|=\max_{x\in\left[a,b\right]}\left|f\left(x\right)\right|$ 是巴拿赫空间.

## 习题 1.2-13 (内积空间的可数直和)

设 $R_n$ 都是内积空间,

$$
R=\left\{\left\{x_n\right\}:x_n\in R_n,\ \sum_n\left\|x_n\right\|^2< \infty\right\}
$$

按 $\left\langle\left\{x_n\right\},\left\{y_n\right\}\right\rangle=\sum_n\left\langle x_n,y_n\right\rangle$ 成为内积空间; 若每个 $R_n$ 是希尔伯特空间, 则 $R$ 也是希尔伯特空间.

## 定义 1.3.1 (正交系与标准正交系)

设 $\mathfrak F$ 是内积空间 $H$ 中的一族非零向量.

(i) 如果 $\mathfrak F$ 中任何两个不同的向量都正交, 就称 $\mathfrak F$ 是 $H$ 的正交系;

(ii) 如果正交系 $\mathfrak F$ 中每个向量的范数都等于 $1$,

就称 $\mathfrak F$ 是标准正交系 (规范正交系).

## 定理 1.3.1 (贝塞尔不等式)

设 $\mathfrak F=\left\{e_\lambda:\lambda\in\Lambda\right\}$ 是 Hilbert 空间 $H$ 中的标准正交系. 对每个 $x\in H$, 其 Fourier 系数 $\left\{\left\langle x,e_\lambda\right\rangle:\lambda\in\Lambda\right\}$ 中最多只有可列个不为零, 且 $\sum_{\lambda\in\Lambda}\left|\left\langle x,e_\lambda\right\rangle\right|^2\le\left\|x\right\|^2$.

## 定理 1.3.2 (标准正交基的等价条件)

设 $\mathfrak F=\left\{e_\lambda:\lambda\in\Lambda\right\}$ 是 Hilbert 空间 $H$ 中的标准正交系, 下列命题等价:

(i) 对任意 $x\in H$, $x=\sum_{\lambda\in\Lambda}\left\langle x,e_\lambda\right\rangle e_\lambda$;

(ii) $\overline{\operatorname{span}\left\{e_\lambda:\lambda\in\Lambda\right\}}=H$;

(iii) $\mathfrak F$ 是完全的, 即若 $x\in H$ 满足 $x\perp e_\lambda$ ($\forall\lambda\in\Lambda$), 则 $x=0$;

(iv) $\mathfrak F$ 是完备的, 即对任意 $x\in H$, 帕塞瓦尔等式 $\left\|x\right\|^2=\sum_{\lambda\in\Lambda}\left|\left\langle x,e_\lambda\right\rangle\right|^2$ 成立.

满足上述条件之一的标准正交系称为 $H$ 中的标准正交基.

## 定理 1.3.3 (标准正交系可扩张为标准正交基)

希尔伯特空间 $H$ 中的任意标准正交系都可扩张为 $H$ 的一组标准正交基.

## 例 1.3.3 (三角多项式标准正交系)

在实 (或复) 周期函数空间 $L^2\left[0,2\pi\right]$ 中, 规定内积 $\left\langle f,g\right\rangle=\frac{1}{2\pi}\int_0^{2\pi}f\left(x\right)\overline{g\left(x\right)}\,\mathrm dx$, 则

$$
\left\{1,\sqrt2\cos x,\sqrt2\sin x,\sqrt2\cos2x,\sqrt2\sin2x,\cdots,\sqrt2\cos nx,\sqrt2\sin nx,\cdots\right\}
$$

组成 $L^2\left[0,2\pi\right]$ 的标准正交系.

## 例 1.3.7 ($e^{inx}$ 构成标准正交基)

在复空间 $L^2\left[0,2\pi\right]$ 中, $\left\{e^{inx}:n\in\mathbb Z\right\}$ 是一组标准正交基.

## 例 1.3.8 (勒让德多项式)

在 $L^2\left[-1,1\right]$ 中, 函数列 $g_k\left(x\right)=x^k$ ($k=0,1,2,\cdots$) 是线性无关的. 勒让德多项式 $P_0\left(x\right)=1$, $P_n\left(x\right)=\frac{1}{2^n n!}\frac{\mathrm d^n}{\mathrm dx^n}\left(x^2-1\right)^n$ ($n=1,2,\cdots$) 是 $L^2\left[-1,1\right]$ 中的正交多项式系; 单位化后 $h_0\left(x\right)=\frac{1}{\sqrt2}$, $h_n\left(x\right)=\frac{1}{2^n n!}\sqrt{\frac{2n+1}{2}}\frac{\mathrm d^n}{\mathrm dx^n}\left(x^2-1\right)^n$ 是 $\left\{g_k\right\}$ 经过格拉姆-施密特过程得到的标准正交向量系.

## 例 1.3.9 (埃尔米特多项式构成完备正交系)

令 $H_n\left(t\right)=\left(-1\right)^n\mathrm e^{t^2}\frac{\mathrm d^n}{\mathrm dt^n}\mathrm e^{-t^2}$ 为埃尔米特多项式, 则加权多项式族 $\psi_n\left(t\right)=\left(2^n n!\sqrt\pi\right)^{-1/2}\mathrm e^{-t^2/2}H_n\left(t\right)$ 组成 $L^2\left(\mathbb R,\mathrm e^{-t^2}\mathrm dt\right)$ 中的完备标准正交系; 特别地, 多项式族关于权 $\mathrm e^{-t^2}$ 正交且完备.

## 定义 1.4.1 (内点、内部与开集)

设 $A$ 是度量空间 $\left(X,d\right)$ 的点集, $x_0\in A$. 若存在 $r> 0$ 使 $\left\{x:d\left(x,x_0\right)< r\right\}\subset A$, 则称 $x_0$ 是 $A$ 的内点; $A$ 的内点全体称为 $A$ 的内部; 若 $A$ 中每点都是内点, 则称 $A$ 是开集.

## 引理 1.4.1 (基本点列与完备性)

(i) 收敛点列是基本点列;

(ii) 基本点列若有收敛子列则自身收敛于同一极限;

(iii) 完备度量空间的闭子集是完备子空间;

(iv) 完备子空间是闭子集.

## 命题 1.4.1 (可分空间的子空间可分)

设 $\left(X,d\right)$ 可分, $A\subset X$, 则 $\left(A,d\right)$ 也是可分的.

## 定理 1.4.1 (连续映射的等价条件)

设 $f:X\to Y$ 是度量空间之间的映射, 下列条件等价:

(i) $f$ 连续;

(ii) $Y$ 中任一开集 $O$ 的原像 $f^{-1}\left(O\right)$ 是 $X$ 中的开集;

(iii) $Y$ 中任一闭集 $F$ 的原像 $f^{-1}\left(F\right)$ 是 $X$ 中的闭集.

## 例 1.4.1 (开球是开集)

度量空间中开球 $O\left(x_0,r\right)=\left\{x:d\left(x,x_0\right)< r\right\}$ 是开集.

## 注 1.4.1 ($L^p\left(\mathbb R^n\right)$ 中的稠密子集)

类似地, 可得 $L^p\left(\mathbb R^n\right)$ ($1\le p< \infty$) 中的简单函数全体、阶梯函数全体以及 $C_c^\infty\left(\mathbb R^n\right)$ 均是稠密子集.

## 定理 1.4.2 (有限维的赋范线性空间是完备的)

有限维赋范线性空间是完备的. 其证明中断言存在正实数 $c_1,c_2$, 使对 $X$ 中每个 $x=\sum_{i=1}^n x_i e_i$ 成立

$$
c_1\sqrt{\sum_{i=1}^n\left|x_i\right|^2}\le\left\|x\right\|\le c_2\sqrt{\sum_{i=1}^n\left|x_i\right|^2}
$$

即式 (1.21).

## 例 1.4.2 (闭球是闭集)

度量空间中闭球 $B\left(x_0,r\right)=\left\{x:d\left(x,x_0\right)\le r\right\}$ 是闭集.

## 定义 1.4.3 (极限点、导集、闭包与闭集)

(i) 若存在异于 $x_0$ 的点列 $x_n\to x_0$, 则 $x_0$ 是 $A$ 的极限点;

(ii) 极限点全体记为导集 $A'$, 闭包 $\overline A=A\cup A'$;

(iii) 若 $A'\subset A$, 则称 $A$ 是闭集.

## 例 1.4.3 (距离函数连续)

设 $F$ 是度量空间 $\left(X,d\right)$ 的非空子集, $d\left(x,F\right)=\inf_{z\in F}d\left(x,z\right)$. 由三角不等式得 $\left|d\left(x_1,F\right)-d\left(x_2,F\right)\right|\le d\left(x_1,x_2\right)$, 故 $x\mapsto d\left(x,F\right)$ 连续且一致连续.

## 定义 1.4.5 (稠密性)

在度量空间 $\left(X,d\right)$ 中, 对于 $X$ 中一个子集 $A$, 称 $A$ 在 $X$ 中稠密是指 $X\subset\overline A$ (即 $\overline A=X$).

## 例 1.4.5 (魏尔斯特拉斯第一逼近定理)

有界闭区间 $\left[a,b\right]$ 上, 多项式全体 $P$ 在 $C\left[a,b\right]$ 中稠密.

## 定义 1.4.6 (可分性)

若度量空间 $X$ 中存在可数稠密子集, 则称 $X$ 是可分空间.

## 例 1.4.6 ($L^p$ 中的稠密子集)

对直线上有界闭区间 $\left[a,b\right]$ 及 $1\le p< \infty$, $L^p\left[a,b\right]$ 中的简单函数全体、阶梯函数全体、$C_c^\infty\left(a,b\right)$、$C\left[a,b\right]$ 以及多项式全体 $P$ 均是 $L^p\left[a,b\right]$ 的稠密子集.

## 定义 1.4.7 (完备性)

(i) 若 $\left\{x_n\right\}$ 满足: 对任意 $\varepsilon> 0$, 存在 $N$, 使 $n,m\ge N$ 时 $d\left(x_n,x_m\right)< \varepsilon$, 则称 $\left\{x_n\right\}$ 是基本点列 (柯西点列);

(ii) 若每个基本点列都收敛, 则称 $X$ 完备;

(iii) 完备赋范线性空间称为巴拿赫空间;

(iv) 完备内积空间称为希尔伯特空间.

## 例 1.4.9 ($C$ 与 $L^{p}$ 的可分性)

$C\left[a,b\right]$ 和 $L^p\left[a,b\right]$ ($1\le p< \infty$) 是可分空间.

## 例 1.4.10 ($l^{\infty}$ 不可分)

有界数列空间 $l^\infty$ 是不可分的.

## 例 1.4.11 ($L^{\infty}$ 不可分)

$L^\infty\left[a,b\right]$ 是不可分的.

## 例 1.4.13 ($L^{p}\left(E\right)$ 是巴拿赫空间)

设 $E$ 是 $\mathbb R^n$ 的勒贝格可测集, 则 $L^p\left(E\right)$ ($1\le p< \infty$) 是巴拿赫空间; 特别地, $L^2\left(E\right)$ 是希尔伯特空间.

## 习题 1.4-15 (平均连续性)

设 $f\in L^{p}\left(\mathbb{R}\right)$, $1\le p< \infty$, 则

$$
\lim_{h\to0}\left(\int_{\mathbb{R}}\left|f\left(x+h\right)-f\left(x\right)\right|^{p}\,\mathrm dm\right)^{1/p}=0.
$$

## 定义 1.5.1 (不动点)

设 $X$ 为集合, $\varphi:X\to X$. 若 $x^*\in X$ 使 $\varphi\left(x^*\right)=x^*$, 则称 $x^*$ 是 $\varphi$ 的不动点.

## 定理 1.5.1 (巴拿赫不动点定理)

设 $X$ 是完备度量空间, $\varphi:X\to X$ 是压缩映射, 则 $\varphi$ 在 $X$ 中有唯一不动点 $x^*$; 对任意初值 $x_0$, 迭代 $x_n=\varphi^n\left(x_0\right)$ 收敛于 $x^*$, 且 $d\left(x^*,x_n\right)\le\frac{\alpha^n}{1-\alpha}d\left(x_1,x_0\right)$.

## 注 1.5.1 (迭代法的误差估计)

在定理 1.5.1 (巴拿赫不动点定理)的证明中, 令误差不等式两端取极限可得 $d\left(x^*,x_n\right)\le\frac{\alpha^n}{1-\alpha}d\left(x_1,x_0\right)$ 即式 (1.25).

## 定义 1.5.2 (压缩映射)

设 $\left(X,d\right)$ 是度量空间, $\varphi:X\to X$. 若存在 $0\le\alpha< 1$, 使对一切 $x,y\in X$ 有 $d\left(\varphi\left(x\right),\varphi\left(y\right)\right)\le\alpha d\left(x,y\right)$, 则称 $\varphi$ 是 $X$ 上的压缩映射, $\alpha$ 称为压缩系数.

## 定理 1.5.2 ($\varphi^{n}$ 压缩蕴含唯一不动点)

设完备度量空间 $X$ 上的映射 $\varphi$ 存在自然数 $n$, 使 $\varphi^n$ 是压缩映射, 则 $\varphi$ 在 $X$ 中有唯一不动点.

## 定理 1.5.3 (初值问题解的存在唯一性)

设 $f\left(x,y\right)$ 在区域 $D$ 上连续且关于 $y$ 满足利普希茨条件 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$, 则当 $h< \min\left\{a,\frac{\lambda}{M},\frac{1}{L}\right\}$ 时, 初值问题 $y'=f\left(x,y\right)$, $y\left(x_0\right)=y_0$ 在 $\left[x_0-h,x_0+h\right]$ 上有唯一解.

## 定义 1.6.1 (相对列紧集)

设 $A$ 是度量空间 $X$ 的子集. 若 $A$ 的闭包 $\overline{A}$ 是紧集, 则称 $A$ 是相对列紧集.

## 推论 1.6.1 (相对列紧集可分且有界)

相对列紧集是可分的有界集.

## 例 1.6.1 (有限维空间中相对列紧等价于有界)

在 $\mathbb R^n$ (及任意有限维赋范线性空间) 中, 子集 $A$ 是相对列紧集当且仅当 $A$ 是有界集; 有界闭集因此是紧集.

## 注 1.6.1 (网中的点不必属于集合本身)

$\varepsilon$-网中的点可以不必属于 $A$ 本身.

## 定理 1.6.2 (列紧 $\Leftrightarrow$ 覆盖紧)

度量空间 $X$ 是紧集当且仅当它是列紧集 (即 $X$ 中任意点列都有收敛子列).

## 定义 1.6.3 ($\varepsilon$-网与完全有界集)

设 $A$ 是度量空间 $X$ 的子集, $\varepsilon> 0$. 若存在 $X$ 的有限子集 $\left\{x_1,\dots,x_N\right\}$, 使得 $A\subset \bigcup_{i=1}^{N}U\left(x_i,\varepsilon\right)$, 则称 $\left\{x_1,\dots,x_N\right\}$ 是 $A$ 的一个 $\varepsilon$-网. 若对每个 $\varepsilon> 0$, $A$ 都有有限的 $\varepsilon$-网, 则称 $A$ 是完全有界集.

## 定理 1.6.3 (豪斯多夫定理)

设 $X$ 是完备的度量空间, $A\subset X$, 则 $A$ 是相对列紧集当且仅当 $A$ 是完全有界集.

## 推论 1.6.3 (连续函数达到上下确界)

设 $X$ 是紧度量空间, $f\in C\left(X\right)$, 则 $f$ 在 $X$ 上达到上确界与下确界.

## 例 1.6.3 ($\mathbb{R}^n$ 中有界集完全有界)

设 $A$ 是 $\mathbb{R}^n$ 中的有界集, 则 $A$ 是完全有界集.

## 定义 1.6.5 (一致连续与等度连续)

(i) 设 $f:X\to Y$ 是度量空间之间的映射. 若对每个 $\varepsilon> 0$ 存在 $\delta> 0$, 使得 $d_X\left(x_1,x_2\right)< \delta$ 蕴含 $d_Y\left(f\left(x_1\right),f\left(x_2\right)\right)< \varepsilon$, 则称 $f$ 一致连续.

(ii) 设 $X$ 是紧度量空间, $\mathscr{F}\subset C\left(X\right)$. 若对每个 $\varepsilon> 0$ 存在 $\delta> 0$, 使得对一切 $f\in\mathscr{F}$ 及 $x_1,x_2\in X$, 由 $d\left(x_1,x_2\right)< \delta$ 可推出 $\left|f\left(x_1\right)-f\left(x_2\right)\right|< \varepsilon$, 则称 $\mathscr{F}$ 是等度连续的.

## 定理 1.6.5 (阿泽拉-阿斯卡里定理)

设 $A\subset C\left[a,b\right]$, 则 $A$ 是相对列紧集当且仅当 $A$ 是有界的且等度连续的.

## 定理 1.6.7 (科尔莫戈罗夫-里斯-弗雷歇定理)

设 $A\subset L^{p}\left(\mathbb{R}\right)$, $1\le p< \infty$. 则 $A$ 是完全有界集当且仅当下列三条件同时成立:

(i) $A$ 是有界集;

(ii) (等度 $L^{p}$-胎紧) 对每个 $\varepsilon> 0$, 存在 $M> 0$, 使得 $\int_{\left\{\left|x\right|> M\right\}}\left|f\left(x\right)\right|^{p}\,\mathrm dm< \varepsilon^{p}$, $\forall f\in A$;

(iii) (等度 $L^{p}$-范数连续) 对每个 $\varepsilon> 0$, 存在 $\delta> 0$, 使得 $\left\|f\left(x+h\right)-f\left(x\right)\right\|_{p}\le\varepsilon$, $\forall f\in A$, $\forall \left|h\right|< \delta$.

## 定理 1.6.9 (紧度量空间上的性质)

设 $X$ 是紧的度量空间, 则:

(i) $X$ 上的连续函数是一致连续的;

(ii) $C\left(X\right)$ 按范数 $\left\|f\right\|=\max_{x\in X}\left|f\left(x\right)\right|$ 构成巴拿赫空间;

(iii) (阿泽拉-阿斯卡里定理) $A\subset C\left(X\right)$ 是相对列紧集当且仅当 $A$ 是有界的且等度连续的.
