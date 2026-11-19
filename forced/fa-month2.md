# 泛函分析: 第 2 次月考

## 定义 1.1.1 (度量空间)

设 $X$ 是一个非空集合, 若对于 $X$ 中任意两个元素 $x,y$, 都有一个实数 $d\left(x,y\right)$ 与它们对应, 而且满足下面条件: (i) (非负性与正定性) 对任意 $x,y\in{X}$, $d\left(x,y\right)\ge0$, 并且 $d\left(x,y\right)=0$ 的充要条件是 $x=y$; (ii) (对称性) 对任意 $x,y\in{X}$, $d\left(x,y\right)=d\left(y,x\right)$; (iii) (三角不等式) 对任意 $x,y,z\in{X}$, $d\left(x,y\right)\le{d}\left(x,z\right)+d\left(z,y\right)$, 则称 $\left(X,d\right)$ 是一个度量空间, $d$ 为 $X$ 上的度量.

## 定义 1.1.1 (度量空间)

设 $X$ 是一个非空集合, 若对于 $X$ 中任意两个元素 $x,y$, 有一个实数 $d\left(x,y\right)$ 与它们对应, 而且满足: (i) $d\left(x,y\right)\ge0$, $d\left(x,y\right)=0$ 当且仅当 $x=y$; (ii) $d\left(x,y\right)=d\left(y,x\right)$; (iii) $d\left(x,y\right)\le{d}\left(x,z\right)+d\left(z,y\right)$, 则称 $\left(X,d\right)$ 是度量空间.

## 定义 1.1.2 (极限)

设 $\left(X,d\right)$ 是度量空间, $\left\{x_n\right\}_{n=1}^\infty$ 是 $X$ 中点列, $x_0\in{X}$, 若 $\lim_{n\to\infty}d\left(x_n,x_0\right)=0$, 则称点列 $\left\{x_n\right\}$ 按照度量 $d$ 收敛于 $x_0$, 记为 $\lim_{n\to\infty}x_n=x_0$.

## 定义 1.1.2 (极限)

设 $\left(X,d\right)$ 是度量空间, $\left\{x_n\right\}_{n=1}^\infty$ 是 $X$ 中点列, $x_0\in{X}$, 若 $\lim_{n\to\infty}d\left(x_n,x_0\right)=0$, 则称点列 $\left\{x_n\right\}_{n=1}^\infty$ 按照度量 $d$ 收敛于 $x_0$, 记为 $\lim_{n\to\infty}x_n=x_0$.

## 定义 1.1.2 (极限)

设 $\left(X,d\right)$ 是度量空间, $\left\{x_n\right\}\subset{X}$, $x_0\in{X}$. 若 $\lim_{n\to\infty}d\left(x_n,x_0\right)=0$, 则称点列 $\left\{x_n\right\}$ 按度量 $d$ 收敛于 $x_0$.

## 例 1.1.2 ($n$ 维欧几里得空间)

在 $n$ 个有序实数组 $x=\left(x_1,x_2,\cdots,x_n\right)$ 全体组成的集合 $X$ 中, 定义 $d\left(x,y\right)=\sqrt{\sum_{i=1}^{n}\left(x_i-y_i\right)^2}$, 则 $\left(X,d\right)$ 是度量空间, 称为 $n$ 维欧几里得空间, 通常记为 $\mathbb{R}^n$.

## 例 1.1.10 (一致收敛与度量收敛)

由例 1.1.6 的讨论可知, $C\left[a,b\right]$ 中点列按度量 $d\left(f,g\right)=\max_{x\in\left[a,b\right]}\left|f\left(x\right)-g\left(x\right)\right|$ 收敛等价于区间 $\left[a,b\right]$ 上的函数列一致收敛.

## 例 1.1.12 (可测函数等价类空间)

对于有限区间 $\left[a,b\right]$, 记

$$
\mathfrak{G}=\left\{\left[a,b\right]\;\text{上几乎处处有限的勒贝格可测函数}\right\},
$$

$f,g\in\mathfrak{G}$ 等价是指 $f\overset{m}=g$, 仍以 $f$ 表示 $f$ 在 $\mathcal{S}=\mathfrak{G}/\sim$ 中对应的等价类; 对于 $f,g\in\mathcal{S}$, 定义 $d\left(f,g\right)=\int_{\left[a,b\right]}\frac{\left|f\left(t\right)-g\left(t\right)\right|}{1+\left|f\left(t\right)-g\left(t\right)\right|}\,\mathrm{d}m\left(t\right)$, 这是一个度量, 且 $d\left(f,g\right)=0$ 当且仅当 $f\overset{m}=g$.

## 习题 1.2-13 (内积空间的可数直和)

设 $R_n$ 都是内积空间,

$$
R=\left\{\left\{x_n\right\}:x_n\in{R}_n,\sum_n\left\|x_n\right\|^2<\infty\right\}
$$

按 $\left\langle\left\{x_n\right\},\left\{y_n\right\}\right\rangle=\sum_n\left\langle{x}_n,y_n\right\rangle$ 成为内积空间; 若每个 $R_n$ 是希尔伯特空间, 则 $R$ 也是希尔伯特空间.

## 定义 1.2.1 (哈梅尔基与维数)

线性空间 $X$ 上的一个极大线性无关组称为 $X$ 的一组哈梅尔基; 若哈梅尔基中只有有限个元素, 则称 $X$ 是有限维线性空间.

## 定义 1.2.1 (哈梅尔基)

线性空间 $X$ 上的一个极大线性无关组称为空间 $X$ 的一组哈梅尔基. 若 $X$ 的某个哈梅尔基中只有有限个元素, 则称 $X$ 是有限维线性空间, 否则称其为无限维线性空间.

## 定义 1.2.2 (半范数与范数)

记 $\mathbb{K}$ 是实数域 $\mathbb{R}$ 或复数域 $\mathbb{C}$. 对于 $\mathbb{K}$ 上的线性空间 $X$, 若每个向量 $x$ 都对应一个实数 $\left\|x\right\|$, 满足: (i) $\left\|x\right\|\ge0$; (ii) $\left\|\alpha{x}\right\|=\left|\alpha\right|\left\|x\right\|$; (iii) $\left\|x+y\right\|\le\left\|x\right\|+\left\|y\right\|$, 则称 $\left\|\cdot\right\|$ 为半范数. 若还满足 $\left\|x\right\|=0$ 当且仅当 $x=0$, 则称 $\left\|\cdot\right\|$ 为范数, $\left(X,\left\|\cdot\right\|\right)$ 称为赋范线性空间. 范数诱导度量 $d\left(x,y\right)=\left\|x-y\right\|$.

## 定义 1.2.2 (半范数与范数)

设 $X$ 是 $\mathbb{K}$ 上的线性空间. 若每个 $x\in{X}$ 对应实数 $\left\|x\right\|$, 满足 (i) $\left\|x\right\|\ge0$; (ii) $\left\|\alpha{x}\right\|=\left|\alpha\right|\left\|x\right\|$; (iii) $\left\|x+y\right\|\le\left\|x\right\|+\left\|y\right\|$, 则称 $\left\|\cdot\right\|$ 为半范数. 若还满足 $\left\|x\right\|=0\Leftrightarrow{x}=0$, 则称 $\left\|\cdot\right\|$ 为范数, $\left(X,\left\|\cdot\right\|\right)$ 称为赋范线性空间. 范数诱导度量 $d\left(x,y\right)=\left\|x-y\right\|$, 且 $\left\|\cdot\right\|$ 在该度量拓扑下连续.

## 定理 1.2.2 (勾股定理, 毕达哥拉斯定理)

对内积空间 $H$ 中两个元素 $x,y$, 若 $x\perp{y}$, 则 $\left\|x+y\right\|^2=\left\|x\right\|^2+\left\|y\right\|^2$.

## 定理 1.2.2 (毕达哥拉斯定理)

对内积空间 $H$ 中两个元素 $x,y$, 若 $x\perp{y}$, 则 $\left\|x+y\right\|^2=\left\|x\right\|^2+\left\|y\right\|^2$.

## 定义 1.2.3 (内积空间)

记 $\mathbb{K}$ 是实数域 $\mathbb{R}$ 或复数域 $\mathbb{C}$. 对于 $\mathbb{K}$ 上的线性空间 $H$, 如果任何两个向量 $x,y$ 都对应一个数 $\left\langle{x},y\right\rangle\in\mathbb{K}$, 满足: (i) 共轭对称性 $\left\langle{x},y\right\rangle=\overline{\left\langle{y},x\right\rangle}$; (ii) 对第一变元的线性性 $\left\langle\alpha{x}+\beta{y},z\right\rangle=\alpha\left\langle{x},z\right\rangle+\beta\left\langle{y},z\right\rangle$; (iii) 正定性 $\left\langle{x},x\right\rangle\ge0$ 且 $\left\langle{x},x\right\rangle=0$ 当且仅当 $x=0$, 则称 $\left\langle\cdot,\cdot\right\rangle$ 是 $H$ 中的内积, 称 $H$ 是内积空间.

## 定义 1.2.3 (内积空间)

记 $\mathbb{K}$ 是实数域 $\mathbb{R}$ 或复数域 $\mathbb{C}$. 对于 $\mathbb{K}$ 上的线性空间 $H$, 如果任何两个向量 $x,y$ 都对应一个数 $\left\langle{x},y\right\rangle\in\mathbb{K}$, 满足: (i) 共轭对称性 $\left\langle{x},y\right\rangle=\overline{\left\langle{y},x\right\rangle}$; (ii) 对第一变元的线性性 $\left\langle\alpha{x}+\beta{y},z\right\rangle=\alpha\left\langle{x},z\right\rangle+\beta\left\langle{y},z\right\rangle$; (iii) 正定性 $\left\langle{x},x\right\rangle\ge0$ 且 $\left\langle{x},x\right\rangle=0$ 当且仅当 $x=0$, 则称 $\left\langle\cdot,\cdot\right\rangle$ 是 $H$ 中的内积, 称 $H$ 是内积空间.

## 引理 1.2.3 (柯西-施瓦茨不等式)

设 $x,y\in{H}$ ($H$ 为内积空间), 则 $\left|\left\langle{x},y\right\rangle\right|^2\le\left\langle{x},x\right\rangle\left\langle{y},y\right\rangle$, 特别地当 $\left\|x\right\|=\left\|y\right\|=1$ 时 $\left|\left\langle{x},y\right\rangle\right|\le1$.

## 引理 1.2.3 (柯西-施瓦茨不等式)

设 $H$ 是内积空间, $x,y\in{H}$, 则 $\left|\left\langle{x},y\right\rangle\right|^2\le\left\langle{x},x\right\rangle\left\langle{y},y\right\rangle$.

## 引理 1.2.3 (柯西-施瓦茨不等式)

对内积空间中任意 $x,y$, 成立 $\left|\left\langle{x},y\right\rangle\right|^2\le\left\langle{x},x\right\rangle\left\langle{y},y\right\rangle$.

## 引理 1.2.3 (柯西-施瓦茨不等式)

对内积空间中任意 $x,y$, 成立 $\left|\left\langle{x},y\right\rangle\right|^2\le\left\langle{x},x\right\rangle\left\langle{y},y\right\rangle$.

## 引理 1.2.4 (内积的连续性)

设 $H$ 是内积空间, 则内积关于两个变元是连续的: 当 $x_n\to{x}$, $y_n\to{y}$ 时, 有 $\left\langle{x}_n,y_n\right\rangle\to\left\langle{x},y\right\rangle$.

## 例 1.2.8 ($L^p\left(E\right)$ 是巴拿赫空间)

设 $E$ 是欧几里得空间 $\mathbb{R}^k$ 的勒贝格可测集, $1\le{p}<\infty$, 则 $L^p\left(E\right)$ 按范数 $\left\|f\right\|_p=\left(\int_E\left|f\right|^p\,\mathrm{d}m\right)^{1/p}$ 是赋范线性空间, 且该范数诱导的度量是完备的, 即 $L^p\left(E\right)$ 是巴拿赫空间.

## 例 1.2.12 ($C\left[a,b\right]$ 是巴拿赫空间)

有限闭区间 $\left[a,b\right]$ 上的连续函数空间 $C\left[a,b\right]$ 按范数 $\left\|f\right\|=\max_{x\in\left[a,b\right]}\left|f\left(x\right)\right|$ 是巴拿赫空间.

## 定义 1.3.1 (正交系与标准正交系)

设 $\mathfrak{F}$ 是内积空间 $H$ 中的一族非零向量. (i) 如果 $\mathfrak{F}$ 中任何两个不同的向量都正交, 就称 $\mathfrak{F}$ 是 $H$ 的正交系; (ii) 如果正交系 $\mathfrak{F}$ 中每个向量的范数都等于 $1$, 就称 $\mathfrak{F}$ 是标准正交系 (规范正交系).

## 定理 1.3.1 (贝塞尔不等式)

设 $\mathfrak{F}=\left\{e_\lambda:\lambda\in\Lambda\right\}$ 是希尔伯特空间 $H$ 中的标准正交系. 对每个 $x\in{H}$, 其傅里叶系数 $\left\{\left\langle{x},e_\lambda\right\rangle:\lambda\in\Lambda\right\}$ 中最多只有可列个不为零, 且 $\sum_{\lambda\in\Lambda}\left|\left\langle{x},e_\lambda\right\rangle\right|^2\le\left\|x\right\|^2$.

## 定理 1.3.2 (标准正交基的等价条件)

设 $\mathfrak{F}=\left\{e_\lambda:\lambda\in\Lambda\right\}$ 是希尔伯特空间 $H$ 中的标准正交系, 下列命题等价: (i) 对任意 $x\in{H}$, $x=\sum_{\lambda\in\Lambda}\left\langle{x},e_\lambda\right\rangle{e}_\lambda$; (ii) $\overline{\operatorname{span}\left\{e_\lambda:\lambda\in\Lambda\right\}}=H$; (iii) $\mathfrak{F}$ 是完全的, 即若 $x\in{H}$ 满足 $x\perp{e}_\lambda$ ($\forall\lambda\in\Lambda$), 则 $x=0$; (iv) $\mathfrak{F}$ 是完备的, 即对任意 $x\in{H}$, 帕塞瓦尔等式 $\left\|x\right\|^2=\sum_{\lambda\in\Lambda}\left|\left\langle{x},e_\lambda\right\rangle\right|^2$ 成立. 满足上述条件之一的标准正交系称为 $H$ 中的标准正交基.

## 定理 1.3.2 (标准正交基的等价条件)

设 $\mathfrak{F}=\left\{e_\lambda:\lambda\in\Lambda\right\}$ 是希尔伯特空间 $H$ 中的标准正交系, 下列命题等价: (i) 对任意 $x\in{H}$, $x=\sum_{\lambda\in\Lambda}\left\langle{x},e_\lambda\right\rangle{e}_\lambda$; (ii) $\overline{\operatorname{span}\left\{e_\lambda:\lambda\in\Lambda\right\}}=H$; (iii) $\mathfrak{F}$ 是完全的, 即若 $x\in{H}$ 满足 $x\perp{e}_\lambda$ ($\forall\lambda\in\Lambda$), 则 $x=0$; (iv) $\mathfrak{F}$ 是完备的, 即对任意 $x\in{H}$, 帕塞瓦尔等式 $\left\|x\right\|^2=\sum_{\lambda\in\Lambda}\left|\left\langle{x},e_\lambda\right\rangle\right|^2$ 成立. 满足上述条件之一的标准正交系称为 $H$ 中的标准正交基.

## 定理 1.3.2 (标准正交基的等价条件)

设 $\mathfrak{F}=\left\{e_\lambda:\lambda\in\Lambda\right\}$ 是希尔伯特空间 $H$ 中的标准正交系, 下列命题等价: (i) 对任意 $x\in{H}$, $x=\sum_{\lambda\in\Lambda}\left\langle{x},e_\lambda\right\rangle{e}_\lambda$; (ii) $\overline{\operatorname{span}\left\{e_\lambda:\lambda\in\Lambda\right\}}=H$; (iii) $\mathfrak{F}$ 是完全的, 即若 $x\in{H}$ 满足 $x\perp{e}_\lambda$ ($\forall\lambda\in\Lambda$), 则 $x=0$; (iv) $\mathfrak{F}$ 是完备的, 即对任意 $x\in{H}$, 帕塞瓦尔等式 $\left\|x\right\|^2=\sum_{\lambda\in\Lambda}\left|\left\langle{x},e_\lambda\right\rangle\right|^2$ 成立. 满足上述条件之一的标准正交系称为 $H$ 中的标准正交基.

## 定理 1.3.3 (标准正交系可扩张为标准正交基)

希尔伯特空间 $H$ 中的任意标准正交系都可扩张为 $H$ 的一组标准正交基.

## 推论 1.3.3 (正交补与稠密性)

设 $H$ 是希尔伯特空间, $M$ 是 $H$ 的线性子空间, 那么 $\overline{M}=\left(M^\perp\right)^\perp$. 特别地, $M^\perp=\left\{0\right\}$ 的充要条件是 $M$ 在 $H$ 中稠密.

## 例 1.3.3 (三角多项式标准正交系)

在实 (或复) 周期函数空间 $L^2\left[0,2\pi\right]$ 中, 规定内积 $\left\langle{f},g\right\rangle=\frac{1}{2\pi}\int_0^{2\pi}f\left(x\right)\overline{g\left(x\right)}\,\mathrm{d}x$, 则

$$
\left\{1,\sqrt2\cos{x},\sqrt2\sin{x},\sqrt2\cos2x,\sqrt2\sin2x,\cdots,\sqrt2\cos{n}x,\sqrt2\sin{n}x,\cdots\right\}
$$

组成 $L^2\left[0,2\pi\right]$ 的标准正交系.

## 例 1.3.7 ($e^{inx}$ 构成标准正交基)

在复空间 $L^2\left[0,2\pi\right]$ 中, $\left\{e^{inx}:n\in\mathbb{Z}\right\}$ 是一组标准正交基.

## 例 1.3.9 (埃尔米特多项式构成完备正交系)

令 $H_n\left(t\right)=\left(-1\right)^n\mathrm{e}^{t^2}\frac{\mathrm{d}^n}{\mathrm{d}t^n}\mathrm{e}^{-t^2}$ 为埃尔米特多项式, 则加权多项式族 $\psi_n\left(t\right)=\left(2^nn!\sqrt\pi\right)^{-1/2}\mathrm{e}^{-t^2/2}H_n\left(t\right)$ 组成 $L^2\left(\mathbb{R},\mathrm{e}^{-t^2}\mathrm{d}t\right)$ 中的完备标准正交系; 特别地, 多项式族关于权 $\mathrm{e}^{-t^2}$ 正交且完备.

## 例 1.3.9 (埃尔米特多项式构成完备正交系)

令 $H_n\left(t\right)=\left(-1\right)^n\mathrm{e}^{t^2}\frac{\mathrm{d}^n}{\mathrm{d}t^n}\mathrm{e}^{-t^2}$ 为埃尔米特多项式, 则 $\psi_n\left(t\right)=\left(2^nn!\sqrt\pi\right)^{-1/2}\mathrm{e}^{-t^2/2}H_n\left(t\right)$ 组成 $L^2\left(\mathbb{R},\mathrm{e}^{-x^2}\mathrm{d}m\left(x\right)\right)$ 中的完备标准正交系.

## 习题 1.4-15 (平均连续性)

设 $f\in{L}^{p}\left(\mathbb{R}\right)$, $1\le{p}<\infty$, 则

$$
\lim_{h\to0}\left(\int_{\mathbb{R}}\left|f\left(x+h\right)-f\left(x\right)\right|^{p}\,\mathrm{d}m\right)^{1/p}=0.
$$

## 定义 1.4.1 (内点, 内部与开集)

设 $A$ 是度量空间 $\left(X,d\right)$ 的点集, $x_0\in{A}$. 若存在 $r>0$ 使 $\left\{x:d\left(x,x_0\right)<{}r\right\}\subset{A}$, 则称 $x_0$ 是 $A$ 的内点; $A$ 的内点全体称为 $A$ 的内部; 若 $A$ 中每点都是内点, 则称 $A$ 是开集.

## 引理 1.4.1 (基本点列与完备性)

设 $X$ 是度量空间, 则: (i) 基本点列是有界的; (ii) 若 $X$ 完备, 则点列收敛当且仅当它是基本点列; (iii) 完备度量空间的闭子集是完备的.

## 引理 1.4.1 (基本点列与完备性)

设 $X$ 是度量空间, 则: (i) 基本点列是有界的; (ii) 若 $X$ 完备, 则点列收敛当且仅当它是基本点列; (iii) 完备度量空间的闭子集是完备的.

## 命题 1.4.1 (可分空间的子空间可分)

设 $\left(X,d\right)$ 可分, $A\subset{X}$, 则 $\left(A,d\right)$ 也是可分的.

## 定理 1.4.1 (连续映射的等价条件)

设 $f:X\to{Y}$ 是度量空间之间的映射, 下列条件等价: (i) $f$ 连续; (ii) $Y$ 中任一开集 $O$ 的原像 $f^{-1}\left(O\right)$ 是 $X$ 中的开集; (iii) $Y$ 中任一闭集 $F$ 的原像 $f^{-1}\left(F\right)$ 是 $X$ 中的闭集.

## 注 1.4.1 ($L^p\left(\mathbb{R}\right)$ 中的稠密子集)

类似地, 可得 $L^p\left(\mathbb{R}\right)$ ($1\le{p}<\infty$) 中的简单函数全体, 阶梯函数全体以及 $C_c^\infty\left(\mathbb{R}\right)$ 均是稠密子集.

## 注 1.4.1 ($L^{p}$ 中的稠密子集)

(i) $L^p\left(\mathbb{R}^n\right)$ ($1\le{p}<\infty$) 中的简单函数全体, 阶梯函数全体以及 $C_c^\infty\left(\mathbb{R}^n\right)$ 均是稠密子集; (ii) 在 $L^\infty\left[a,b\right]$ 中只有简单函数全体稠密.

## 注 1.4.1 ($L^{p}$ 中的稠密子集)

(i) $L^p\left(\mathbb{R}^n\right)$ ($1\le{p}<\infty$) 中的简单函数全体, 阶梯函数全体以及 $C_c^\infty\left(\mathbb{R}^n\right)$ 均是稠密子集; (ii) 在 $L^\infty\left[a,b\right]$ 中只有简单函数全体稠密.

## 例 1.4.1 (开球是开集)

度量空间中开球 $O\left(x_0,r\right)=\left\{x:d\left(x,x_0\right)<{}r\right\}$ 是开集.

## 定理 1.4.2 (有限维赋范线性空间完备)

有限维的赋范线性空间是完备的.

## 定理 1.4.2 (有限维赋范线性空间完备)

有限维的赋范线性空间是完备的.

## 例 1.4.2 (闭球是闭集)

度量空间中闭球 $B\left(x_0,r\right)=\left\{x:d\left(x,x_0\right)\le{r}\right\}$ 是闭集.

## 定义 1.4.3 (极限点, 导集, 闭包与闭集)

(i) 若存在异于 $x_0$ 的点列 $x_n\to{x}_0$, 则 $x_0$ 是 $A$ 的极限点; (ii) 极限点全体记为导集 $A'$, 闭包 $\overline{A}=A\cup{A}'$; (iii) 若 $A'\subset{A}$, 则称 $A$ 是闭集.

## 例 1.4.3 (距离函数连续)

设 $F$ 是度量空间 $\left(X,d\right)$ 的非空子集, $d\left(x,F\right)=\inf_{z\in{F}}d\left(x,z\right)$. 由三角不等式得 $\left|d\left(x_1,F\right)-d\left(x_2,F\right)\right|\le{d}\left(x_1,x_2\right)$, 故 $x\mapsto{d}\left(x,F\right)$ 连续且一致连续.

## 定义 1.4.5 (稠密性)

在度量空间 $\left(X,d\right)$ 中, 对于 $X$ 中一个子集 $A$, 称 $A$ 在 $X$ 中稠密是指 $X\subset\overline{A}$ (即 $\overline{A}=X$).

## 定义 1.4.5 (稠密性)

在度量空间 $\left(X,d\right)$ 中, 对于 $X$ 中一个子集 $A$, 称 $A$ 在 $X$ 中稠密是指 $X\subset\overline{A}$ (即 $\overline{A}=X$).

## 定义 1.4.5 (稠密性)

在度量空间 $\left(X,d\right)$ 中, 对于 $X$ 中一个子集 $A$, 称 $A$ 在 $X$ 中稠密是指 $X\subset\overline{A}$ (即 $\overline{A}=X$).

## 例 1.4.5 (魏尔斯特拉斯第一逼近定理)

有界闭区间 $\left[a,b\right]$ 上, 多项式全体 $P$ 在 $C\left[a,b\right]$ 中稠密.

## 定义 1.4.6 (可分性)

若度量空间 $X$ 中存在可数稠密子集, 则称 $X$ 是可分空间.

## 例 1.4.6 ($L^p$ 中的稠密子集)

对直线上有界闭区间 $\left[a,b\right]$ 及 $1\le{p}<\infty$, $L^p\left[a,b\right]$ 中的简单函数全体, 阶梯函数全体, $C_c^\infty\left(a,b\right)$, $C\left[a,b\right]$ 以及多项式全体 $P$ 均是 $L^p\left[a,b\right]$ 的稠密子集.

## 定义 1.4.7 (完备性)

(i) 若 $\left\{x_n\right\}$ 满足: 对任意 $\varepsilon>0$, 存在 $N$, 使 $n,m\ge{N}$ 时 $d\left(x_n,x_m\right)<\varepsilon$, 则称 $\left\{x_n\right\}$ 是基本点列 (柯西点列); (ii) 若每个基本点列都收敛, 则称 $X$ 完备; (iii) 完备赋范线性空间称为巴拿赫空间; (iv) 完备内积空间称为希尔伯特空间.

## 定义 1.4.7 (完备性)

(i) 若 $\left\{x_n\right\}$ 满足: 对任意 $\varepsilon>0$, 存在 $N$, 使 $n,m\ge{N}$ 时 $d\left(x_n,x_m\right)<\varepsilon$, 则称 $\left\{x_n\right\}$ 是基本点列 (柯西点列); (ii) 若每个基本点列都收敛, 则称 $X$ 完备; (iii) 完备赋范线性空间称为巴拿赫空间; (iv) 完备内积空间称为希尔伯特空间.

## 例 1.4.9 ($C$ 与 $L^{p}$ 的可分性)

$C\left[a,b\right]$ 和 $L^p\left[a,b\right]$ ($1\le{p}<\infty$) 是可分空间.

## 例 1.4.10 ($l^{\infty}$ 不可分)

有界数列空间 $l^\infty$ 是不可分的.

## 例 1.4.11 ($L^{\infty}$ 不可分)

$L^\infty\left[a,b\right]$ 是不可分的.

## 例 1.4.13 ($L^{p}\left(E\right)$ 是巴拿赫空间)

设 $E$ 是 $\mathbb{R}^n$ 的勒贝格可测集, 则 $L^p\left(E\right)$ ($1\le{p}<\infty$) 是巴拿赫空间; 特别地, $L^2\left(E\right)$ 是希尔伯特空间.

## 例 1.4.13 ($L^{p}\left(E\right)$ 是巴拿赫空间)

设 $E$ 是 $\mathbb{R}^n$ 的勒贝格可测集, 则 $L^p\left(E\right)$ ($1\le{p}<\infty$) 是巴拿赫空间; 特别地, $L^2\left(E\right)$ 是希尔伯特空间.

## 定义 1.5.1 (不动点)

设 $X$ 为集合, $\varphi:X\to{X}$. 若 $x^*\in{X}$ 使 $\varphi\left(x^*\right)=x^*$, 则称 $x^*$ 是 $\varphi$ 的不动点.

## 定理 1.5.1 (巴拿赫不动点定理)

设 $X$ 是完备度量空间, $\varphi:X\to{X}$ 是压缩映射, 则 $\varphi$ 在 $X$ 中有唯一不动点 $x^*$; 对任意初值 $x_0$, 迭代 $x_n=\varphi^n\left(x_0\right)$ 收敛于 $x^*$, 且 $d\left(x^*,x_n\right)\le\frac{\alpha^n}{1-\alpha}d\left(x_1,x_0\right)$.

## 定理 1.5.1 (巴拿赫不动点定理)

设 $X$ 是完备的度量空间, $T:X\to{X}$ 是压缩映射, 则 $T$ 在 $X$ 中存在唯一的不动点 $x$; 且对任意的 $x_0\in{X}$, 迭代序列 $x_n=T^{n}x_0$ 收敛于 $x$, 误差估计 $d\left(x_n,x\right)\le\frac{\theta^{n}}{1-\theta}d\left(x_0,Tx_0\right)$.

## 注 1.5.1 (迭代法的误差估计)

在**定理 1.5.1 (巴拿赫不动点定理)** 的证明中, 令误差不等式两端取极限可得 $d\left(x^*,x_n\right)\le\frac{\alpha^n}{1-\alpha}d\left(x_1,x_0\right)$.

## 定义 1.5.2 (压缩映射)

设 $\left(X,d\right)$ 是度量空间, $\varphi:X\to{X}$. 若存在 $0\le\alpha<1$, 使对一切 $x,y\in{X}$ 有 $d\left(\varphi\left(x\right),\varphi\left(y\right)\right)\le\alpha{d}\left(x,y\right)$, 则称 $\varphi$ 是 $X$ 上的压缩映射, $\alpha$ 称为压缩系数.

## 定理 1.5.2 ($\varphi^{n}$ 压缩蕴含唯一不动点)

设完备度量空间 $X$ 上的映射 $\varphi$ 存在自然数 $n$, 使 $\varphi^n$ 是压缩映射, 则 $\varphi$ 在 $X$ 中有唯一不动点.

## 定理 1.5.3 (初值问题解的存在唯一性)

设 $f\left(x,y\right)$ 在区域 $D$ 上连续且关于 $y$ 满足利普希茨条件 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le{L}\left|y_1-y_2\right|$, 则当 $h<\min\left\{a,\frac{\lambda}{M},\frac{1}{L}\right\}$ 时, 初值问题 $y'=f\left(x,y\right)$, $y\left(x_0\right)=y_0$ 在 $\left[x_0-h,x_0+h\right]$ 上有唯一解.

## 定义 1.6.1 (相对列紧集)

设 $X$ 是度量空间, $A$ 是 $X$ 的子集. 如果 $A$ 中的任何点列都有在 $X$ 中收敛的子列, 就称 $A$ 是 $X$ 中的相对列紧集; 如果 $X$ 自身是相对列紧集, 就称 $X$ 是列紧空间.

## 定理 1.6.1 (无限维空间的单位球不相对列紧)

如果赋范线性空间 $X$ 是无限维的, 那么 $X$ 的单位球不是相对列紧的.

## 推论 1.6.1 (相对列紧集可分且有界)

相对列紧集是可分的有界集.

## 注 1.6.1 (网中的点不必属于集合本身)

$\varepsilon$-网中的点可以不必属于 $A$ 本身.

## 例 1.6.1 (有限维空间中相对列紧等价于有界)

在 $\mathbb{R}^n$ (及任意有限维赋范线性空间) 中, 子集 $A$ 是相对列紧集当且仅当 $A$ 是有界集; 有界闭集因此是紧集.

## 定理 1.6.2 (列紧 $\Leftrightarrow$ 覆盖紧)

度量空间 $X$ 是紧集当且仅当它是列紧集 (即 $X$ 中任意点列都有收敛子列).

## 定义 1.6.3 ($\varepsilon$-网与完全有界集)

设 $A$ 是度量空间 $X$ 的子集, $\varepsilon>0$. 若存在 $X$ 的有限子集 $\left\{x_1,\dots,x_N\right\}$, 使得 $A\subset\bigcup_{i=1}^{N}U\left(x_i,\varepsilon\right)$, 则称 $\left\{x_1,\dots,x_N\right\}$ 是 $A$ 的一个 $\varepsilon$-网. 若对每个 $\varepsilon>0$, $A$ 都有有限的 $\varepsilon$-网, 则称 $A$ 是完全有界集.

## 定理 1.6.3 (豪斯多夫定理)

设 $X$ 是完备的度量空间, $A\subset{X}$, 则 $A$ 是相对列紧集当且仅当 $A$ 是完全有界集.

## 推论 1.6.3 (连续函数达到上下确界)

度量空间 $X$ 的紧子集 $K$ 上的连续函数 $f$ 有界, 且上, 下确界在 $K$ 上达到.

## 推论 1.6.3 (连续函数达到上下确界)

设 $X$ 是紧度量空间, $f\in{C}\left(X\right)$, 则 $f$ 在 $X$ 上达到上确界与下确界.

## 例 1.6.3 ($\mathbb{R}^n$ 中有界集完全有界)

设 $A$ 是 $\mathbb{R}^n$ 中的有界集, 则 $A$ 是完全有界集.

## 定理 1.6.5 (阿泽拉-阿斯卡里定理)

设 $A\subset{C}\left[a,b\right]$, 则 $A$ 是相对列紧集当且仅当 $A$ 是有界的且等度连续的.

## 定理 1.6.7 (科尔莫戈罗夫-里斯-弗雷歇定理)

设 $A\subset{L}^{p}\left(\mathbb{R}\right)$, $1\le{p}<\infty$. 则 $A$ 是完全有界集当且仅当下列三条件同时成立: (i) $A$ 是有界集; (ii) (等度 $L^{p}$-胎紧) 对每个 $\varepsilon>0$, 存在 $M>0$, 使得 $\int_{\left\{\left|x\right|>M\right\}}\left|f\left(x\right)\right|^{p}\,\mathrm{d}m<\varepsilon^{p}$, $\forall{f}\in{A}$; (iii) (等度 $L^{p}$-范数连续) 对每个 $\varepsilon>0$, 存在 $\delta>0$, 使得 $\left\|f\left(x+h\right)-f\left(x\right)\right\|_{p}\le\varepsilon$, $\forall{f}\in{A}$, $\forall\left|h\right|<\delta$.

## 定理 1.6.9 (紧度量空间上的性质)

设 $X$ 是紧的度量空间, 则: (i) $X$ 上的连续函数是一致连续的; (ii) $C\left(X\right)$ 按范数 $\left\|f\right\|=\max_{x\in{X}}\left|f\left(x\right)\right|$ 构成巴拿赫空间; (iii) (阿泽拉-阿斯卡里定理) $A\subset{C}\left(X\right)$ 是相对列紧集当且仅当 $A$ 是有界的且等度连续的.

## 定理 2.1.1 (线性算子有界与连续的等价条件)

设 $\left(X,\left\|\cdot\right\|\right),\left(Y,\left\|\cdot\right\|\right)$ 是赋范线性空间, $T:X\to{Y}$ 是线性映射, 则下列命题等价: (i) $T$ 是连续映射; (ii) $T$ 在点 $0$ 连续; (iii) 存在 $M>0$, 使得 $\left\|Tx\right\|\le{M}\left\|x\right\|$. 如果算子 $T$ 满足定理中任一条件, 就称 $T$ 是有界算子; 否则就称 $T$ 为无界算子.

## 例 2.1.1 (矩阵表示的线性算子)

设 $\mathbb{K}^n$ 是 $n$ 维 (实或复系数) 向量空间, 在 $\mathbb{K}^n$ 中取一组基 $\left\{e_1,e_2,\cdots,e_n\right\}$. 相应于任意一个 $n$ 阶方阵 $\left(t_{ji}\right)$, 作 $\mathbb{K}^n\to\mathbb{K}^n$ 的算子 $T$ 如下: 当 $x=\sum_{i=1}^{n}x_ie_i$ 时, $y=Tx=\sum_{j=1}^{n}y_je_j$, 其中 $y_j=\sum_{i=1}^{n}t_{ji}x_i$ ($j=1,2,\cdots,n$). 这样定义的 $T$ 是一个线性算子, 这个算子在线性代数中称为线性变换. 算子 $T$ 显然由矩阵 $\left(t_{ji}\right)$ 唯一确定, 有时就直接记为 $T=\left(t_{ji}\right)$.

## 定义 2.1.2 (算子范数)

设 $T$ 为赋范线性空间 $X$ 到赋范线性空间 $Y$ 的有界算子, 称 $\left\|T\right\|=\sup_{x\neq0}\frac{\left\|Tx\right\|}{\left\|x\right\|}$ 为算子 $T$ 的范数. 对有界线性算子 $T$, 成立 $\left\|Tx\right\|\le\left\|T\right\|\left\|x\right\|,\quad\forall{x}\in{X}$.

## 定义 2.1.2 (算子范数)

设 $T$ 为赋范线性空间 $X$ 到赋范线性空间 $Y$ 的有界算子, 称 $\left\|T\right\|=\sup_{x\neq0}\frac{\left\|Tx\right\|}{\left\|x\right\|}$ 为算子 $T$ 的范数. 对有界线性算子 $T$, 成立 $\left\|Tx\right\|\le\left\|T\right\|\left\|x\right\|,\quad\forall{x}\in{X}$.

## 例 2.1.6 (傅里叶变换)

对 $f\in{L}^1\left(\mathbb{R}\right)$, 定义它的傅里叶变换 $\mathcal{F}\left(f\right)$ (或记作 $\widehat{f}$) 为

$$
\mathcal{F}\left(f\right)\left(t\right)=\int_{\mathbb{R}}f\left(x\right)\mathrm{e}^{-2\pi\mathrm{i}tx}\,\mathrm{d}x,\quad{f}\in{L}^1\left(\mathbb{R}\right),
$$

则 $\widehat{f}$ 是 $\mathbb{R}$ 上的连续函数, 且当 $\left|t\right|\to\infty$ 时 $\widehat{f}\left(t\right)\to0$; 因此 $\mathcal{F}:f\mapsto\widehat{f}$ 是 $L^1\left(\mathbb{R}\right)$ 到 $c_0\left(\mathbb{R}\right)$ 的线性算子.

## 例 2.1.8 (有限维赋范空间上的线性算子连续)

有限维赋范空间中的线性算子是连续算子.

## 例 2.1.9 (微分算子的无界性)

设 $X=C^{\left(1\right)}\left[a,b\right]$, 视 $X$ 为 $C\left[a,b\right]$ 的子空间 (就是说, $X$ 中的范数取为 $C\left[a,b\right]$ 中的范数) 时, $X$ 也成为一个赋范线性空间. 定义算子 $D:X\to{C}\left[a,b\right]$ 如下: $\left(Dx\right)\left(t\right)=\frac{\mathrm{d}}{\mathrm{d}t}x\left(t\right),\quad\forall{x}\in{X}$. 那么 $D$ 显然是线性算子. $D$ 是无界的: 取 $x_n\left(t\right)=\mathrm{e}^{-n\left(t-a\right)}$, 则 $\left\|x_n\right\|=1$, 但 $\left(Dx_n\right)\left(t\right)=-n\mathrm{e}^{-n\left(t-a\right)}$, 故 $\left\|Dx_n\right\|=n\to\infty$.

## 例 2.2.1 (线性泛函的核 (iv))

设 $1\le{q}\le\infty$, $\frac1q+\frac1p=1$. 对于 $\varphi\in{L}^q\left[a,b\right]$, 令 $F_\varphi\left(\psi\right)=\int_{\left[a,b\right]}\psi\left(t\right)\overline{\varphi\left(t\right)}\,\mathrm{d}t$, 由赫尔德不等式, $F_\varphi$ 为 $L^p\left[0,1\right]$ 上的有界线性泛函, 且 $\left\|F_\varphi\right\|=\left\|\varphi\right\|_q$. 它的核

$$
\ker{F}_\varphi=\left\{\psi\in{L}^p\left[0,1\right]:\,\int_0^1\psi\left(t\right)\overline{\varphi\left(t\right)}\,\mathrm{d}t=0\right\}.
$$

## 定义 2.2.2 (保范算子与同构)

设 $X,Y$ 是两个赋范线性空间, $U$ 是 $X$ 到 $Y$ 的映射. (i) 如果对一切 $x\in{X}$, 有 $\left\|Ux\right\|=\left\|x\right\|$, 那么称 $U$ 是 $X$ 到 $Y$ 的保范算子; (ii) 如果 $U$ 不但是保范的, 又是线性的, 而且还实现 $X$ 到 $Y$ 上的一一对应, 那么我们就称 $U$ 是 $X$ 到 $Y$ 上的 (保范) 同构映射; (iii) 若空间 $X,Y$ 之间存在一个从 $X$ 到 $Y$ 上的 (保范) 同构映射, 就称 $X$ 和 $Y$ 同构, 记为 $X\cong{Y}$.

## 定理 2.2.2 (里斯表示定理)

设 $H$ 是希尔伯特空间, $F$ 是 $H$ 上的连续线性泛函, 那么存在唯一的向量 $y\in{H}$, 使得 $F\left(x\right)=\left\langle{x},y\right\rangle,\quad\forall{x}\in{H}$, 并且 $\left\|F\right\|=\left\|y\right\|$.

## 例 2.2.2 (算子导出的共轭双线性泛函)

设 $T$ 是 $H$ 上的线性算子, 则 $T$ 导出的泛函 $\varphi\left(x,y\right)=\left(Tx,y\right)$ 是共轭双线性泛函. 如果 $T$ 还是有界的, 那么 $\varphi$ 也是有界的共轭双线性泛函且 $\left\|\varphi\right\|=\left\|T\right\|$.

## 定义 2.2.3 (共轭双线性泛函)

设 $H$ 是内积空间, $\varphi\left(x,y\right)$ 是 $H$ 上的二元泛函. (i) 如果对于任何 $x,y,z\in{H}$ 及 $\alpha,\beta\in\mathbb{C}$, 都成立

$$
\varphi\left(\alpha{x}+\beta{y},z\right)=\alpha\varphi\left(x,z\right)+\beta\varphi\left(y,z\right),\quad\varphi\left(z,\alpha{x}+\beta{y}\right)=\overline\alpha\varphi\left(z,x\right)+\overline\beta\varphi\left(z,y\right),
$$

那么称 $\varphi\left(\cdot,\cdot\right)$ 是 $H$ 上的共轭双线性泛函. (ii) 如果对于任何 $x,y\in{H}$ 成立 $\varphi\left(x,y\right)=\overline{\varphi\left(y,x\right)}$, 那么称 $\varphi\left(x,y\right)$ 是 $H$ 上的埃尔米特泛函. (iii) 对共轭双线性泛函 $\varphi$, 如果有正常数 $c$ 使得 $\left|\varphi\left(x,y\right)\right|\le{c}\left\|x\right\|\left\|y\right\|,\quad\forall{x},y\in{H}$, 那么称 $\varphi$ 是 $H$ 上有界的共轭双线性泛函, $\left\|\varphi\right\|=\sup_{\left\|x\right\|=\left\|y\right\|=1}\left|\varphi\left(x,y\right)\right|$ 称为泛函 $\varphi$ 的范数. ## 2.1-1 (零空间闭并不蕴含算子有界) 设 $T$ 是赋范线性空间 $X$ 到赋范线性空间 $Y$ 的线性算子. 如果零空间 $\ker\left(T\right)=\left\{x:Tx=0\right\}$ 是闭集, 问 $T$ 是否有界? 不一定. 反例取自**例 2.1.9 (微分算子的无界性)**: 取 $X=C^{\left(1\right)}\left[a,b\right]$ 按 $C\left[a,b\right]$ 的范数 $\left\|x\right\|=\max_{t\in\left[a,b\right]}\left|x\left(t\right)\right|$, $Y=C\left[a,b\right]$, $T=D$, 其中 $$ \left(Dx\right)\left(t\right)=\frac{\mathrm{d}}{\mathrm{d}t}x\left(t\right),\quad{x}\in{X}. $$ 先证 $\ker{D}$ 是 $X$ 的闭集. 由 $Dx=0$ 当且仅当 $x'$ 在 $\left[a,b\right]$ 上恒为 $0$, 而闭区间上导数恒为 $0$ 的函数是常值函数, 故

$$
\ker{D}=\left\{x\in{X}:\,\exists\,c\in\mathbb{R},x\left(t\right)=c,\forall\,t\in\left[a,b\right]\right\}.
$$

设 $\left\{x_n\right\}\subset\ker{D}$ 且 $x_n\to{x}$ 于 $X$, 则 $x_n\equiv{c}=x$, $\forall\,n\in\mathbb{N}$. 故 $x\in\ker{D}$, 即 $\ker{D}$ 闭. $\blacksquare$ 再证 $D$ 无界. 取 $x_n\left(t\right)=\mathrm{e}^{-n\left(t-a\right)}$, 则 $\left\|x_n\right\|=\max_t\mathrm{e}^{-n\left(t-a\right)}=1$, 而 $\left(Dx_n\right)\left(t\right)=-n\mathrm{e}^{-n\left(t-a\right)}$, 故 $\left\|Dx_n\right\|=n$ 无界. $\blacksquare$

## 定理 2.2.6 (埃尔米特泛函的有界性)

设 $\varphi\left(\cdot,\cdot\right)$ 是复希尔伯特空间 $H$ 上的共轭双线性埃尔米特泛函, 且存在常数 $c$ 使得 $\left|\varphi\left(x,x\right)\right|\le{c}\left\|x\right\|^2,\quad\forall{x}\in{H}$, 那么 $\varphi$ 是有界的, 且 $\left\|\varphi\right\|\le{c}$.

## 定理 2.3.1 (哈恩-巴拿赫延拓定理)

设 $L_0$ 是实赋范线性空间 $L$ 的线性子空间. 若 $f_0$ 是 $L_0$ 上的有界线性泛函, 则存在 $L$ 上的有界线性泛函 $f$, $f|_{L_0}=f_0$, 且 $\left\|f\right\|=\left\|f_0\right\|$.

## 定理 2.3.1 (哈恩-巴拿赫延拓定理)

设 $L_0$ 是实赋范线性空间 $L$ 的线性子空间. 若 $f_0$ 是 $L_0$ 上的有界线性泛函, 则存在 $L$ 上的有界线性泛函 $f$, $f|_{L_0}=f_0$, 且 $\left\|f\right\|=\left\|f_0\right\|$.

## 推论 2.3.1 (范数可达的泛函)

对赋范线性空间 $X$ 中的非零元素 $x_0$, 存在 $f\in{X}^{*}$ 使得 $\left\|f\right\|=1$ 且 $f\left(x_0\right)=\left\|x_0\right\|$.

## 推论 2.3.4 (闭线性子空间与点的分离)

设 $M$ 是赋范线性空间 $\left(X,\left\|\cdot\right\|\right)$ 的闭线性子空间, $x\notin{M}$, 则存在 $f\in{X}^{*}$ 使得 $\left\|f\right\|=1$, $f\left(M\right)=0$, $f\left(x\right)=d\left(x,M\right)$.

## 推论 2.3.4 (闭线性子空间与点的分离)

设 $M$ 是赋范线性空间 $\left(X,\left\|\cdot\right\|\right)$ 的闭线性子空间, $x\notin{M}$, 则存在 $f\in{X}^*$ 使得 $\left\|f\right\|=1$, $f\left(M\right)=0$, $f\left(x\right)=d\left(x,M\right)$.

## 定义 2.4.1 (凸集)

设 $V$ 是线性空间, $M$ 是 $V$ 的一个子集. 如果对于任意的 $x,y\in{M}$, 及数 $\alpha\in\left[0,1\right]$, 有 $\alpha{x}+\left(1-\alpha\right)y\in{M}$, 就称 $M$ 是一个凸集.

## 定义 2.4.1 (凸集)

设 $V$ 是线性空间, $M$ 是 $V$ 的一个子集. 如果对于任意的 $x,y\in{M}$, 及数 $\alpha\in\left[0,1\right]$, 有 $\alpha{x}+\left(1-\alpha\right)y\in{M}$, 就称 $M$ 是一个凸集.

## 引理 2.4.1 (一点与凸集的分离)

设 $A$ 是实赋范线性空间 $L$ 中的凸子集, 如果 $A$ 的内部 $A^\circ$ 是非空的, 并且 $y_0\notin{A}^\circ$, 则 $L$ 上存在非零的连续线性泛函 $f$, 使得 $f\left(x\right)\le{f}\left(y_0\right)$ 对一切 $x\in{A}$ 成立.

## 定理 2.4.1 (凸集分离定理)

设 $M$ 与 $N$ 是实赋范线性空间 $L$ 中的凸集, 如果 $M$ 的内部 $M^\circ$ 是非空的, 并且 $M^\circ\cap{N}=\emptyset$, 则存在 $L$ 上非零的连续线性泛函 $f$ 分离 $M$ 与 $N$, 即 $\sup_{x\in{M}}f\left(x\right)\le\inf_{x\in{N}}f\left(x\right)$.

## 推论 2.4.1 (闭凸集与紧凸集的严格分离)

设 $M,N$ 是实赋范线性空间 $L$ 中的闭凸集, $d\left(M,N\right)=\inf_{x\in{M},y\in{N}}d\left(x,y\right)>0$, 则存在 $L$ 上的非零连续线性泛函 $f$ 严格分离 $M$ 与 $N$, 即 $\sup_{x\in{M}}f\left(x\right)<\inf_{y\in{N}}f\left(y\right)$.

## 注 2.4.1 (复赋范线性空间的实部分离)

设 $A$ 是复赋范线性空间 $L$ 中的凸子集, 如果 $A^\circ$ 是非空的, 并且 $y_0\notin{A}^\circ$, 则 $L$ 上存在非零的连续线性泛函 $f$, 使得 $\sup_{x\in{A}}\operatorname{Re}f\left(x\right)\le\operatorname{Re}f\left(y_0\right)$.

## 定义 2.4.2 (闵可夫斯基泛函)

设 $M$ 是线性空间 $V$ 中吸收的凸集. 对于任意的 $x\in{V}$, 定义 $p_M\left(x\right)=\inf\left\{\alpha:\alpha>0,\alpha^{-1}x\in{M}\right\}$, 称 $p_M$ 为 $M$ 的闵可夫斯基泛函.

## 例 2.4.2 (凸函数的上方图是凸集)

若 $\varphi$ 是直线 $\mathbb{R}$ 上的凸函数, 即

$$
\varphi\left(tx+\left(1-t\right)y\right)\le{t}\varphi\left(x\right)+\left(1-t\right)\varphi\left(y\right), \forall{x},y\in\mathbb{R}, t\in\left(0,1\right),
$$

那么图形 $\left\{\left(x,y\right)\in\mathbb{R}^2:y\ge\varphi\left(x\right)\right\}$ 是平面中的一个凸集.

## 定义 2.4.3 (分离与严格分离)

设 $V$ 是实线性空间, $M$ 与 $N$ 是它的子集, $f$ 是 $V$ 上的线性泛函. (i) 如果存在常数 $C$, 使得 $f\left(x\right)\le{C}$, $\forall{x}\in{M}$ 与 $f\left(y\right)\ge{C}$, $\forall{y}\in{N}$, 即

$$
\sup\left\{f\left(x\right):x\in{M}\right\}\le\inf\left\{f\left(x\right):x\in{N}\right\},
$$

则称线性泛函 $f$ 分离集 $M$ 与 $N$. (ii) 如果线性泛函 $f$ 满足

$$
\sup\left\{f\left(x\right):x\in{M}\right\}<\inf\left\{f\left(x\right):x\in{N}\right\},
$$

则称 $f$ 严格分离 $M$ 与 $N$.

## 命题 2.4.3 (吸收凸集的闵可夫斯基泛函)

设 $M$ 是线性空间 $V$ 中的一个吸收凸子集, 那么 $M$ 的闵可夫斯基泛函 $p_M\left(x\right)$ 是 $V$ 上的一个次线性泛函, 并且

$$
\left\{x:p_M\left(x\right)<1\right\}\subset{M}\subset\left\{x:p_M\left(x\right)\le1\right\}.
$$

如果 $M$ 还是均衡的, 那么 $p_M\left(x\right)$ 是 $V$ 上的一个半范数.

## 定义 2.5.1 (自反空间)

设 $X$ 是赋范线性空间, $J$ 是典则映射. 如果 $J:X\to{X}^{**}$ 是同构, 就称 $X$ 是自反的.

## 注 2.5.1 (一般可测空间上 $L^p$ 的对偶)

设 $\left(X,\mathcal{R}\right)$ 是一个可测空间, $\mu$ 是它的一个 $\sigma$-有限测度. 对赋范线性空间 $L^p\left(X,\mu\right)$ ($1\le{p}<\infty$) 上的一个连续线性泛函 $\psi$, 都存在唯一的 $g\in{L}^q\left(X,\mu\right)$ ($\frac1p+\frac1q=1$), 使得 $\psi\left(f\right)=\int_Xf\left(x\right)g\left(x\right)\,\mathrm{d}\mu\left(x\right)$, $\forall{f}\in{L}^p\left(X,\mu\right)$, 且此时 $\left\|\psi\right\|=\left\|g\right\|_q$.

## 定理 2.5.2 (里斯表示定理)

设 $X$ 是紧度量空间. 对实 (复) 连续函数空间 $C\left(X\right)$ 上的一个连续线性泛函 $f$, 存在 $X$ 上唯一的全有限广义测度 (复测度) $\mu$ 使得 $f\left(x\right)=\int_Xx\left(t\right)\,\mathrm{d}\mu\left(t\right)$, $\forall{x}\in{C}\left(X\right)$, 并且 $\left\|f\right\|=\left|\mu\right|\left(X\right)$, 这里 $\left|\mu\right|$ 是 $\mu$ 的全变差测度.

## 例 2.5.2 (自反空间的对偶空间自反)

当 $X$ 是自反空间时, $X^*$ 也是自反的; 事实上这时 $\left(X^*\right)^{**}=X^{***}=\left(X^{**}\right)^*=X^*$.

## 定理 2.5.3 (典则映射的保范性)

设 $X$ 是赋范线性空间, 映射 $J:x\mapsto{x}^{**}$ 是从 $X$ 到 $X^{**}$ 的保范的线性算子, 即 (i) $\left(\alpha{x}+\beta{y}\right)^{**}=\alpha{x}^{**}+\beta{y}^{**}$; (ii) $\left\|x^{**}\right\|=\left\|x\right\|$.

## 定义 3.1.1 (疏朗集)

设 $A$ 是度量空间 $X$ 的一个子集, 如果 $A$ 的闭包 $\overline{A}$ 不含有 $X$ 的非空开集, 即 $\overline{A}$ 没有内点, 则称 $A$ 在 $X$ 中是疏朗的.

## 定理 3.1.1 (贝尔纲定理)

完备度量空间是第二纲的.

## 注 3.1.1 (疏朗集的等价刻画)

从定义可以看出, $A$ 是疏朗集当且仅当 $\overline{A}$ 是疏朗的. 由此易得 $A$ 是疏朗集也等价于 $\overline{A}$ 的余集 $\overline{A}^c=X\setminus\overline{A}$ 是稠密的.
