<!-- MAGI -->
# 第2章 行列と連立一次方程式

> **注記:** このファイルは AI により保守されます。

## 2.1 行列の基本

数を長方形に並べたものを行列といいます。$m$ 行 $n$ 列の行列を $m\times n$ 行列といい、$A=(a_{ij})$ の $a_{ij}$ は第 $i$ 行第 $j$ 列の成分です。行数と列数が等しい行列を正方行列、対角成分がすべて1で他が0の行列を単位行列 $I$ といいます。

### 和、差、実数倍

和と差は同じ型の行列にだけ定義され、対応する成分ごとに計算します。実数倍も各成分を倍します。

$$
(a_{ij})+(b_{ij})=(a_{ij}+b_{ij}),\qquad k(a_{ij})=(ka_{ij}).
$$

> **例題 2.1** $A=\begin{pmatrix}1&-2\\3&0\end{pmatrix}$、$B=\begin{pmatrix}2&1\\-1&4\end{pmatrix}$ のとき、$2A-B$ を求めてください。
>
> <details><summary>解答</summary>
>
> $$2A-B=\begin{pmatrix}2&-4\\6&0\end{pmatrix}-\begin{pmatrix}2&1\\-1&4\end{pmatrix}=\begin{pmatrix}0&-5\\7&-4\end{pmatrix}.$$
> </details>

## 2.2 行列の積

$A$ が $m\times n$、$B$ が $n\times p$ のとき、積 $AB$ は $m\times p$ 行列です。その $(i,j)$ 成分は、$A$ の第 $i$ 行と $B$ の第 $j$ 列の内積

$$
(AB)_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj}
$$

です。「内側の数」$n$ が一致するときだけ積を作れます。一般に $AB\ne BA$ であり、片方だけが定義されることもあります。一方、結合法則 $(AB)C=A(BC)$ と分配法則 $A(B+C)=AB+AC$ は成り立ちます。

> **例題 2.2** $A=\begin{pmatrix}1&2\\-1&3\end{pmatrix}$、$B=\begin{pmatrix}2&0\\1&-2\end{pmatrix}$ の $AB$ と $BA$ を求めてください。
>
> <details><summary>解答</summary>
>
> $$AB=\begin{pmatrix}4&-4\\1&-6\end{pmatrix},\qquad BA=\begin{pmatrix}2&4\\3&-4\end{pmatrix}.$$
> 同じ行列にはならないため、積の順序を入れ替えてはいけません。
> </details>

## 2.3 逆行列と正則性

$n$ 次正方行列 $A$ に対し、$AA^{-1}=A^{-1}A=I$ を満たす行列 $A^{-1}$ を逆行列といいます。逆行列をもつ $A$ を正則、もたない $A$ を非正則といいます。

2次正方行列では

$$
A=\begin{pmatrix}a&b\\c&d\end{pmatrix},\qquad
A^{-1}=\frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}
$$

です。ただし $ad-bc\ne0$ が必要です。

### 掃き出し法による逆行列

一般の正方行列では、拡大行列 $(A\mid I)$ に次の行基本変形を行います。

1. 2つの行を交換する。
2. ある行を0でない実数倍する。
3. ある行に別の行の実数倍を加える。

左側を $I$ にできれば、右側が $A^{-1}$ です。左側に零行が現れて $I$ にできなければ、$A$ は非正則です。

> **例題 2.3** $A=\begin{pmatrix}2&1\\1&1\end{pmatrix}$ の逆行列を求めてください。
>
> <details><summary>解答</summary>
>
> $\det A=2\cdot1-1\cdot1=1$ なので正則です。公式から
> $$A^{-1}=\begin{pmatrix}1&-1\\-1&2\end{pmatrix}.$$
> 実際に $AA^{-1}=I$ で確認できます。
> </details>

## 2.4 行列式

正方行列 $A$ に対応する実数を行列式といい、$\det A$ または $|A|$ と書きます。2次では

$$
\det\begin{pmatrix}a&b\\c&d\end{pmatrix}=ad-bc.
$$

3次では、たとえば第1行について余因子展開すると

$$
\det A=a_{11}\begin{vmatrix}a_{22}&a_{23}\\a_{32}&a_{33}\end{vmatrix}
-a_{12}\begin{vmatrix}a_{21}&a_{23}\\a_{31}&a_{33}\end{vmatrix}
+a_{13}\begin{vmatrix}a_{21}&a_{22}\\a_{31}&a_{32}\end{vmatrix}.
$$

### 計算に使う性質

- 2つの行を交換すると、行列式の符号が変わる。
- 1つの行を $k$ 倍すると、行列式は $k$ 倍になる。
- 1つの行に別の行の実数倍を加えても、行列式は変わらない。
- 三角行列の行列式は対角成分の積である。
- $\det(AB)=\det A\det B$、$\det(A^T)=\det A$。
- $A$ が正則であることと $\det A\ne0$ は同値である。

> **例題 2.4** $A=\begin{pmatrix}1&2&0\\2&5&1\\0&1&3\end{pmatrix}$ の行列式を、行基本変形の性質を使って求めてください。
>
> <details><summary>解答</summary>
>
> 第2行から第1行の2倍を引いても値は変わりません。
> $$\det A=\begin{vmatrix}1&2&0\\0&1&1\\0&1&3\end{vmatrix}=\begin{vmatrix}1&2&0\\0&1&1\\0&0&2\end{vmatrix}=1\cdot1\cdot2=2.$$
> </details>

## 2.5 連立一次方程式

連立一次方程式は $A\boldsymbol{x}=\boldsymbol{b}$ と書けます。係数行列と定数列を並べた拡大係数行列 $(A\mid\boldsymbol{b})$ を行基本変形して階段形にする方法をガウスの消去法、さらに左側を簡約階段形にする方法をガウス・ジョルダン法（掃き出し法）といいます。

解の形は次の3通りです。

- 各未知数の値が定まり、一意解をもつ。
- 自由変数が残り、無数の解をもつ。
- $(0\ \cdots\ 0\mid c)$（$c\ne0$）という矛盾した行が現れ、解をもたない。

$A$ が正方かつ正則なら、一意解は $\boldsymbol{x}=A^{-1}\boldsymbol{b}$ です。ただし、計算では逆行列を明示的に求めるより掃き出し法の方が効率的なことが多くあります。

> **例題 2.5** 次の連立一次方程式を解いてください。
> $$\begin{cases}x+y+z=4,\\2x-y+z=1,\\x+2y-z=3.\end{cases}$$
>
> <details><summary>解答</summary>
>
> $$\left(\begin{array}{ccc|c}1&1&1&4\\2&-1&1&1\\1&2&-1&3\end{array}\right)
> \longrightarrow
> \left(\begin{array}{ccc|c}1&0&0&1\\0&1&0&1\\0&0&1&2\end{array}\right).$$
> よって $(x,y,z)=(1,1,2)$ です。
> </details>

## よくある誤り

- 行列の積を成分ごとの積として計算する。
- $AB=BA$ として積の順序を変える。
- 逆行列の公式を $\det A=0$ のときにも使う。
- 行を $k$ 倍したとき、行列式も $k$ 倍になることを忘れる。
- 掃き出し法で、定数列に同じ行基本変形を行わない。

## 章末チェック

- [ ] 行列の型から、和や積が定義されるか判断できる
- [ ] 行列の和、差、実数倍、積を正しく計算できる
- [ ] 行列式から正則性を判定し、逆行列を求められる
- [ ] 行列式の性質を選んで計算を簡単にできる
- [ ] 掃き出し法で連立一次方程式を解き、解の個数も判断できる

さらに練習する場合は [`../exercises/`](../exercises/) に進みます。
<!-- /MAGI -->
