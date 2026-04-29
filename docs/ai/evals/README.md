---
title: ai/evals/ 索引
purpose: AI 出力を評価する eval データセット・指標を蓄積する
when_to_read: プロンプト・モデルを変更する前、AI 機能の品質を評価したいとき
keywords: [eval, prompt eval, LLM, rubric, ハルシネーション]
---

# ai/evals/ — AI 評価セット

CONSTITUTION 第6条「Good/Bad データセット駆動」の AI 版。
モデル / プロンプト変更は本ディレクトリの eval を通すこと。

## 一覧

<!-- eval を追加したらここに 1 行ポインタを足す。例:
- [note-summary-eval](./note-summary-eval.md) — ノート要約の rubric 準拠率と引用整合性
-->

（まだ eval は登録されていません）

## 追加手順

1. [`_template.md`](./_template.md) をコピー
2. Good / Bad 出力例と rubric を書く
3. 主指標（例: rubric 一致率、ハルシネーション率、引用整合性）を定義
4. 関連 AI 機能 (`../features/<name>.md`) からリンク

## 推奨指標

| 指標 | 用途 |
| --- | --- |
| Rubric 準拠率 | 出力が定義したフォーマット・観点に従っているか |
| Ground truth 一致率 | 専門家ラベルとの一致 |
| ハルシネーション率 | 事実外言及の発生率 |
| 引用整合性 | 入力に存在する事実のみを根拠にしているか |
| 人手レビュー gating | しきい値以下では reject |
