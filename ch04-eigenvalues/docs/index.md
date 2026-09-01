<!-- MAGI -->
# 第4章 固有値と固有ベクトル

> **注記:** このファイルは AI により保守されます。

## 4.1 固有値・固有ベクトルとは

$n$ 次正方行列 $A$ に対し、零ベクトルでない $\boldsymbol{v}$ と実数または複素数 $\lambda$ が

$$
A\boldsymbol{v}=\lambda\boldsymbol{v}
$$

を満たすとき、$\lambda$ を $A$ の固有値、$\boldsymbol{v}$ を $\lambda$ に属する固有ベクトルといいます。線形変換 $A$ によって、$\boldsymbol{v}$ の向きは変わらず $\lambda$ 倍されます。$\lambda<0$ なら向きは反転し、$\lambda=0$ なら零ベクトルへ移ります。

固有ベクトル自身は零ベクトルではありません。ただし、固有ベクトルの0でない実数倍も同じ固有値の固有ベクトルです。

## 4.2 固有値の求め方

定義式を移項すると

$$
(A-\lambda I)\boldsymbol{v}=\boldsymbol{0}
$$

です。$\boldsymbol{v}\ne\boldsymbol{0}$ となる解が存在するには $A-\lambda I$ が非正則でなければならないため、

$$
\det(A-\lambda I)=0
$$

が必要です。これを特性方程式といいます。$\det(\lambda I-A)=0$ を使っても根は同じですが、途中の符号を一方に統一します。

2次行列 $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ では

$$
\det(\lambda I-A)=\lambda^2-(a+d)\lambda+(ad-bc)
=\lambda^2-(\operatorname{tr}A)\lambda+\det A.
$$

したがって、固有値の和はトレース $a+d$、積は行列式 $ad-bc$ となり、検算に使えます。

> **例題 4.1** $A=\begin{pmatrix}4&1\\2&3\end{pmatrix}$ の固有値を求めてください。
>
> <details><summary>解答</summary>
>
> $$\det(\lambda I-A)=\begin{vmatrix}\lambda-4&-1\\-2&\lambda-3\end{vmatrix}
> =\lambda^2-7\lambda+10=(\lambda-5)(\lambda-2).$$
> よって固有値は $5,2$ です。和 $7$ はトレース、積 $10$ は行列式と一致します。
> </details>

## 4.3 固有ベクトルの求め方

固有値 $\lambda$ ごとに、同次連立一次方程式

$$
(A-\lambda I)\boldsymbol{v}=\boldsymbol{0}
$$

を解きます。自由変数を1つ以上残し、零ベクトルを除いた解が固有ベクトルです。

> **例題 4.2** 例題4.1の各固有値に属する固有ベクトルを求めてください。
>
> <details><summary>解答</summary>
>
> $\lambda=5$ のとき
> $$A-5I=\begin{pmatrix}-1&1\\2&-2\end{pmatrix}$$
> なので $-x+y=0$、すなわち $y=x$ です。固有ベクトルは $t(1,1)^T$（$t\ne0$）です。
>
> $\lambda=2$ のとき
> $$A-2I=\begin{pmatrix}2&1\\2&1\end{pmatrix}$$
> なので $2x+y=0$ です。固有ベクトルは $s(1,-2)^T$（$s\ne0$）です。
>
> 実際に $A(1,1)^T=5(1,1)^T$、$A(1,-2)^T=2(1,-2)^T$ となります。
> </details>

## 4.4 重複する固有値

特性方程式で同じ根が複数回現れることがあります。根として現れる回数を代数的重複度、固有空間 $\ker(A-\lambda I)$ の次元を幾何学的重複度といいます。幾何学的重複度は1以上、代数的重複度以下です。

たとえば

$$
A=\begin{pmatrix}2&1\\0&2\end{pmatrix}
$$

は固有値 $2$ を2重にもつ一方、$(A-2I)\boldsymbol{v}=\boldsymbol{0}$ から固有ベクトルは $t(1,0)^T$（$t\ne0$）だけです。「2重の固有値だから独立な固有ベクトルが2本ある」とは限りません。

## 4.5 対角化

$n$ 次行列 $A$ に一次独立な固有ベクトルが $n$ 本あれば、それらを列に並べた行列 $P$ と、対応する固有値を同じ順序で対角成分に並べた行列 $D$ によって

$$
P^{-1}AP=D,\qquad A=PDP^{-1}
$$

とできます。これを対角化といいます。固有値がすべて異なれば、対応する固有ベクトルは一次独立なので対角化できます。固有値が重複する場合は、一次独立な固有ベクトルが必要な本数だけ得られるか確認します。

対角行列の累乗は各対角成分を累乗するだけなので、

$$
A^k=PD^kP^{-1}
$$

により行列の高い累乗を計算できます。

> **例題 4.3** $A=\begin{pmatrix}4&1\\2&3\end{pmatrix}$ を対角化してください。
>
> <details><summary>解答</summary>
>
> 例題4.2の固有ベクトルを固有値 $5,2$ の順に並べて
> $$P=\begin{pmatrix}1&1\\1&-2\end{pmatrix},\qquad D=\begin{pmatrix}5&0\\0&2\end{pmatrix}.$$
> $\det P=-3\ne0$ なので $P$ は正則であり、$P^{-1}AP=D$ です。列の順序を変える場合は、$D$ の固有値の順序も同時に変えます。
> </details>

## 計算手順のまとめ

1. $\det(\lambda I-A)$ を計算する。
2. 特性方程式 $\det(\lambda I-A)=0$ を解く。
3. 各 $\lambda$ について $(A-\lambda I)\boldsymbol{v}=\boldsymbol{0}$ を解く。
4. $\boldsymbol{v}\ne\boldsymbol{0}$ とし、必要なら基底として簡単な固有ベクトルを選ぶ。
5. $A\boldsymbol{v}=\lambda\boldsymbol{v}$、固有値の和と積で検算する。

## よくある誤り

- $A-\lambda I$ で対角成分以外からも $\lambda$ を引く。
- 固有値だけ求めて、固有ベクトルを求め忘れる。
- 同次方程式の解として零ベクトルだけを書く。
- 異なる固有値に対して同じ式 $(A-\lambda I)\boldsymbol{v}=0$ を使い回す。
- $P$ の列と $D$ の対角成分の対応順をずらす。

## 章末チェック

- [ ] 特性方程式を正しく立てて解ける
- [ ] 各固有値について固有空間を求められる
- [ ] 定義式とトレース・行列式を使って検算できる
- [ ] 重複固有値で独立な固有ベクトルの本数を確認できる
- [ ] 対角化可能な行列を対角化し、累乗へ応用できる

さらに練習する場合は [`../exercises/`](../exercises/) に進みます。
<!-- /MAGI -->
