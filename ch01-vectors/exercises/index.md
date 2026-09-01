<!-- MAGI -->
# 練習問題 - 第1章 ベクトルと空間図形

> 対応: [`../docs/index.md`](../docs/index.md)

## 問1

$\boldsymbol{a}=(1,-2,2)$、$\boldsymbol{b}=(3,1,-1)$ とする。$3\boldsymbol{a}-2\boldsymbol{b}$ と $|\boldsymbol{a}|$ を求めてください。

<details><summary>解答</summary>

**答: $3\boldsymbol{a}-2\boldsymbol{b}=(-3,-8,8)$、$|\boldsymbol{a}|=3$**

$3\boldsymbol{a}=(3,-6,6)$、$2\boldsymbol{b}=(6,2,-2)$ なので差は $(-3,-8,8)$ です。また $|\boldsymbol{a}|=\sqrt{1+4+4}=3$ です。

</details>

## 問2

$\boldsymbol{a}=(1,1,0)$ と $\boldsymbol{b}=(1,0,1)$ の内積となす角を求めてください。

<details><summary>解答</summary>

**答: 内積は $1$、なす角は $60^\circ$**

$\boldsymbol{a}\cdot\boldsymbol{b}=1$、$|\boldsymbol{a}|=|\boldsymbol{b}|=\sqrt2$ なので $\cos\theta=1/2$ です。

</details>

## 問3

$\boldsymbol{a}=(2,-1,3)$ と $\boldsymbol{b}=(k,2,-6)$ が平行になる実数 $k$ は存在しますか。また、$\boldsymbol{a}$ と $\boldsymbol{c}=(1,k,1)$ が垂直になる $k$ を求めてください。

<details><summary>解答</summary>

**答: 平行になるのは $k=-4$、垂直になるのは $k=5$**

平行条件は $\boldsymbol{b}=-2\boldsymbol{a}$ なので $k=-4$ です。垂直条件は $\boldsymbol{a}\cdot\boldsymbol{c}=2-k+3=0$ なので $k=5$ です。

</details>

## 問4

点 $P(2,-1,0)$ を通り、ベクトル $(1,3,-2)$ に平行な直線を媒介変数表示してください。また、点 $Q(4,5,-4)$ がこの直線上にあるか判定してください。

<details><summary>解答</summary>

**答: $(x,y,z)=(2,-1,0)+t(1,3,-2)$、$Q$ は直線上にある**

$Q-P=(2,6,-4)=2(1,3,-2)$ なので $t=2$ とすれば $Q$ が得られます。

</details>

## 問5

3点 $A(1,0,0)$、$B(0,1,0)$、$C(0,0,1)$ を通る平面の方程式を求めてください。

<details><summary>解答</summary>

**答: $x+y+z=1$**

$\overrightarrow{AB}=(-1,1,0)$ と $\overrightarrow{AC}=(-1,0,1)$ の両方に垂直な法線ベクトルとして $(1,1,1)$ を選べます。点 $A$ を代入して $x+y+z=1$ です。

</details>

## 問6

中心が $C(2,-1,3)$ で、点 $P(4,1,4)$ を通る球の方程式を求めてください。

<details><summary>解答</summary>

**答: $(x-2)^2+(y+1)^2+(z-3)^2=9$**

$r^2=|\overrightarrow{CP}|^2=2^2+2^2+1^2=9$ です。

</details>
<!-- /MAGI -->
