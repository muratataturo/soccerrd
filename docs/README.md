---
title: docs ナビゲーション索引
purpose: docs/ の構造とそれぞれのフォルダ・ファイルの目的を一望し、目的に応じたファイルへ最短で到達するための索引
when_to_read: docs/ にあるドメイン知識を検索する最初のエントリ
keywords: [索引, ナビゲーション, 構造, memory, domain knowledge]
---

# docs/ — プロジェクト・ドメイン知識の永続メモリ

このディレクトリはプロダクト「soccerrd」のドメイン知識を、職能別に蓄積するための永続メモリです。
**最初に [CONSTITUTION.md](./CONSTITUTION.md) を読み**、その上で目的に合わせたサブディレクトリへ移動してください。

## ディレクトリ構造

| パス | 何を保持するか | いつ読むか |
| --- | --- | --- |
| [CONSTITUTION.md](./CONSTITUTION.md) | プロダクト憲法（最上位の判断基準） | あらゆる意思決定の前に必読 |
| [product/](./product/) | プロダクト戦略・ペルソナ・優先度・機能仕様 | 何を作るか・なぜ作るかを判断するとき |
| [engineering/](./engineering/) | アーキテクチャ・テスト・技術判断 | どう実装・検証するかを判断するとき |
| [research/](./research/) | 競合調査・マーケット分析 | 競合劣位・差別化を判断するとき |
| [ai/](./ai/) | AI 機能・プロンプト・eval | サッカーNote をはじめ AI 機能を作るとき |
| [metrics/](./metrics/) | 横断的な定量評価指標 | KPI・成功指標を定義するとき |

## 検索のヒント

- **「機能 X を実装したい」** → `product/features/` で仕様 → `engineering/` で実装方針 → `ai/` で AI 連携 → `metrics/` で評価指標
- **「競合 Y との差は」** → `research/competitors/`
- **「テストデータをどう作る」** → `engineering/testing.md` と `engineering/datasets/`
- **「プロンプトの eval」** → `ai/evals/`

## ファイル名規約

- 各ディレクトリの先頭は `README.md`（索引）
- テンプレートは `_template.md`（先頭アンダースコアでソート時上位、検索時に弾きやすい）
- 機能・競合・eval などインスタンス文書は `kebab-case.md`（例: `note-search.md`, `hudl.md`, `note-ranking-eval.md`）

## 更新規約

- 新規機能を着手する前に `product/features/<name>.md` を作成し、Constitution と紐付ける
- 学びが得られたら必ずどこかのファイルへ反映する（口頭知識を残さない）
- ファイルを追加したら該当 `README.md` へ 1 行ポインタを足す
- 既存ファイルを更新できる場合は新規作成しない（重複は誤判断の温床）
