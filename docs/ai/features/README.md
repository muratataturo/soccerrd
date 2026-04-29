---
title: ai/features/ 索引
purpose: AI 機能ごとの設計・プロンプト・関連 eval を集約する
when_to_read: AI 機能を実装・改修するとき
keywords: [AI 機能, prompt, サッカーNote]
---

# ai/features/ — AI 機能仕様

機能 1 つにつき 1 ファイル。`product/features/<name>.md` と 1:1 対応するか、AI 単独機能として独立させる。

## 一覧

<!-- AI 機能を追加したらここに 1 行ポインタを足す。例:
- [note-summarizer](./note-summarizer.md) — ノートを要約しタグを生成
-->

（まだ AI 機能は登録されていません）

## 追加手順

1. [`_template.md`](./_template.md) をコピー
2. プロンプト本体・eval リンクを記載
3. 関連 `product/features/<name>.md` からリンク
4. プロンプト変更時は eval を再実行し、結果を更新履歴に記録
