---
title: "GRSMD — ブラウザだけで動く Markdown ビューワー を作ったよ"
emoji: "🐵"
type: "idea"
topics:
  - "markdown"
  - "plantuml"
  - "mermaid"
published: true
published_at: "2026-01-25 12:54"
---

2026-03-01 : 大幅アップデート!
![](https://storage.googleapis.com/zenn-user-upload/eb9f790e963b-20260301.png)

**GRSMD: GoodRelax Simple Markdown Renderer & Viewer**は、  
ブラウザ上だけで動作する、プライバシー重視の Markdown レンダラー & ビューワー です。

- 完全無料。 広告無し。 インストール不用。 プラグイン不用。 OSS。
- Markdown / Mermaid / 数式 / シンタックスハイライトは完全にクライアントサイドで描画
- PlantUML はユーザーの同意を得た場合のみレンダリング
- バックエンドなし、データ収集なし
- Mermaid / PlantUMLの図を SVG / PNGにコピーしてPPTに貼り付け可能

## サイト

以下のページで、そのまま試せます。

👉 https://goodrelax.github.io/gr-simple-md-renderer/

## 使い方

1. ページを開いて MarkdownをCtrl +v で貼り付け
   　 または、.md/.txt を ドラッグ & ドロップ
2. 完了

PlantUML を含む場合は、明示的な同意を取った上でのみ処理されます。

## サンプルデータ（コピペ用）

Mermaid 図・シーケンス図・コードブロックを含む  
サンプルデータはこちらです。

👉 https://goodrelax.github.io/gr-simple-md-renderer/sample-data.md
👉 https://goodrelax.github.io/gr-simple-md-renderer/sample-data-2.md

## GitHub

ソースコードはこちら。

👉 https://github.com/GoodRelax/gr-simple-md-renderer

## 改善

2026-02-23 : 大きなシーケンス図をズームできるようにした。  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;...実務でかなり便利。
2026-03-01 : 1手でMarkdownビューを表示できるようにした。  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;...これ以上の省力化はできんだろう。
2026-03-01 : SVG/PNGをコピペ可能に。  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... まだまだパワポ資料が要るし。
2026-03-01 : MCBSMDのプロンプトを改良。  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;... [?] を長押ししたらわかるよ。
