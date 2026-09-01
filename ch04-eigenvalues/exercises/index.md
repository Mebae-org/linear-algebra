<!-- MAGI -->
# 練習問題 - 第4章 固有値と固有ベクトル

> 対応: [`../docs/index.md`](../docs/index.md)

## 問1

$A=\begin{pmatrix}3&0\\0&-2\end{pmatrix}$ の固有値と、それぞれに属する固有ベクトルを求めてください。

<details><summary>解答</summary>

**答: $\lambda=3$ では $t(1,0)^T$、$\lambda=-2$ では $s(0,1)^T$（$t,s\ne0$）**

対角行列では対角成分が固有値です。各座標軸方向が対応する固有ベクトルになります。

</details>

## 問2

$A=\begin{pmatrix}2&1\\1&2\end{pmatrix}$ の固有値と固有ベクトルを求めてください。

<details><summary>解答</summary>

**答: $\lambda=3$ では $t(1,1)^T$、$\lambda=1$ では $s(1,-1)^T$（$t,s\ne0$）**

$\det(\lambda I-A)=(\lambda-2)^2-1=(\lambda-3)(\lambda-1)$ です。各固有値について $(A-\lambda I)\boldsymbol{v}=0$ を解きます。

</details>

## 問3

$\boldsymbol{v}=(1,2)^T$ は $A=\begin{pmatrix}3&1\\2&2\end{pmatrix}$ の固有ベクトルですか。

<details><summary>解答</summary>

**答: 固有ベクトルではない**

$A\boldsymbol{v}=(5,6)^T$ です。$(5,6)^T$ は $(1,2)^T$ の実数倍ではないため、固有ベクトルではありません。

</details>

## 問4

$A=\begin{pmatrix}4&0\\1&2\end{pmatrix}$ を対角化してください。

<details><summary>解答</summary>

**答: $P=\begin{pmatrix}2&0\\1&1\end{pmatrix}$、$D=\begin{pmatrix}4&0\\0&2\end{pmatrix}$ とすれば $P^{-1}AP=D$**

固有値は $4,2$ です。$\lambda=4$ の固有ベクトルに $(2,1)^T$、$\lambda=2$ の固有ベクトルに $(0,1)^T$ を選び、対応する順序で並べます。

</details>

## 問5

$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$ は対角化できますか。

<details><summary>解答</summary>

**答: 対角化できない**

固有値は $1$ のみで代数的重複度は2です。一方、$(A-I)\boldsymbol{v}=0$ から固有ベクトルは $t(1,0)^T$ に限られ、一次独立な固有ベクトルが2本得られません。

</details>

## 問6

固有値が $2,5$ である2次行列 $A$ のトレースと行列式を求めてください。

<details><summary>解答</summary>

**答: $\operatorname{tr}A=7$、$\det A=10$**

固有値の和がトレース、積が行列式です。

</details>
<!-- /MAGI -->
