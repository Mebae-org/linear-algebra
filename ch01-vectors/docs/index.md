<!-- MAGI -->
# 第1章 ベクトルと空間図形

> **注記:** このファイルは AI により保守されます。

## 1.1 ベクトルと成分表示

ベクトルは、大きさと向きをもつ量です。平面ベクトルを $\boldsymbol{a}=(a_1,a_2)$、空間ベクトルを $\boldsymbol{a}=(a_1,a_2,a_3)$ のように成分で表します。始点 $A(x_1,y_1,z_1)$、終点 $B(x_2,y_2,z_2)$ のベクトルは

$$
\overrightarrow{AB}=(x_2-x_1,\ y_2-y_1,\ z_2-z_1)
$$

です。始点を原点に移しても成分が変わらないため、ベクトルを成分で計算できます。大きさが0のベクトルを零ベクトル $\boldsymbol{0}$ といいます。

### 和、差、実数倍

同じ次元のベクトルは成分ごとに計算します。

$$
\begin{aligned}
\boldsymbol{a}+\boldsymbol{b}&=(a_1+b_1,\ldots,a_n+b_n),\\
\boldsymbol{a}-\boldsymbol{b}&=(a_1-b_1,\ldots,a_n-b_n),\\
k\boldsymbol{a}&=(ka_1,\ldots,ka_n).
\end{aligned}
$$

差 $\boldsymbol{a}-\boldsymbol{b}$ は $\boldsymbol{a}+(-\boldsymbol{b})$ です。実数倍では、$k<0$ のとき向きが反対になります。

> **例題 1.1** $\boldsymbol{a}=(2,-1,3)$、$\boldsymbol{b}=(-1,4,2)$ のとき、$2\boldsymbol{a}-\boldsymbol{b}$ を求めてください。
>
> <details><summary>解答</summary>
>
> $$2\boldsymbol{a}-\boldsymbol{b}=(4,-2,6)-(-1,4,2)=(5,-6,4).$$
> </details>

### 大きさと単位ベクトル

$\boldsymbol{a}=(a_1,a_2,a_3)$ の大きさは、三平方の定理から

$$
|\boldsymbol{a}|=\sqrt{a_1^2+a_2^2+a_3^2}
$$

です。$\boldsymbol{a}\ne\boldsymbol{0}$ と同じ向きで大きさが1の単位ベクトルは $\boldsymbol{a}/|\boldsymbol{a}|$ です。

> **例題 1.2** $\boldsymbol{a}=(2,-1,2)$ の大きさと、同じ向きの単位ベクトルを求めてください。
>
> <details><summary>解答</summary>
>
> $|\boldsymbol{a}|=\sqrt{4+1+4}=3$ なので、単位ベクトルは $(2/3,-1/3,2/3)$ です。
> </details>

## 1.2 内積

2つのベクトル $\boldsymbol{a},\boldsymbol{b}$ の内積は、成分を使って

$$
\boldsymbol{a}\cdot\boldsymbol{b}=a_1b_1+a_2b_2+a_3b_3
$$

と計算します。また、零ベクトルでない2ベクトルのなす角を $\theta$（$0\leq\theta\leq\pi$）とすると

$$
\boldsymbol{a}\cdot\boldsymbol{b}=|\boldsymbol{a}|\,|\boldsymbol{b}|\cos\theta,
\qquad
\cos\theta=\frac{\boldsymbol{a}\cdot\boldsymbol{b}}{|\boldsymbol{a}|\,|\boldsymbol{b}|}
$$

が成り立ちます。内積の結果はベクトルではなく実数です。

### 平行と垂直の判定

- 平行: $\boldsymbol{a}\ne\boldsymbol{0}$、$\boldsymbol{b}\ne\boldsymbol{0}$ に対し、$\boldsymbol{b}=k\boldsymbol{a}$ となる実数 $k$ がある。
- 垂直: $\boldsymbol{a}\cdot\boldsymbol{b}=0$。ただし、方向を論じるときは零ベクトルを除く。

> **例題 1.3** $\boldsymbol{a}=(1,2,-1)$ と $\boldsymbol{b}=(2,-1,0)$ は垂直ですか。
>
> <details><summary>解答</summary>
>
> $\boldsymbol{a}\cdot\boldsymbol{b}=1\cdot2+2\cdot(-1)+(-1)\cdot0=0$ なので垂直です。
> </details>

## 1.3 空間内の直線

点 $P_0(x_0,y_0,z_0)$ を通り、零ベクトルでない方向ベクトル $\boldsymbol{d}=(a,b,c)$ に平行な直線上の点を $P(x,y,z)$ とします。$\overrightarrow{P_0P}$ が $\boldsymbol{d}$ の実数倍になるため、直線のベクトル方程式は

$$
\begin{pmatrix}x\\y\\z\end{pmatrix}
=
\begin{pmatrix}x_0\\y_0\\z_0\end{pmatrix}
+t\begin{pmatrix}a\\b\\c\end{pmatrix}
\quad(t\in\mathbb{R})
$$

です。これは媒介変数表示 $x=x_0+at$、$y=y_0+bt$、$z=z_0+ct$ と同じです。$a,b,c$ がすべて0でない場合は

$$
\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}
$$

とも表せます。0の成分があるときは、この対称形で0除算をせず、たとえば $a=0$ なら $x=x_0$ と書きます。

> **例題 1.4** $A(1,0,-1)$ と $B(3,1,2)$ を通る直線を媒介変数表示してください。
>
> <details><summary>解答</summary>
>
> 方向ベクトルは $\overrightarrow{AB}=(2,1,3)$ なので、$(x,y,z)=(1,0,-1)+t(2,1,3)$ です。
> </details>

## 1.4 空間内の平面

点 $P_0(x_0,y_0,z_0)$ を通り、法線ベクトル $\boldsymbol{n}=(a,b,c)\ne\boldsymbol{0}$ に垂直な平面を考えます。平面上の点 $P(x,y,z)$ に対して $\overrightarrow{P_0P}$ と $\boldsymbol{n}$ は垂直なので、

$$
\boldsymbol{n}\cdot\overrightarrow{P_0P}=0
$$

です。したがって平面の方程式は

$$
a(x-x_0)+b(y-y_0)+c(z-z_0)=0
$$

または $ax+by+cz=d$ となります。平面 $a_1x+b_1y+c_1z=d_1$ と $a_2x+b_2y+c_2z=d_2$ の平行・垂直は、それぞれの法線ベクトルの平行・垂直で判定できます。

> **例題 1.5** 点 $(1,-1,2)$ を通り、直線 $(x,y,z)=(0,1,1)+t(2,-1,3)$ に垂直な平面の方程式を求めてください。
>
> <details><summary>解答</summary>
>
> 直線の方向ベクトル $(2,-1,3)$ を平面の法線ベクトルにできます。よって $2(x-1)-(y+1)+3(z-2)=0$、整理して $2x-y+3z=9$ です。
> </details>

## 1.5 空間内の球

中心 $C(a,b,c)$、半径 $r>0$ の球は、球面上の点 $P(x,y,z)$ が $|\overrightarrow{CP}|=r$ を満たすことから

$$
(x-a)^2+(y-b)^2+(z-c)^2=r^2
$$

と表されます。一般形から中心と半径を読むときは平方完成します。

> **例題 1.6** $x^2+y^2+z^2-2x+4y-6z+5=0$ の中心と半径を求めてください。
>
> <details><summary>解答</summary>
>
> 平方完成すると $(x-1)^2+(y+2)^2+(z-3)^2=9$ です。中心は $(1,-2,3)$、半径は $3$ です。
> </details>

## よくある誤り

- $\overrightarrow{AB}$ を「終点 $B$ から始点 $A$ を引く」$B-A$ ではなく、逆に計算する。
- 大きさ $|\boldsymbol{a}|$ で平方根を取り忘れる。
- 平行判定で成分ごとに異なる倍率を使う。
- 直線の方向ベクトルと平面の法線ベクトルを混同する。
- 球の方程式で右辺を $r$ とし、$r^2$ にしない。

## 章末チェック

- [ ] ベクトルを成分表示し、和・差・実数倍・大きさを計算できる
- [ ] 内積から角度を求め、平行・垂直を判定できる
- [ ] 点と方向ベクトルから直線の方程式を立てられる
- [ ] 点と法線ベクトルから平面の方程式を立てられる
- [ ] 球の標準形と一般形を相互に変換できる

さらに練習する場合は [`../exercises/`](../exercises/) に進みます。
<!-- /MAGI -->
