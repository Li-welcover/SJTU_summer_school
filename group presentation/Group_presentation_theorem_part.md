## [[Physical Origin of the Asymmetric Ring.pdf]] 
### definition of BH's shadow
The central hole surrounded by a bright ring arises because of **strong gravitational lensing**. The central flux depression is the so-called black hole “shadow”, and corresponds to lines of sight that terminate on the event horizon.

### photon ring angular radius
For an $a^{\star}=0$ *(which means the spin of the BH is 0)* black hole of mass M and distance D, the photon ring angular radius on the sky is:$$
\theta_{p}\equiv \frac{\sqrt{ 27 }GM}{c^{2}D}\tag{1}
$$
---
对于一个质量为 $M$ 的 Schwarzschild 黑洞（为什么不考虑自旋后面解释）度规：
$$ds^2 = -A(r)c^2 dt^2 + A(r)^{-1} dr^2 + r^2 (d\theta^2 + \sin^2\theta d\phi^2)$$
我们考虑在赤道面（$\theta = \frac{\pi}{2}$）传播的光线，因此度规可以简化为：
$$ds^2 = 0 = -\left(1 - \frac{2GM}{c^2 r} \right)c^2 dt^2 + \left(1 - \frac{2GM}{c^2 r} \right)^{-1} dr^2 + r^2 d\phi^2$$
考虑从无穷远发出的光线，其运动方程可以写成**有效势形式**：
$$\left(\frac{dr}{d\lambda}\right)^2 + V_{\text{eff}}(r) = \left( \frac{E}{c} \right)^2\tag{2}$$
有效势：$$V_{\text{eff}}(r) = \left(1 - \frac{2GM}{c^2 r}\right) \frac{L^2}{r^2}.$$
令光子在某一轨道上绕黑洞做圆周运动，需满足：$\frac{dV_{\text{eff}}}{dr} = 0$（势能极值点）；$V_{\text{eff}} = \left( \frac{E}{c} \right)^2$
计算 $V_{\text{eff}}$ 的极值位置：
$$\frac{d}{dr} \left[ \left(1 - \frac{2GM}{c^2 r}\right) \frac{L^2}{r^2} \right] = 0$$
解得：
$$r = \frac{3GM}{c^2}$$
因此，光子可以在 $r = 3GM/c^2$ 处做不稳定圆轨道，这就是所谓的“光子环”所在的物理位置。
在黑洞观测中，光线的路径可由其入射参数（impact parameter）描述：
$$b \equiv \frac{L}{E/c}.$$对于光子环半径 $r = 3GM/c^2$，我们将其入射参数记作 $b_p$，可以从前述有效势中求得：
$$\left( \frac{E}{c} \right)^2 = \left(1 - \frac{2GM}{c^2 r} \right)\frac{L^2}{r^2} \Rightarrow \left( \frac{E}{c} \right)^2 = \left(1 - \frac{2GM}{c^2 r} \right)\frac{(bE/c)^2}{r^2}
$$
消去 $E$，代入 $r = 3GM/c^2$, 解得：
$$b_p = \sqrt{27} \frac{GM}{c^2}.
$$
远处静止观测者距离黑洞 $D$，从黑洞射向他的光线以角度 $\theta_p$ 到达。他所看到的黑洞视角下的光线轨迹，其角半径满足：
$$\theta_p = \frac{b_p}{D} = \frac{\sqrt{27} GM}{c^2 D}
$$
  
> where we have scaled to the most likely mass from Gebhardt et al.(2011) and a distance of 16.9 Mpc. The photon ring angular radius for other inclinations and values of a* differs by at most 13% from Equation (1), and most of this variation occurs at $1-|a_{\star}|\ll 1$. Evidently the angular radius of the observed photon ring is approximately ~20$\mu$as  which is close to the prediction of the black hole model given in Equation (1).
（这段话意思就是只有自旋超级大的时候才有百分之十三的差异，中低自旋影响就更小了。

这篇文章介绍了克尔光子球的半解析计算[[Photon rings in Kerr space .pdf]]

---
关于（2）式——有效势形式的运动方程，可以用测地线方程，也可以用哈密顿方法导出。后者更适合于考虑等离子体环绕的情形（目前我在算的等离子体中的引力透镜偏折角就是用的这种方法）。
光子的哈密顿量为：
$$\mathcal{H} = \frac{1}{2} g^{\mu\nu} p_\mu p_\nu = \frac{1}{2} \left[ -\frac{p_t^2}{A(r)c^2} + A(r) p_r^2 + \frac{p_\phi^2}{r^2} \right] = 0$$
能量守恒，轨道角动量守恒（$p_t = -E$, $p_\phi = L$）：
$$A(r) p_r^2 + \frac{L^2}{r^2} = \frac{E^2}{c^2 A(r)} \Rightarrow p_r^2 = \frac{1}{A(r)^2} \left[ \frac{E^2}{c^2} - A(r)\frac{L^2}{r^2} \right]$$
代换 $p_r = \frac{dr}{d\lambda}$，即可得到有效势形式运动方程：
$$
\left( \frac{dr}{d\lambda} \right)^2 + V_{\text{eff}}(r) = \left( \frac{E}{c} \right)^2
$$
如果考虑黑洞周围的等离子体分布，则应该用光子修正哈密顿量[optical metric](https://en.wikipedia.org/wiki/Optical_metric)求解，当然也可以直接拿来主义，参考这篇笔记及其参考文献[[等离子体光线偏折复算]]
$$
H = \frac{1}{2} \left( g^{\mu\nu} p_\mu p_\nu + (n^2 - 1)(p_0 V_t)^2 \right)
$$
即Gordon metric下的Hamilton量。
$n$ 是等离子体折射率：
$$
n=\sqrt{ 1-\epsilon }=\sqrt{ 1- \frac{\omega_{p}^{2}}{\omega^{2}} }
$$
$\omega_{p}$ 是等离子体的振荡频率 见[[郭书.pdf]]（4.9.16式）$\omega_{p}=\frac{4\pi e^{2}N(r)}{m}$，$N(r)$ 为等离子体密度函数。$\omega$ 是有限远处，时谐电磁波的圆频率
红移关系建立了有限远处和无限远处的电磁波频率的关系：
$$
\omega(r)=\frac{\omega_{\infty}}{\sqrt{ g_{00} }}=\frac{\omega_{\infty}}{\sqrt{ A(r) }}
$$

再用哈密顿正则方程以及能量角动量双守恒，可以得到 $\frac{d\phi}{dr}$ 关于 $r$ 的显式表达式。
下面附上mma的计算代码，可以给出任意等离子体分布函数下，光子的运动方程。
```mathematica
ClearAll["Global`*"]
coord = {t, r, \[Theta], \[Phi]};
gdown = {{Am[r], 0, 0, 0}, {0, -Bm[r], 0, 0}, {0, 0, -Cm[r], 0}, {0, 
     0, 0, -Cm[r]}} /. {\[Theta] -> \[Pi]/2};
gup = Simplify[Inverse[gdown]];
gupMatrix = Table[gup[[i, j]], {i, 1, 4}, {j, 1, 4}];
pdown = {pt, pr, 0, pphi};
pup = Table[\!\(
\*UnderoverscriptBox[\(\[Sum]\), \(j = 1\), \(4\)]\(gupMatrix[[i, 
      j]]\ pdown[[j]]\)\), {i, 1, 4}];
Vt = 1/Sqrt[Am[r]];
n[r_, \[Omega]_] := Sqrt[1 - \[Omega]e[r]^2/\[Omega]^2];
RedShift = {\[Omega] -> \[Omega]\[Infinity]/Sqrt[Am[r]]};
H = Simplify[1/2 (\!\(
\*UnderoverscriptBox[\(\[Sum]\), \(i = 1\), \(4\)]\(
\*UnderoverscriptBox[\(\[Sum]\), \(j = 1\), \(4\)]gupMatrix[[i, 
          j]]\ pdown[[i]]\ pdown[[j]]\)\) + (n[r, \[Omega]]^2 - 
         1) (pdown[[1]] Vt)^2)];
dxtd\[Lambda] = \!\(
\*SubscriptBox[\(\[PartialD]\), \(pt\)]H\);
dxrd\[Lambda] = \!\(
\*SubscriptBox[\(\[PartialD]\), \(pr\)]H\);
dx\[Phi]d\[Lambda] = \!\(
\*SubscriptBox[\(\[PartialD]\), \(pphi\)]H\);
ptConst = -ħ \[Omega]\[Infinity];
pphiConst = ħ \[Omega]\[Infinity] b;
HSimplified = 
  Simplify[
   H /. {pt -> ptConst, 
      pphi -> pphiConst, \[Omega]e[
        r]^2 -> \[Omega]\[Infinity]^2 \[Epsilon][r]^2} /. RedShift];
Print["Hamiltonian H = ", HSimplified];
prSol = Solve[HSimplified == 0, pr, Reals][[2]];
d\[Phi]d\[Lambda] = 
  dx\[Phi]d\[Lambda] /. {pt -> ptConst, pphi -> pphiConst};
drd\[Lambda] = 
  dxrd\[Lambda] /. {pt -> ptConst, pphi -> pphiConst} /. prSol;
Assumption1 = {\[Omega]\[Infinity] \[Element] 
    Reals, \[Omega]\[Infinity] > 0, 0 < Am[r] < 1, Bm[r] > 1, 
   r0 > 0};
Simplify[d\[Phi]d\[Lambda]/drd\[Lambda], 
  Assumptions -> {ħ \[Element] Reals, r > 0, \[Omega] > 0, ħ > 0}];
Refine[%, 
  Am[r] \[Element] Reals && \[Omega]\[Infinity] > 0 && Am[r] > 0 && 
   Cm[r] > 0 && Bm[r] > 0];
d\[Phi]dr = 
  Refine[%, 
   Bm[r] > 0 && {-\[Epsilon]^2 + 1/Am[r] - b^2/Cm[r]} \[Element] 
     Reals];
Print["d\[Phi]/dr = ", d\[Phi]dr];
```