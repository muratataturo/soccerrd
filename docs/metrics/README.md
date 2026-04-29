---
title: metrics/ 索引 — 横断的な定量評価指標
purpose: 機能・組織横断で追う KPI と、それぞれの測定方法を集約する
when_to_read: 機能の成功条件・KPI を定義するとき、ダッシュボードを作るとき
keywords: [metric, KPI, 定量評価, ダッシュボード, North Star]
---

# metrics/ — 定量評価指標台帳

CONSTITUTION 第5条で要求される「すべての項目を数値で評価できる」状態を担保するための台帳。

## 一覧

<!-- 指標を追加したらここに 1 行ポインタを足す。例:
- [weekly-note-edit-rate](./weekly-note-edit-rate.md) — 週次アクティブノート編集率（retention 主指標）
-->

（まだ指標は登録されていません）

## 階層

| 階層 | 例 | 置き場 |
| --- | --- | --- |
| North Star | 月間アクティブサッカーNote 数 | 本ディレクトリ |
| ペルソナ別 | コーチの組織知還元率 | 本ディレクトリ |
| 機能別 | ノート検索クリック→保存転換率 | 本ディレクトリ + `product/features/<name>.md` |
| AI 別 | rubric 準拠率・ハルシネーション率 | 本ディレクトリ + `ai/evals/` |

## 追加手順

1. [`_template.md`](./_template.md) をコピー
2. 何の判断に使うかを明記する（決定不能な指標は登録しない）
3. ベースライン・目標・測定方法・観測ダッシュボードを書く
4. 関連 `product/features/<name>.md` または `ai/features/<name>.md` からリンク
