<!-- MAGI -->
# 線形代数

ベクトル、行列、線形変換、固有値を基礎から学ぶ教材です。各章に解説（`docs/`）、解答付き練習問題（`exercises/`）、提出課題（`assignments/`）をまとめています。

## 対象

- 対象者: 大学・高等専門学校の初学者、線形代数を学び直したい人
- 前提知識: 中学校から高等学校程度の式計算、座標、一次・二次方程式、三角比
- 到達目標: ベクトルと行列を計算し、空間図形、連立一次方程式、線形変換、固有値問題へ応用できる

## 使い方

1. 各章の `README.md` で概要と学習目標を確認します。
2. `docs/` で内容を学びます。
3. `exercises/` で理解を確認します。
4. `assignments/` の課題を解き、Issue Form から数値解答を提出します。
5. GitHub Actions の採点コメントを確認します。不正解の場合は新しい Issue から再挑戦できます。

提出課題は各章5問、1問4点の20点満点です。解答欄には単位や式を含めず、整数1つを入力します。全角数字、全角記号、空白は採点時に正規化されます。

## 章一覧

| 章 | タイトル | 概要 |
|----|----------|------|
| [第1章](./ch01-vectors/) | ベクトルと空間図形 | ベクトルの演算、内積、平行・垂直、直線・平面・球 |
| [第2章](./ch02-matrices/) | 行列と連立一次方程式 | 行列の演算、逆行列、行列式、連立一次方程式 |
| [第3章](./ch03-linear-transformations/) | 線形変換 | 表現行列、合成・逆変換、対称移動、回転 |
| [第4章](./ch04-eigenvalues/) | 固有値と固有ベクトル | 固有値・固有ベクトル、対角化とその応用 |

モデルコアカリキュラムの各到達目標と章の対応は、各章の `README.md` に示します。

## ディレクトリ構成

```text
[REPOSITORY]/
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── LICENSE-CODE
├── .github/
└── chNN-short-name/
    ├── README.md
    ├── docs/
    ├── exercises/
    └── assignments/
```

## ライセンス

- **教材・文章・図版**: [CC BY 4.0](./LICENSE)
- **サンプルコード**: [MIT](./LICENSE-CODE)

## 貢献・誤り報告

執筆手順は [`CONTRIBUTING.md`](./CONTRIBUTING.md) を参照してください。誤りの指摘や提案は [Issue](https://github.com/Mebae-org/linear-algebra/issues/new/choose) からお願いします。
<!-- /MAGI -->
