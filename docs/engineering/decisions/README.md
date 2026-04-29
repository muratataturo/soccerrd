---
title: decisions/ 索引 — アーキテクチャ判断記録 (ADR)
purpose: 後戻りしづらい技術判断の理由を時系列に残す
when_to_read: 既存判断の理由を知りたいとき、新規判断を記録するとき
keywords: [ADR, architecture, decision]
---

# decisions/ — Architecture Decision Records

ファイル命名: `NNNN-<short-title>.md`（連番、kebab-case）。例: `0001-data-model.md`。

## 一覧

<!-- ADR を追加したらここに 1 行ポインタを足す。例:
- [0001-data-model](./0001-data-model.md) — accepted — サッカーNote のコアデータモデル
-->

（まだ ADR は登録されていません）

## 追加手順

1. [`_template.md`](./_template.md) をコピーし連番を振る
2. ステータスは `proposed` → 議論を経て `accepted` / `rejected`
3. 過去の ADR を上書きする場合は、「Supersedes #N」と明記し、旧 ADR は `superseded` に更新
