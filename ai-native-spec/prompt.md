OK.
Zennの記事は一旦GitHubで先に公開する。
C:\Users\good\_\OneDrive\Documents\GitHub\articles\clean-architecture\article_ja.md

を参考に
C:\Users\good\_\OneDrive\Documents\GitHub\articles\ai-native-spec\article_ja.md
の書式を整えて。

コンセプトを決める — ソフトのコンセプトと解決すべき課題を明文化する（Ch1）
重要な判断を下す — 技術選定や仕様の分岐点で意志入れする（AIが適切なタイミングでユーザーに問いかける）
成果物を確認する — 成果物が要件を満たすか最終確認・承認する（Ch4を中心にAIが提示する成果物確認の提案をベースに使って）

これでどう？

- **When** [トリガー], the System **shall** [応答].
- **While** [状態], the System **shall** [応答].
- **If** [トリガー], then the System **shall** [応答].

ここは自動運転の具体例に置換 2行でいいよ

---

コンセプトを定義する — 何を作り、何を守るか決める（Ch1）
構造を決める — アーキテクチャの最終判断は人間が下す（Ch3）
合否を判定する — Gherkinシナリオに基づくUAT（Ch4-Ch5）

ずれたな。

元のマニュアルにはなんて書いてたっけ？
記事を更新する前にここに引用せよ。

章構成: STFB（上剛下柔）
STFBはフルセンテンスを併記せよ

👉
章番号を併記せよ

👉 要求には EARS
の前に1章の説明が全くないのは遺憾
1章だけは自身の経験と好みをかなり反映したけど。
は1章の説明に移動

Architecture (Mermaid):
シーケンス図でしょ？

コンセプトを定義する — AIに 何を 作るか伝える（Ch1）
重要な判断を下す — アーキテクチャを選び、曖昧さを解消する（Ch3）
結果を受け入れる — UAT、最終的な PASS/FAIL 判定（Ch4）

チャプターといまいち合ってない。
重要な判断を下す はどの章になるのだろう？
結果を受け入れる？ なんでも受け入れるわけじゃない。

Ch5 Test Strategy テスト戦略
ごめん指示不足 Ch6も必要。 レビューに使う旨シンプルに記事に書いて。

全部はかけないので、
→書けない。

全体的に、改行が不適切。
長い文章は**適切なところ**で、行末をダブルスペースを入れて改行せよ。
あくまで読者が斜め読みでも頭に入ることが重要

章構成の日英併記

Ch1 Foundation 基本事項 ← Rigid / 剛: rarely changes / めったに変わらない
Ch2 Requirements 要求
Ch3 Architecture 構造
Ch4 Specification 仕様 ← Flexible / 柔: changes often / よく変わる
Ch5 Test Strategy テスト戦略

にして。 基盤っていまいちピンとこんのよ。

章ごとに最適な記法
かな。

0.8秒 要らなくない？ 100ms と 1秒だけでいいやん。 記事なんだし。 混乱させてどうするの？

以下は日英併記で。
Chapter 1 Foundation ← 剛: めったに変わらない
Chapter 2 Requirements
Chapter 3 Architecture
Chapter 4 Specification ← 柔: よく変わる
Chapter 5 Test Strategy
Chapter 6 Design Principles

章ごとに最適な記法を選ぶ
の章名が微妙。 複数案提案せよ

ここは　層？ 章？ 提案せよ。 あと1列目の次に和訳の列も必要

具体例
100ms / 1秒 / 0.8秒の関係が不明。というかあってる？

タイトル長すぎ。
EARS・Gherkin・Mermaidを再構成して、AI用の仕様書テンプレートを作った

AI用の仕様書テンプレートを作ってみたよ

が良くない？

仕様書 = プロンプト なんだと。

の一文要らんよね？

When 前方2m以内に障害物を検知した場合,
は
2m はもう遅いよ。
もっと現実的な数値にして。　というか秒数かな。 1秒？

ファイル 内容
日本語の方を上において。 オリジナルが日本語だから。

しめはこれぐらいかな？ 強要する感じは好きじゃない。
次のAI駆動プロジェクトに取り込んでみては？
改善点や別の組み合わせのアイデアがあれば共有してくれると嬉しい。
みんなで楽しくやるのが好きだから♪
