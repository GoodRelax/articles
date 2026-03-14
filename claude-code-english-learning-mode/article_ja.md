---
layout: default
title: "プロンプトを書きながら英語を身に付ける作戦"
date: 2026-03-14
lang: ja
key: claude-code-english-learning-mode
tags: [ai, claudecode, productivity, english, skill]
---

## 目次

- Table of Contents
  {:toc}

---

## なぜ？

Claude (Code)に毎日のようにプロンプトを打つ。  
でも、英語もちょっとは勉強しておきたい。  
⇒　そんなん一緒にやればいいじゃん！

## なにした？

英語でプロンプトを打ったら、一旦、英語チェックしてから作業するようClaudeに指示するスキルを作った。

## どうやる？

### インストール方法（Claude Chat / Claude Cowork）

#### プロンプトで（推奨）

1. 下記のプロンプトを貼り付ける：

```
下記リンクのスキルを SKILL.md として出力せよ。
結果を自分のスキルにコピーして、/en で使えるようにする。
https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md
```

2. 出力後、**「自分のスキルにコピー」** ボタンを押す。

#### 手動で

1. [SKILL.md](https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md) を右クリック → **「名前を付けてリンク先を保存」** → ファイル名を `SKILL.md` にする（`.txt` になる場合は `.md` に変更）
2. **カスタマイズ → スキル → 「+」 → 「スキルをアップロード」** でアップロード

### インストール方法（Claude Code）

#### プロンプトで（推奨）

下記のプロンプトを貼り付ける：

```
下記リンクのスキルをダウンロードして ~/.claude/skills/en/SKILL.md に保存せよ。
※プロジェクトの .claude/ ではなく、ユーザーホームの ~/.claude/ に配置すること。
https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md
```

#### 手動で

1. [SKILL.md](https://raw.githubusercontent.com/GoodRelax/gr-tools/refs/heads/main/gr-en-coach/skills/en/SKILL.md) を右クリック → **「名前を付けてリンク先を保存」** → ファイル名を `SKILL.md` にする（`.txt` になる場合は `.md` に変更）
2. `~/.claude/skills/en/SKILL.md` に配置（プロジェクトではなくユーザーホーム）

## 使い方

**`/en on` で英語練習モード開始。 `/en off` で終了。**  
これで、毎日のClaude活用がミニ英語レッスンになる。

### 練習の流れ：

1. **英語でプロンプトを書く**
2. **Claude が文法をチェック** — 間違い、不自然な表現、タイポを指摘
3. **Claude が意図を確認** — やりたいことを自然な英語で言い直す
4. **確認したら実行** — そこから通常通りタスクを実行

## おいしいの？

ちょうどいい先生になってくれたよ。 嫌味じゃない程度に方向修正してくれる。さすがClaudeやね。

> 今どきはAIが優秀なので、英語無しでもなんとかなるけどさ。
> 世界を相手にすると、英語ができないのはハンディキャップでしかない。
> そもそもプログラミング言語が英語ベースだし。
>
> 外人さんとの話すとき、自動通訳は原理上レイテンシーをゼロにできないからイライラするし、そもそも、合成音声だと言葉に魂が入らない。
> 下手でもやっぱり英語を使うべき。
> でも、せっかくなら上手くなりたい...よね？

ただし、実のところ、このスキルの対象者はすこし英語ができる人向け。  
だいたい、英検3~4級以上。　あとは本人のガッツ次第♪

:::details 具体例（クリックで展開）

ユーザー:

> I'd like to write a article for this EN skill. The first, show me a proposal of the folder name.

Claude:

> - "write **a** article" — what article should come before a word starting with a vowel sound?
> - "**The first**, show me..." → More natural: **"First, show me..."**
>
> You'd like to write an article about the /en skill, and you want me to first propose a folder name — is that right?

ユーザー:

> "Correct."

あとは普通に作業が進む。

説教なし。中断なし。さっと直して、確認して、仕事に戻る。

:::

このスキルが誰かの役に立ったら幸いです。

© 2026 GoodRelax. MIT License.
