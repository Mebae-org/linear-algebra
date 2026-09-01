<!-- MAGI -->
# 練習問題 - 第3章 線形変換

> 対応: [`../docs/index.md`](../docs/index.md)

## 問1

$T(x,y)=(2x+y,x-y)$ は線形変換ですか。線形変換なら表現行列と $T(-1,3)$ を求めてください。

<details><summary>解答</summary>

**答: 線形変換、表現行列は $\begin{pmatrix}2&1\\1&-1\end{pmatrix}$、$T(-1,3)=(1,-4)$**

各成分が $x,y$ の一次結合で定数項を含まないため線形です。表現行列を座標ベクトルに掛けて像を得ます。

</details>

## 問2

$S(1,0)=(1,2)$、$S(0,1)=(3,-1)$ を満たす線形変換 $S$ の表現行列を求めてください。

<details><summary>解答</summary>

**答: $\begin{pmatrix}1&3\\2&-1\end{pmatrix}$**

標準基底の像を列として並べます。

</details>

## 問3

$T$ と $S$ の表現行列がそれぞれ $A=\begin{pmatrix}1&2\\0&1\end{pmatrix}$、$B=\begin{pmatrix}0&-1\\1&0\end{pmatrix}$ のとき、$T$ の後に $S$ を行う合成変換の行列を求めてください。

<details><summary>解答</summary>

**答: $BA=\begin{pmatrix}0&-1\\1&2\end{pmatrix}$**

$S(T(\boldsymbol{x}))=B(A\boldsymbol{x})=(BA)\boldsymbol{x}$ です。

</details>

## 問4

直線 $y=x$ に関する対称移動の行列を求め、点 $(3,-2)$ の像を求めてください。

<details><summary>解答</summary>

**答: 行列は $\begin{pmatrix}0&1\\1&0\end{pmatrix}$、像は $(-2,3)$**

$y=x$ に関する対称移動では $x$ 座標と $y$ 座標が入れ替わります。

</details>

## 問5

原点を中心に時計回りに $30^\circ$ 回転する行列を求めてください。

<details><summary>解答</summary>

**答: $\begin{pmatrix}\sqrt3/2&1/2\\-1/2&\sqrt3/2\end{pmatrix}$**

時計回り $30^\circ$ は反時計回り $-30^\circ$ です。$R_\theta$ に $\theta=-30^\circ$ を代入します。

</details>

## 問6

$A=\begin{pmatrix}2&1\\1&1\end{pmatrix}$ で表される線形変換の逆変換の行列を求めてください。

<details><summary>解答</summary>

**答: $A^{-1}=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}$**

$\det A=1$ なので逆変換が存在し、その表現行列は $A^{-1}$ です。

</details>
<!-- /MAGI -->
