---
format:
  pdf:
    documentclass: extarticle
    classoption: twocolumn
    latex-engine: xelatex
    papersize: a4
    fontsize: 8pt
    geometry:
      - paper=a4paper
      - top=0.4cm
      - bottom=0.4cm
      - left=0.5cm
      - right=0.5cm
    header-includes:
      - \usepackage{ctex}
      - \usepackage{enumitem}
      - \setlist{nosep,leftmargin=1em}
      - \usepackage{titlesec}
      - \titleformat{\section}{\normalfont\small\bfseries}{}{0pt}{}
      - \titlespacing*{\section}{0pt}{1pt}{1pt}
      - \setlength{\parindent}{0pt}
      - \setlength{\parskip}{0pt}
      - \renewcommand{\baselinestretch}{0.95}
      - \pagestyle{empty}
    toc: false
    title-block-style: none
    keep-md: true
---

**1.3.2 合同变换**: $T(\boldsymbol x)=\boldsymbol xT+P,\ T\in O(n),\ P\in\mathbb E^n$; $\det T=1$ 刚体运动, $\det T=-1$ 反向刚体运动.

**2.2.1 弧长与弧长参数**: $s(t)=\int_c^d|\boldsymbol r'(t)|\,\mathrm dt$; $|\frac{\mathrm d\boldsymbol r}{\mathrm ds}|\equiv1$ 的 $s$ 即弧长参数; $|\frac{\mathrm d\boldsymbol r}{\mathrm dt}|\equiv1 \Leftrightarrow t$ 是弧长参数.

**2.2.2 曲率为常数**: $\kappa=0$ 直线; $\kappa=\alpha\ne0$ 半径为 $1/|\alpha|$ 的圆.

**2.3.1 空间标架**: $\kappa=|\dot{\boldsymbol t}|=|\boldsymbol r''|$, $\boldsymbol n=\dot{\boldsymbol t}/\kappa$, $\boldsymbol b=\boldsymbol t\wedge\boldsymbol n$, $\tau=\langle\dot{\boldsymbol n},\boldsymbol b\rangle$; $\boldsymbol t=\boldsymbol r'$.

**2.3.2 弗雷内公式**: $\dot{\boldsymbol t}=\kappa\boldsymbol n$, $\dot{\boldsymbol n}=-\kappa\boldsymbol t+\tau\boldsymbol b$, $\dot{\boldsymbol b}=-\tau\boldsymbol n$. (亦编号 2.3.2)

**2.3.3 二阶展开**: $\boldsymbol r(s)=\boldsymbol r(0)+s\dot{\boldsymbol r}(0)+\frac{s^2}2\ddot{\boldsymbol r}(0)+O(s^3)$, $\ddot{\boldsymbol r}(0)=\kappa(0)\boldsymbol n(0)$.

**2.4.5 一般参数曲率/挠率**: $\kappa=\frac{|\boldsymbol r'\wedge\boldsymbol r''|}{|\boldsymbol r'|^3}$, $\tau=\frac{(\boldsymbol r',\boldsymbol r'',\boldsymbol r''')}{|\boldsymbol r'\wedge\boldsymbol r''|^2}$.

**2.4.12 切线像**: $\kappa^{*}=\sqrt{1+(\tau/\kappa)^2}$, $\tau^{*}=\frac1\kappa\frac{(\tau/\kappa)'}{1+(\tau/\kappa)^2}$.

**2.4.15 球面曲线**: $(\frac1\kappa)^2+[\frac1\tau\frac{\mathrm d}{\mathrm ds}\frac1\kappa]^2\equiv$ 常数 $\Rightarrow$ 球面曲线或 $\kappa$ 常数.

**3.1.1 曲面/单位法向**: $\boldsymbol r_u\wedge\boldsymbol r_v\ne0$, $\boldsymbol n=\frac{\boldsymbol r_u\wedge\boldsymbol r_v}{|\boldsymbol r_u\wedge\boldsymbol r_v|}\perp\boldsymbol r_u,\boldsymbol r_v$.

**3.1.5 等值面**: $\nabla F\ne0 \Rightarrow S_c=\{F=c\}$ 曲面; 切平面 $F_x(x-x_0)+F_y(y-y_0)+F_z(z-z_0)=0$.

**3.2.1 第一基本形式**: $I=\langle\mathrm d\boldsymbol r,\mathrm d\boldsymbol r\rangle=g_{\alpha\beta}\,\mathrm du^\alpha\,\mathrm du^\beta$, $g_{\alpha\beta}=\langle\boldsymbol r_\alpha,\boldsymbol r_\beta\rangle$ (亦记 $E,F,G$); 与参数选取无关.

**3.3.1 第二基本形式**: $II=-\langle\mathrm d\boldsymbol r,\mathrm d\boldsymbol n\rangle=b_{\alpha\beta}\,\mathrm du^\alpha\,\mathrm du^\beta$, $b_{\alpha\beta}=\langle\boldsymbol r_{\alpha\beta},\boldsymbol n\rangle$ (亦记 $L,M,N$).

**3.3.1 点分类**: $k_1k_2>0$ 椭圆点, $<0$ 双曲点, $=0$ 抛物点, $k_1=k_2=0$ 平点.

**3.3.2 渐近方向**: 法曲率 $=0$ 的方向; 双曲点两个, 抛物点唯一.

**3.4.1 魏因加滕**: $W=-\mathrm d\boldsymbol n:\ T_PS\to T_PS$, $\lambda\boldsymbol r_u+\mu\boldsymbol r_v\mapsto-(\lambda\boldsymbol n_u+\mu\boldsymbol n_v)$; 自共轭 $\langle W\boldsymbol v,\boldsymbol w\rangle=\langle\boldsymbol v,W\boldsymbol w\rangle$.

**3.4.1 图形式基本量**: $g_{\alpha\beta}=\delta_{\alpha\beta}+f_\alpha f_\beta$, $b_{\alpha\beta}=\frac{f_{\alpha\beta}}{\sqrt{1+f_1^2+f_2^2}}$.

**3.4.2 法曲率**: $k_n(\boldsymbol w)=\frac{II(\boldsymbol w,\boldsymbol w)}{I(\boldsymbol w,\boldsymbol w)}=\frac{b_{\alpha\beta}\,\mathrm du^\alpha\,\mathrm du^\beta}{g_{\alpha\beta}\,\mathrm du^\alpha\,\mathrm du^\beta}$; 弧长曲线 $k_n=\langle\ddot{\boldsymbol r},\boldsymbol n\rangle$; 只依赖切方向.

**3.5.1 主曲率/主方向**: $W$ 特征值 $k_1\le k_2$, 主方向 $k_1\ne k_2$ 时正交; $H=\frac{k_1+k_2}2$, $K=k_1k_2$.

**3.5.1 面积微元**: $\mathrm dA=\sqrt{g_{11}g_{22}-g_{12}^2}\,\mathrm du\,\mathrm dv$.

**3.5.1 曲率线网参数**: 非脐点存在使 $I,II$ 对角; 参数曲线是曲率线 $\Leftrightarrow g_{12}=b_{12}=0$ (习题 3.6.29).

**3.5.2 主方向坐标**: $\boldsymbol r_u(P)=\boldsymbol e_1,\ \boldsymbol r_v(P)=\boldsymbol e_2$; 则 $L(P)=k_1,\ M(P)=0,\ N(P)=k_2$.

**3.5.2 欧拉公式**: $k_n(\boldsymbol v)=k_1\cos^2\theta+k_2\sin^2\theta$; 推论 $k_1\le k_n(\boldsymbol v)\le k_2$.

**3.5.4 特征方程**: $k$ 主曲率 $\Leftrightarrow \det(b_{\alpha\beta}-k g_{\alpha\beta})=0$ $\Leftrightarrow k^2-2Hk+K=0$.

**3.5.4/3.5.6 平均/高斯曲率**: $H=\frac{k_1+k_2}2$, $K=k_1k_2$; $\boldsymbol n_u\wedge\boldsymbol n_v=K\,\boldsymbol r_u\wedge\boldsymbol r_v$; $K=\det W$, $2H=\operatorname{tr}W$, $W=g^{-1}b$.

**3.5.5 脐点**: $k_1=k_2$; $k\ne0$ 圆点, $k=0$ 平点.

**3.5.5 高斯映射面积**: $\mathrm d\sigma=K\,\mathrm dA$, $\lim_{D\to P}\frac{\mathrm{Area}(g(D))}{\mathrm{Area}(D)}=K(P)$.

**3.5.8 同时对角化**: $Q^{\top}gQ=I_2$, $Q^{\top}bQ=\mathrm{diag}(k_1,k_2)$, 即一点可取 $g_{\alpha\beta}=\delta_{\alpha\beta}$.

**3.5.9 二阶近似**: $\boldsymbol r-\boldsymbol r(P)=\Delta u\,\boldsymbol e_1+\Delta v\,\boldsymbol e_2+\frac12(k_1\Delta u^2+k_2\Delta v^2)\boldsymbol n+o$; 椭圆点近似椭圆抛物面, 双曲点双曲抛物面, 抛物点抛物柱面.

**3.6.1 旋转面**: $\boldsymbol r(u,v)=(f\cos v,f\sin v,g)$, $f>0$; 图形 $\boldsymbol r(t,\theta)=(t\cos\theta,t\sin\theta,\varphi(t))$; 曲率线=每点切向为主方向.

**3.6.2 旋转面基本量**: $g_{11}=f'^2+g'^2$, $g_{12}=0$, $g_{22}=f^2$, $b_{11}=\frac{f'g''-f''g'}{\sqrt{f'^2+g'^2}}$, $b_{12}=0$, $b_{22}=\frac{fg'}{\sqrt{f'^2+g'^2}}$; $k_1=\frac{b_{11}}{g_{11}}$, $k_2=\frac{b_{22}}{g_{22}}$. 图形: $I=(1+\varphi'^2)\mathrm dt^2+t^2\mathrm d\theta^2$, $II=\frac{\varphi''}{\sqrt{1+\varphi'^2}}\mathrm dt^2+\frac{t\varphi'}{\sqrt{1+\varphi'^2}}\mathrm d\theta^2$.

**3.6.3 常高斯旋转面**: 弧长参数下 $K=-\frac{f''}{f}$; $K>0$ 球面, $K=0$ 圆柱/平面/圆锥面, $K<0$ 伪球面; 图形 $K\equiv k \Leftrightarrow \frac1{1+\varphi'^2}=c-kt^2$.

**3.6.4 直纹面**: $\boldsymbol r(u,v)=\boldsymbol a(u)+v\boldsymbol\ell(u)$, $|\boldsymbol\ell|=1$.

**3.6.4 常平均旋转面**: $H\equiv0 \Rightarrow$ 悬链面 $\varphi=\mathrm{arcosh}\,t$.

**3.6.5 柱面/锥面/切线面**: $\boldsymbol\ell$ 常向量 柱面; $\boldsymbol a$ 常向量 锥面; $\boldsymbol\ell=\boldsymbol a'/|\boldsymbol a'|$ 切线面.

**3.6.6/3.6.7 可展曲面**: $K=0$ 的直纹面 $\Leftrightarrow b_{12}\equiv0 \Leftrightarrow$ 沿直母线法向量不变 $\Leftrightarrow (\boldsymbol a',\boldsymbol\ell,\boldsymbol\ell')\equiv0$; 可展曲面恰为柱面, 锥面, 切线面 (3.6.8).

**3.6.9/3.6.10 全脐曲面**: $k_1=k_2$ 处处 $\Leftrightarrow$ 平面或球面的一部分.

**3.6.12 正交参数系**: $g_{12}=0$; 每点邻域存在.

**4.2.1 克里斯托费尔符号**: $\Gamma^\gamma{}_{\alpha\beta}=\frac12 g^{\gamma\varepsilon}(\partial_\alpha g_{\beta\varepsilon}+\partial_\beta g_{\alpha\varepsilon}-\partial_\varepsilon g_{\alpha\beta})$, $\Gamma^\gamma{}_{\alpha\beta}=\Gamma^\gamma{}_{\beta\alpha}$.

**4.2.1 自然标架运动方程**: $\partial_\beta\boldsymbol r_\alpha=\Gamma^\varepsilon{}_{\alpha\beta}\boldsymbol r_\varepsilon+b_{\alpha\beta}\boldsymbol n$, $\partial_\beta\boldsymbol n=-b_{\alpha\beta}g^{\alpha\varepsilon}\boldsymbol r_\varepsilon$.

**4.3.1 高斯方程**: $\partial_\gamma\Gamma^\delta{}_{\alpha\beta}-\partial_\beta\Gamma^\delta{}_{\alpha\gamma}+\Gamma^\varepsilon{}_{\alpha\beta}\Gamma^\delta{}_{\varepsilon\gamma}-\Gamma^\varepsilon{}_{\alpha\gamma}\Gamma^\delta{}_{\varepsilon\beta}-b_{\alpha\beta}b^\delta{}_\gamma+b_{\alpha\gamma}b^\delta{}_\beta=0$; **科达齐方程**: $\partial_\gamma b_{\alpha\beta}-\partial_\beta b_{\alpha\gamma}+\Gamma^\varepsilon{}_{\alpha\beta}b_{\varepsilon\gamma}-\Gamma^\varepsilon{}_{\alpha\gamma}b_{\varepsilon\beta}=0$ (合称高斯-科达齐方程组).

**4.3.2 曲面基本定理**: $g_{\alpha\beta}$ 正定, $b_{\alpha\beta}$ 对称满足高斯-科达齐方程组 $\Leftrightarrow$ 存在曲面以 $I,II$ 为基本形式, 刚体运动意义下唯一.

**4.3.3 高斯绝妙定理**: $K=\frac{\det(b_{\alpha\beta})}{\det(g_{\alpha\beta})}$ 只依赖 $I$ (内蕴); 正交网 $K=-\frac1{2\sqrt{g_{11}g_{22}}}\big(\partial_1\frac{\partial_1 g_{22}}{\sqrt{g_{11}g_{22}}}+\partial_2\frac{\partial_2 g_{11}}{\sqrt{g_{11}g_{22}}}\big)$.

**5.1.1 测地/法曲率**: $k_g$ 为 $\ddot{\boldsymbol r}$ 切向投影(带号), $k_n=b_{\alpha\beta}\dot u^\alpha\dot u^\beta$; $k_g$ 只依赖 $I$ (内蕴).

**5.1.2 二阶分解**: $\ddot{\boldsymbol c}=(\ddot u^\alpha+\Gamma^\alpha{}_{\varepsilon\tau}\dot u^\varepsilon\dot u^\tau)\boldsymbol r_\alpha+b_{\varepsilon\tau}\dot u^\varepsilon\dot u^\tau\,\boldsymbol n$; $\kappa=|\ddot{\boldsymbol c}|=\sqrt{k_g^2+k_n^2}$, $k_g=\langle\dot{\boldsymbol t},\boldsymbol n\times\boldsymbol t\rangle$.

**5.1.3/5.1.4 测地线**: $k_g=0$; $\ddot u^\alpha+\Gamma^\alpha{}_{\varepsilon\tau}(u)\dot u^\varepsilon\dot u^\tau=0$.

**5.1.5 刘维尔公式** (正交网 $I=g_{11}\mathrm du^2+g_{22}\mathrm dv^2$): $k_g=\theta'(s)-\frac{\partial_2 g_{11}}{2g_{11}\sqrt{g_{22}}}\cos\theta+\frac{\partial_1 g_{22}}{2g_{22}\sqrt{g_{11}}}\sin\theta$; $\cos\theta=\dot u^1\sqrt{g_{11}}$, $\sin\theta=\dot u^2\sqrt{g_{22}}$; 测地线: $\theta'=\frac{\partial_2 g_{11}}{2g_{11}\sqrt{g_{22}}}\cos\theta-\frac{\partial_1 g_{22}}{2g_{22}\sqrt{g_{11}}}\sin\theta$.

**5.1.7 球面测地线**: 即大圆.

**5.5.1 高斯-博内公式**: $D$ 单连通, $\partial D$ 分段光滑, $\alpha_i$ 外角: $\int_{\partial D}k_g\,\mathrm ds+\int_D K\,\mathrm dA+\sum_i\alpha_i=2\pi$.

**6.1.1 旋转指数**: 平面简单闭曲线的旋转指数为 $\pm1$.

**6.1.2 曲率 $=$ 方向角导数**: $\kappa(s)=\frac{\mathrm d\theta}{\mathrm ds}$.

**6.1.3 等周不等式**: $L^2-4\pi A\ge0$, 等号当且仅当 $C$ 是圆.

**6.1.4 维尔丁格不等式**: $\int f=0 \Rightarrow \int (f')^2\ge\int f^2$, 等号 $\Leftrightarrow f=a\cos t+b\sin t$.

**6.2.1 凸曲线**: $\kappa>0$; 高斯映射一一对应 $\Leftrightarrow$ 方向角 $\theta$ 严格单调增.

**7.3.4 芬切尔定理**: $\int_{\boldsymbol r}\kappa\,\mathrm ds\ge2\pi$ (闭曲线).

**7.3.5 扭结曲线全曲率 (法里-米尔诺)**: 非平凡纽结 $\int_\gamma\kappa\,\mathrm ds>4\pi$.

**10.1.1 极小曲面**: $H=0$.

**10.1.1 螺旋面**: $f=\arctan\frac yx$, 唯一的直纹极小曲面.

**10.1.2 函数图几何量**: $\boldsymbol r=(x,y,f)$, $p=f_x,q=f_y,r=f_{xx},s=f_{xy},t=f_{yy}$, $W=\sqrt{1+p^2+q^2}$; $I=(1+p^2)\mathrm dx^2+2pq\,\mathrm dx\,\mathrm dy+(1+q^2)\mathrm dy^2$, $\boldsymbol e_3=\frac1W(-p,-q,1)$, $II=\frac{r\,\mathrm dx^2+2s\,\mathrm dx\,\mathrm dy+t\,\mathrm dy^2}{W}$, $H=\frac{(1+q^2)r-2pqs+(1+p^2)t}{2W^3}$.

**10.1.3 极小曲面方程**: $(1+f_y^2)f_{xx}-2f_xf_yf_{xy}+(1+f_x^2)f_{yy}=0$.

**10.1.3 谢尔克曲面**: $f=\ln\frac{\cos x}{\cos y}$.

