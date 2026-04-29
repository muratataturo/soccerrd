---
title: product/features 索引
purpose: 機能仕様書一覧。各機能は CONSTITUTION とのマッピングを持ち、定量指標で評価される
when_to_read: 既存機能の仕様確認、新規機能を追加する前
keywords: [機能仕様, feature spec, マッピング, ロードマップ]
---

# product/features/ — 機能仕様書

機能ごとに 1 ファイル。命名規則は `kebab-case.md`。

## 一覧

<!-- 機能を追加したらここに 1 行ポインタを足す: `- [機能名](./<name>.md) — 1 行説明` -->

（まだ機能仕様は登録されていません）

## 新規追加の手順

1. [`_template.md`](./_template.md) をコピーして `<name>.md` を作る
2. CONSTITUTION とのマッピング（方向性 × 優先度 × 定量指標）を冒頭に書く
3. Good / Bad データセット（[engineering/datasets/](../../engineering/datasets/)）を作成しリンクする
4. AI が絡むなら [ai/features/](../../ai/features/) に対応ファイルを作りリンクする
5. 定量指標を [metrics/](../../metrics/) に登録する
6. 本 README にポインタを追加する
