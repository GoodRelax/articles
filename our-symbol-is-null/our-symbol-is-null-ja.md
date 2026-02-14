---
layout: default
title: "みんなの象徴はNullである"
date: 2026-02-14
lang: ja
key: our-symbol-is-null
tags: [idea, poem, LLM, mathematics, philosophy]
---

## **みんなの象徴はNull** である

### The Symbol for All of Us is Null

いきなり何を言い出すんだ、と思うかもしれない。

でも本稿を見つけたあなただったら、 きっとこの話はどこかで腹に落ちるだろう。

**5分ください**

- この世界を理解するために、人類が無意識にやっていること。
- AIがまったく同じことをしていること。
- 数学がそれを綺麗に説明してくれること。

そして最後に、

- **なぜ Null がすべての象徴になるのか**

が、一本の線でつながるから。

順に語ろう。

---

## 分かるとは「分ける」こと

世界には、わからないことがたくさんある。

しかし私たちは、それに立ち向かう知恵を持っている。

違う物事に名前を付け、分類することで理解を進める。

丸い果物を

- リンゴ
- ミカン
- 梨

と分けて理解するように。

これは誰もが無意識に行っている、認知のロジックだ。

---

## AIも同じことをしている

AIは**言葉を無限次元のベクトルで理解**する。

どういうことかって？ ここもちゃんと「**分けて理解**」しよう。

- 言葉を： 物事や概念にそれぞれIDを振って
- 無限次元の： 100万個とか実質無限個の添え字をつけられる
- ベクトルで： 向きと長さの矢印に変換可能な配列形式のデータとして
- 理解する： いい感じに整理整頓する

疑似コードで書くとこう

<pre>
 apple = [2, 3, 5, ...]  
 orange = [3, 5, 7, ...]

 dirOfApple = GetDirection(apple)  
 lenOfApple = GetLength(apple)
</pre>

絵で表すと、こうなる。

<object data="./assets/images/embedding.svg" type="image/svg+xml" style="max-width:50vw;"></object>

ChatGPT や Gemini のような LLM(Large Language Model) は、だいたいこの仕組み。  
Embedding (埋め込み) ってやつ。

詳しくは 3Blue1Brown の動画を参照されたし。名作ばかりだ。

[Transformers, the tech behind LLMs - Deep Learning Chapter 5](https://www.youtube.com/watch?v=wjZofJX0v4M)  
[GPTとは何か Transformerの視覚化 - Chapter 5, Deep Learning](https://www.youtube.com/watch?v=KlZ-QmPteqM)

---

## 類比 ↔︎ 対比 / 帰納 ↔︎ 演繹 / 具体 ↔︎ 抽象

大抵のスポーツや武道に基本の型があるように、物の見方にも基本の型がある。それがこの3対。  
無意識にやってる人が多いが、一度言語化して意識的に行う訓練をすると理解がとても早く深くなる。

<pre>
 類比 ↔︎ 対比 :  リンゴもミカンも甘い。
                      ↑↓
               リンゴは赤いミカンは黄色。

 帰納 ↔︎ 演繹 :  木からリンゴが落ちた。引力があるようだ。
                      ↑↓
               枝からとれたミカンは、引力によって地に落ちる。

 具体 ↔︎ 抽象 :  丸くて赤くて甘いリンゴと、丸くて黄色で甘いミカンがある。
                      ↑↓
               丸い果物が2つある。
</pre>

何をあたり前なことを？ ではもう少しちゃんと理解しよう。  
ここからだんだん本気になるよ。  
簡単な数学を使う。でも厳密な数学じゃないからどうぞお気楽に。 数式は読み飛ばして全然OK。

---

### 類比と対比は「写像」である

類比とは共通点を探すこと。 対比とは相違性を探すこと。

例を示そう。

リンゴは、丸くて、赤くて、甘い  
ミカンは、丸くて、黄色で、甘い

これを類比や対比すると

- 類比(Analogy)：同じ方向への線形変換 → リンゴもミカンも甘くて丸い
- 対比(Contrast)：逆方向への線形変換 → リンゴは赤いが、ミカンは黄色

となる。

ベクトル図にするとこうなる。

<object data="./assets/images/analogy-and-contrast.svg" type="image/svg+xml" style="max-width:90vw;"></object>

数式だと、線形写像 $ Ta $ / $ Tc $ によって

- $ 類比 : Ta(\vec{apple}) \uparrow Ta(\vec{orange}) $

- $ 対比 : Tc(\vec{apple}) \downarrow Tc(\vec{orange}) $

と表現できる。

---

### 帰納と演繹は「ベクトルの差と和」である

帰納とは過去の具体的な物事から法則を探求する(さがす)こと。  
演繹とは法則から未来の具体的な物事を推論する(あてる)こと。

ニュートンの万有引力が良い例だ。

<pre>
帰納(Induction)： 法則ベクトルの抽出(抜き出し)   
                  → 木からリンゴが落ちた。引力があるようだ。

演繹(Deduction)： 法則ベクトルの重畳(重ね合わせ) 
                  → 枝から離れたミカンは、引力によって地に落ちる。
</pre>

ベクトル図にするとこうなる。

<object data="./assets/images/induction-and-deduction.svg" type="image/svg+xml" style="max-width:90vw;"></object>

数式だと関数を使って

- $ 帰納 : \text{Extraction}(\vec{past}) \Rightarrow \vec{law} \mid \vec{law} = \vec{facts} - \vec{noise}$

- $ 演繹 : \text{Superposition}(\vec{object}) \Rightarrow \vec{future} \mid \vec{future} = \vec{object} + \vec{law}$

と表現できる。

---

### 具体と抽象は「情報量の増加減」である

- 具体化(Concretize)とはパラメータ(属性)を追加して情報量を増やすこと。
- 抽象化(Abstract)とはパラメータ(属性)を減らして、情報量を絞ること。  
  **いい感じの本質に向かって。**

例を示そう。

「果物」という抽象に、「丸型」、「赤色」、「甘い」というパラメータを追加すると「リンゴ」になる。
「リンゴ」からいろんなパラメータを削減すると「丸型」になる

図にするとこうなる。

<object data="./assets/images/concretize-and-abstract.svg" type="image/svg+xml" style="max-width:90vw;"></object>

数式だと、例えばこう書ける。

- $ 具体化 : \text{Concretize}(\vec{object}) \Rightarrow \vec{object} \oplus \vec{parameters} $

- $ 抽象化 : \text{Abstract}(\vec{object}) \Rightarrow \vec{object} \ominus \vec{parameters} $

「人間」という抽象に、「47歳」と「男」というパラメータを追加すると「おっさん」になるね。

---

## いい感じの本質

情報量を減らして抽象化する際、闇雲に情報を減らしていくと、よく分からんことになる。  
おっさんから髭を取って皺を取ったら、少年になってしまう。 本質的な情報だけを抽出したい。

そんなときに使えるのが PCA（Principal Component Analysis / 主成分分析）。  
PCA? 何それおいしいの？ って人もきっと経験したことがある。

50問ぐらいのアンケートに答えたら、直感的⇔論理的 vs 外交的⇔内向的 とかのマトリクスに性格分類する奴。  
50問のアンケートは 50次元ベクトル。 それを 2次元に落として「性格マップ」にする。

<object data="./assets/images/personality_profiling_ja.svg" type="image/svg+xml" style="max-width:90vw;"></object>

数式で書くとこう。

- 抽出:  
  $\text{Extract}(\vec{data}) \Rightarrow \vec{essence} \mid \vec{essence} = Z W_k \mid W_k = [\vec{v}_1, \dots, \vec{v}_k] \text{ where } \Sigma \vec{v} = \lambda \vec{v}$

  ...
  - $ Z ： Zero-centering $（中心化）
  - $ W ： Weight $（重み付け）
  - $ \lambda ：$ 固有値 ＝ MECEに整理した各情報のサイズ
  - MECE: Mutually Exclusive, Collectively Exhaustive / モレなくダブりなく

$ k = 2 $ にすれば 2次元のマトリクスになる

これって、私たちが無意識にやっている「ざっくり理解」と同じ。

詳しくはこの動画がおすすめ。

[Abstract vector spaces - Chapter 16, Essence of linear algebra](https://www.youtube.com/watch?v=TgKwz5Ikpc8)  
[Chapter 16 抽象ベクトル空間 - 線形代数のエッセンス](https://www.youtube.com/watch?v=FhIXzQdIwRI)

---

### シンボル(象徴)とは「第1主成分」である

物事を整理していくと重要な情報とそうでない情報があるわけで。  
一番重要な情報をシンプルに覚えやすく表現したくなる。

それが**シンボル(象徴)**

旗、マーク、王様、アイドル...

人々が何かを象徴として掲げるとき、やっていることはこれ。  
みんなのベクトルから、一番大事なベクトルに目を向ける

一番大事なベクトル = PCA の **主成分ベクトル** ってわけ。

<object data="./assets/images/symbol.svg" type="image/svg+xml" style="max-width:90vw;"></object>

- 厳密には PCA の第1主成分は「分散が最大の方向」であり、  
  「最も意味がある方向」とは限らないが、数学的メタファーってことで。

---

### 抽象化の極限は？

- 立体の情報をそぎ落として面にする
- 面の情報をそぎ落として線にする
- 線の情報をそぎ落として点にする
  → $ \mathbb{R}^0 $ の点には、座標という情報が残っている。
- 点の情報をもそぎ落とすと...?

$$
    H( \mathbb{R}^3 ) > H( \mathbb{R}^2 ) > H( \mathbb{R}^1 ) > H( \mathbb{R}^0 ) = 0 \quad \gg \quad \emptyset = \text{Null}
$$

最後に残るのは **何もない空間**

## それが**Null（無）**

<object data="./assets/images/ultimate-symbol.svg" type="image/svg+xml" style="max-width:90vw;"></object>

森羅万象を抽象化し続けると最後は**Null** (**無**)になる

だから **Null** は、

- 誰のものでもなく
- 何の属性も持たず
- すべてのベクトルそぎ落とした**究極のシンボル**になる。

リンゴも、ミカンも、あなたも、私も。

### 無限次元のノイズを削ぎ落とした先に、誰もが辿り着く同じ空間。 それが **Null。**

天地開闢、色即是空、ビッグバン....、だいたい同じこと。

#### 同じシンボルに集いし友よ！仲良くしようぜ♪

(c) 2026 GoodRelax. MIT License.
