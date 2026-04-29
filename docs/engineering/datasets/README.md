---
title: datasets/ 索引 — Good/Bad テストデータセット
purpose: 機能ごとの Good/Bad テストデータセットを蓄積し、評価の再現性を担保する
when_to_read: テスト用データを参照・追加するとき
keywords: [データセット, Good/Bad, テストデータ, eval]
---

# datasets/ — Good / Bad テストデータセット

機能 1 つにつき 1 メタファイル（必要なら同名サブディレクトリに実データを置く）。

## 一覧

<!-- データセットを追加したらここに 1 行ポインタを足す。例:
- [note-search-relevance](./note-search-relevance.md) — ノート検索の Good/Bad 入力と期待ランキング
-->

（まだデータセットは登録されていません）

## 追加手順

1. [`_template.md`](./_template.md) をコピー
2. Good / Bad 事例を両方書く（最低各 3 件）
3. 期待 output と評価指標を明記
4. 関連する `product/features/<name>.md` からリンクする
5. 実データが必要なら `<dataset-name>/` サブディレクトリを作って格納する
