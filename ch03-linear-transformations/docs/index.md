<!-- MAGI -->
# 第3章 線形変換

> **注記:** このファイルは AI により保守されます。

## 3.1 線形変換と行列

写像 $T:\mathbb{R}^n\to\mathbb{R}^m$ が任意のベクトル $\boldsymbol{x},\boldsymbol{y}$ と実数 $c$ に対して

$$
T(\boldsymbol{x}+\boldsymbol{y})=T(\boldsymbol{x})+T(\boldsymbol{y}),\qquad
T(c\boldsymbol{x})=cT(\boldsymbol{x})
$$

を満たすとき、$T$ を線形変換といいます。この2条件は $T(a\boldsymbol{x}+b\boldsymbol{y})=aT(\boldsymbol{x})+bT(\boldsymbol{y})$ とまとめられます。必ず $T(\boldsymbol{0})=\boldsymbol{0}$ なので、原点を原点以外へ移す平行移動は線形変換ではありません。

行列 $A$ を用いた $T(\boldsymbol{x})=A\boldsymbol{x}$ は線形変換です。逆に、有限次元の線形変換は基底を決めれば行列で表せます。

> **例題 3.1** $T\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix}$ のもとで、点 $P(2,1)$ の像を求めてください。
>
> <details><summary>解答</summary>
>
> $$T\begin{pmatrix}2\\1\end{pmatrix}=\begin{pmatrix}2&-1\\1&3\end{pmatrix}\begin{pmatrix}2\\1\end{pmatrix}=\begin{pmatrix}3\\5\end{pmatrix}.$$
> 像は点 $(3,5)$ です。
> </details>

## 3.2 表現行列の求め方

標準基底 $\boldsymbol{e}_1=(1,0)^T$、$\boldsymbol{e}_2=(0,1)^T$ を使うと、任意の $\boldsymbol{x}=(x,y)^T$ は $x\boldsymbol{e}_1+y\boldsymbol{e}_2$ です。線形性から

$$
T(\boldsymbol{x})=xT(\boldsymbol{e}_1)+yT(\boldsymbol{e}_2)
$$

となるため、$T(\boldsymbol{e}_1)$ と $T(\boldsymbol{e}_2)$ を**列として**並べた

$$
A=\begin{pmatrix}\vert&\vert\\T(\boldsymbol{e}_1)&T(\boldsymbol{e}_2)\\\vert&\vert\end{pmatrix}
$$

が標準基底に関する表現行列です。

> **例題 3.2** $T(1,0)=(2,1)$、$T(0,1)=(-1,3)$ を満たす線形変換の表現行列と $T(3,-2)$ を求めてください。
>
> <details><summary>解答</summary>
>
> $$A=\begin{pmatrix}2&-1\\1&3\end{pmatrix},\qquad T\begin{pmatrix}3\\-2\end{pmatrix}=A\begin{pmatrix}3\\-2\end{pmatrix}=\begin{pmatrix}8\\-3\end{pmatrix}.$$
> </details>

## 3.3 合成変換と逆変換

$T(\boldsymbol{x})=A\boldsymbol{x}$ の後に $S(\boldsymbol{x})=B\boldsymbol{x}$ を行う合成変換は

$$
(S\circ T)(\boldsymbol{x})=S(T(\boldsymbol{x}))=B(A\boldsymbol{x})=(BA)\boldsymbol{x}
$$

です。したがって、行う順番とは逆に見える $BA$ が表現行列になります。

$A$ が正則なら $T$ は一対一かつ全射で、逆変換は

$$
T^{-1}(\boldsymbol{y})=A^{-1}\boldsymbol{y}
$$

です。$A$ が非正則なら空間を低い次元につぶすため、逆変換は存在しません。

> **例題 3.3** $T$ の行列を $A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$、$S$ の行列を $B=\begin{pmatrix}2&0\\0&-1\end{pmatrix}$ とします。$T$ の後に $S$ を行う合成変換と、その逆変換の行列を求めてください。
>
> <details><summary>解答</summary>
>
> $$BA=\begin{pmatrix}2&2\\0&-1\end{pmatrix}.$$
> 行列式は $-2\ne0$ なので逆変換が存在し、
> $$(BA)^{-1}=A^{-1}B^{-1}=\begin{pmatrix}1/2&1\\0&-1\end{pmatrix}.$$
> </details>

## 3.4 対称移動

原点を通る直線に関する対称移動は線形変換です。代表例は次の通りです。

| 対称の軸・中心 | 座標の変化 | 表現行列 |
|----------------|------------|----------|
| $x$ 軸 | $(x,y)\mapsto(x,-y)$ | $\begin{pmatrix}1&0\\0&-1\end{pmatrix}$ |
| $y$ 軸 | $(x,y)\mapsto(-x,y)$ | $\begin{pmatrix}-1&0\\0&1\end{pmatrix}$ |
| 原点 | $(x,y)\mapsto(-x,-y)$ | $\begin{pmatrix}-1&0\\0&-1\end{pmatrix}$ |
| 直線 $y=x$ | $(x,y)\mapsto(y,x)$ | $\begin{pmatrix}0&1\\1&0\end{pmatrix}$ |

$x$ 軸の正の向きとなす角が $\phi$ の、原点を通る直線に関する対称移動は、直線を $x$ 軸へ $-\phi$ 回転し、$x$ 軸対称にし、$\phi$ 回転して戻すことで

$$
H_\phi=
\begin{pmatrix}
\cos2\phi&\sin2\phi\\
\sin2\phi&-\cos2\phi
\end{pmatrix}
$$

となります。原点を通らない直線に関する対称移動は一般に原点を保たないため、線形変換ではなくアフィン変換です。

## 3.5 平面内の回転

原点を中心に反時計回りに角 $\theta$ だけ回転する線形変換の行列は

$$
R_\theta=
\begin{pmatrix}
\cos\theta&-\sin\theta\\
\sin\theta&\cos\theta
\end{pmatrix}
$$

です。第1列は $(1,0)$ の像 $(\cos\theta,\sin\theta)$、第2列は $(0,1)$ の像 $(-\sin\theta,\cos\theta)$ です。$R_\alpha R_\beta=R_{\alpha+\beta}$、$R_\theta^{-1}=R_{-\theta}=R_\theta^T$ が成り立ちます。

> **例題 3.4** 点 $(2,-1)$ を原点中心に反時計回りに $90^\circ$ 回転した像を求めてください。
>
> <details><summary>解答</summary>
>
> $$R_{90^\circ}=\begin{pmatrix}0&-1\\1&0\end{pmatrix},\qquad
> R_{90^\circ}\begin{pmatrix}2\\-1\end{pmatrix}=\begin{pmatrix}1\\2\end{pmatrix}.$$
> </details>

## よくある誤り

- 定数項を含む写像を、原点の像を確認せず線形変換と判断する。
- 基底の像を表現行列の行として並べる。
- 「$T$ の後に $S$」の行列を $AB$ とする。正しくは $BA$。
- 時計回りと反時計回りで $\sin\theta$ の符号を取り違える。
- 原点を通らない軸に関する対称移動も線形変換だと考える。

## 章末チェック

- [ ] 線形性の2条件を使って線形変換か判定できる
- [ ] 基底ベクトルの像から表現行列を作れる
- [ ] 行列をベクトルに掛けて点の像を求められる
- [ ] 合成する順序を保って表現行列を掛けられる
- [ ] 対称移動と回転の行列を導き、逆変換を求められる

さらに練習する場合は [`../exercises/`](../exercises/) に進みます。
<!-- /MAGI -->
