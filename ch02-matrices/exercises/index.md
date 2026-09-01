<!-- MAGI -->
# 練習問題 - 第2章 行列と連立一次方程式

> 対応: [`../docs/index.md`](../docs/index.md)

## 問1

$A=\begin{pmatrix}1&2\\0&-1\end{pmatrix}$、$B=\begin{pmatrix}3&0\\2&1\end{pmatrix}$ の $A+B$、$AB$、$BA$ を求めてください。

<details><summary>解答</summary>

**答: $A+B=\begin{pmatrix}4&2\\2&0\end{pmatrix}$、$AB=\begin{pmatrix}7&2\\-2&-1\end{pmatrix}$、$BA=\begin{pmatrix}3&6\\2&3\end{pmatrix}$**

積では左の行と右の列の内積を取ります。$AB\ne BA$ であることも確認できます。

</details>

## 問2

$A=\begin{pmatrix}3&1\\5&2\end{pmatrix}$ が正則か判定し、正則なら逆行列を求めてください。

<details><summary>解答</summary>

**答: 正則、$A^{-1}=\begin{pmatrix}2&-1\\-5&3\end{pmatrix}$**

$\det A=6-5=1\ne0$ なので正則です。2次行列の公式を使います。

</details>

## 問3

$A=\begin{pmatrix}1&2&3\\0&-1&2\\0&0&4\end{pmatrix}$ の行列式を求めてください。

<details><summary>解答</summary>

**答: $\det A=-4$**

上三角行列なので、行列式は対角成分の積 $1\cdot(-1)\cdot4=-4$ です。

</details>

## 問4

$\det A=-2$ である3次正方行列 $A$ について、$A$ の第1行と第2行を交換した後、第3行を5倍して得られる行列 $B$ の行列式を求めてください。

<details><summary>解答</summary>

**答: $\det B=10$**

行交換で符号が変わって $2$、1行を5倍すると行列式も5倍になるため $10$ です。

</details>

## 問5

連立方程式 $2x+y=5$、$x-y=1$ を行列を用いて解いてください。

<details><summary>解答</summary>

**答: $(x,y)=(2,1)$**

$$\left(\begin{array}{cc|c}2&1&5\\1&-1&1\end{array}\right)
\longrightarrow
\left(\begin{array}{cc|c}1&0&2\\0&1&1\end{array}\right).$$

</details>

## 問6

次の連立方程式の解の個数を判定し、解があれば表してください。
$$x+2y=3,\qquad 2x+4y=6.$$

<details><summary>解答</summary>

**答: 無数の解をもち、$(x,y)=(3-2t,t)$（$t\in\mathbb{R}$）**

第2式は第1式の2倍で、独立な条件は1つだけです。$y=t$ と置けば $x=3-2t$ です。

</details>
<!-- /MAGI -->
