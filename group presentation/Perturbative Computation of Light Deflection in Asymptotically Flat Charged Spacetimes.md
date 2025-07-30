Let's start from a general static spherically symmetric metric of the form
$$

ds^2 = A(r)\, dt^2 - B(r)\, dr^2 - C(r)\, (d\theta^2 + \sin^2\theta\, d\phi^2)

$$
Restricting to the equatorial plane $\theta = \pi/2$, the metric becomes
$$

ds^2 = A(r)\, dt^2 - B(r)\, dr^2 - C(r)\, d\phi^2

$$
We consider the null geodesics in an asymptotically flat, spherically symmetric spacetime with metric function expanded as
$$
A(r) = 1 - \frac{2M}{r} + \frac{Q}{r^2} + \mathcal{O}\left(\frac{1}{r^3}\right)
$$

---
Letting $x = \frac{1}{r}$, we define
$$
a(x) = A\left(\frac{1}{x}\right) \approx 1 - 2Mx + Qx^2, \quad
b(x) = \frac{1}{a(x)}, \quad
c(x) = x^2
$$

We set $e = \frac{1}{1 - v^2}$, and define $u = \frac{r_0}{r} \in (0,1)$, where $r_0$ is the distance of closest approach and $u_0 = 1/r_0$. The geodesic integral kernel is

$$
y(u_0, u) =
\sqrt{
\frac{
b(u_0 u)\left(e - \kappa a(u_0)\right)
}{
u_0^2 u^4 c(u_0 u)
\left[
e \left(
\frac{c(u_0 u) a(u_0)}{a(u_0 u) c(u_0)} - 1
\right)
+ \kappa a(u_0)\left(
1 - \frac{c(u_0 u)}{c(u_0)}
\right)
\right]
}
}
$$

We expand $y(u_0, u)$ as a power series in $u_0$:

$$
y(u_0, u) = \frac{1}{\sqrt{1 - u^2}} + \sum_{n=1}^{\infty} u_0^n f_n(u)
$$

Each $f_n(u)$ is integrated over $u \in [0,1]$ against the flat-space kernel, yielding the total deflection contribution $ys(u_0)$.

To express the result in terms of the observable impact parameter $b$ , we define

$$
b(u_0) = \sqrt{
\frac{(e - 1)a(u_0)}{c(u_0)(e - \kappa a(u_0))}
}
$$

and compute its inverse $u_0(b)$ via perturbative series inversion. Substituting into the bending angle series, we obtain

$$
\alpha(b) = \pi + \frac{A_1}{b} + \frac{A_2}{b^2} + \frac{A_3}{b^3} + \cdots
$$

where each coefficient $A_n$ depends on $M$, $Q$, and $v$. In the static observer limit $v \to 1$, the charge term appears first at order $b^{-2}$:

$$
\Delta\alpha_Q = -\frac{Q(2 + v^2)}{4 M^2 v^2} \cdot \frac{1}{b^2} + \cdots
$$

This completes the symbolic derivation of the deflection angle to arbitrary order, allowing further analysis of relativistic and electromagnetic corrections.

Here is the code, you can reproduce the results with Mathematica.
```mathematica
$Assumptions = Q > 0 && B > 0 && u > 0 && u < 1;
order = 3;
a[x_] = Assuming[x > 0, 
   Normal[Series[1 - 2 M x + Q x^2, {x, 0, order}]]];
b[x_] = Assuming[x > 0, Normal[Series[1/a[x], {x, 0, order}]]];
c[x_] = Assuming[x > 0, Normal[Series[x^-2, {x, 0, order}]]];
(*将度规在无穷远处做泰勒展开*)
e = 1/(1 - v^2);
\[Kappa] = 1;
y[u0_, u_] = 
 Simplify[
  Series[Sqrt[(b[u0 u] (e - \[Kappa] a[u0]))/(
   u^4 u0^2 c[
     u0 u] (e ((c[u0 u] a[u0])/(a[u0 u] c[u0]) - 1) + \[Kappa] a[
        u0] (1 - c[u0 u]/c[u0])))], {u0, 0, order}]](*将被积函数在无穷远处做泰勒展开*)

Out[8]= 1/Sqrt[1-u^2]+(M u0 (u^2 v^2+u v^2+1))/((u+1) Sqrt[1-u^2] v^2)+(u0^2 (M^2 (3 u^4 v^4+6 u^3 v^4+3 u^2 (v^2+2) v^2+2 u (5 v^2-2)+4 v^2-1)-Q (u+1)^2 v^2 (u^2 v^2+1)))/(2 (u+1)^2 Sqrt[1-u^2] v^4)+(u0^3 (M^3 (5 u^6 v^6+15 u^5 v^6+15 u^4 (v^6+v^4)+u^3 (5 v^4+42 v^2-12) v^2+u^2 (47 v^4-25 v^2+8)+u (28 v^4-17 v^2+4)+8 v^4-4 v^2+1)-M Q (u+1)^2 v^2 (3 u^4 v^4+3 u^3 v^4+6 u^2 v^2+u (5 v^2-2)+4 v^2-1)))/(2 (u+1)^3 Sqrt[1-u^2] v^6)+O(u0^4)

In[10]:= For[n = 1, n < 2 order + 2, n++, 
 coefficient1[n] = FullSimplify[\!\(
\*SubsuperscriptBox[\(\[Integral]\), \(0\), \(1\)]\(
\*FractionBox[
SuperscriptBox[\((u + 1)\), \(n - order - 1\)], 
SqrtBox[\(1 - 
\*SuperscriptBox[\(u\), \(2\)]\)]] \[DifferentialD]u\)\)]]
ys[u0_] = 0;
For[n = 1, n < 2 order + 2, n++, 
 ys[u0_] = 
  ys[u0] + 
   Coefficient[y[u0, x - 1] x^(order + 1) Sqrt[1 - (-1 + x)^2], x^
     n] coefficient1[n]]
Series[-2 (ys[1/(
     Subscript[x, 0] M)] - (ys[1/(Subscript[x, 0] M)] /. v -> 1)), {v,
   1, 2}, {Subscript[x, 0], 0, 1}]

Out[13]= SeriesData[v, 1, {
SeriesData[
Subscript[x, 0], 0, {
   M^(-2) (102 M^2 - 27 M^2 Pi - 26 Q + 5 Pi Q), 
    M^(-2) ((-12) M^2 + 6 M^2 Pi - Pi Q), 4}, -3, 2, 1], 
SeriesData[
Subscript[x, 0], 0, {
   Rational[1, 2] M^(-2) ((-434) M^2 + 129 M^2 Pi + 86 Q - 23 Pi Q), 
    Rational[1, 2] M^(-2) (52 M^2 - 18 M^2 Pi + 3 Pi Q), -6}, -3, 2, 
   1]}, 1, 3, 1]

In[55]:= 
imp[u0_] = 
 Normal[Assuming[u0 > 0 && v > 0, 
   Series[Sqrt[(e - 1) a[u0]/(c[u0] (e - \[Kappa] a[u0]))], {u0, 0, 
     order}]]]
(*计算impact parameter*)

Out[55]= u0 - (M u0^2)/v^2 + (
 u0^3 (3 M^2 - 4 M^2 v^2 + M^2 q^2 v^2))/(2 v^4)

In[51]:= n = 2;
inimp[x_] = x/imp'[0];
While[
  n <= order,
  coefficient = D[imp[inimp[x]], {x, n}] /. x -> 0;
  inimp[x_] = inimp[x] + Simplify[-coefficient x^n/(n! imp'[0])];
  n++
  ];
(*计算impact parameter的反函数*)

In[54]:= Series[
 Expand[Coefficient[2 ys[inimp[s/M]]/2, s^17]] /. v -> v/k, {k, 0, 34}]

Out[54]= 0

In[33]:= 
fa[s_] = Normal[Series[2 ys[inimp[s/M]], {s, 0, order}] // Simplify]
(*结果*)

Out[33]= \[Pi] + 
 s (2 + 2/v^2) + (\[Pi] s^2 (-Q (2 + v^2) + 3 M^2 (4 + v^2)))/(
 4 M^2 v^2) + (
 2 s^3 (-1 + 15 v^2 + 45 v^4 + 5 v^6 - (3 Q v^2 (1 + 6 v^2 + v^4))/
    M^2))/(3 v^6)

In[43]:= 
TeXForm[Series[
   Coefficient[
     2 (ys[1/Subscript[x, 0]/M] - (ys[1/Subscript[x, 0]/M] /. 
           q -> 0)) /. v -> 1, 1/Subscript[x, 0]^15] // Simplify, {q, 
    0, order}]];
TeXForm[StandardForm[
   Coefficient[fa[u0] - (fa[u0] /. q -> 0), u0^15] /. v -> 1 // 
    Simplify]];
Series[Coefficient[fa[u0] - (fa[u0] /. q -> 0), u0^2], {q, 0, 
  order}, {v, Infinity, order}]
(-(5651752743/64) + (29504812882545 \[Pi])/1048576) // Simplify

Out[45]= 0

Out[46]= (819 (-113062658048 + 36025412555 \[Pi]))/1048576

In[47]:= Q = M^2 q^2;

In[49]:= Series[-fa[s] + (fa[s] /. v -> 1), {v, 1, 1}, {s, 0, order}]

Out[49]= SeriesData[v, 1, {
SeriesData[
  s, 0, {4, (-Pi) (-6 + q^2), (-32) (-3 + q^2)}, 1, 4, 1]}, 1, 2, 1]

```

---
