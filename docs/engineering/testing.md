---
title: テスト戦略 — Good/Bad データセットと Playwright UI/UX
purpose: 機能の正しさを「Good/Bad データセット × 期待 output × DS 評価指標」で検証する原則
when_to_read: 新機能のテスト計画を作る前、既存テストを改修する前
keywords: [テスト, Good/Bad, Playwright, eval, データサイエンス, UI, UX]
---

# テスト戦略

## 原則 (CONSTITUTION 第6条)

1. **データセット作成**: Good / Bad の事例を必ず両方そろえる
2. **Output 定義**: データセットに対する期待 output を文書化
3. **評価指標設計**: output を **データサイエンス的に評価** できる指標を設計
4. **継続更新**: 仕様書・データ・指標を Update しながら開発する

## レイヤ別の運用

### ロジック / API
- Good/Bad 入力 → 期待 output（JSON など）
- 指標例: precision / recall, exact match, JSON schema 準拠率, レイテンシ p95

### UI / UX
- Playwright によるシナリオテストで **Good 挙動 / Bad 挙動** を定義する
  - **Good**: ユーザがゴールに到達するまでクリック数・離脱なし
  - **Bad**: 離脱地点・誤操作・モーダル詰まりなどを再現する
- 指標例: ステップ完了率、平均所要時間、Bad シナリオ再現の検出率
- Playwright スクリプトは実装側に置き、データセットメタは [`datasets/`](./datasets/) に置く

### AI 出力
- [ai/evals/](../ai/evals/) を参照（rubric ベースの eval）
- ハルシネーション率・rubric 準拠率を主指標とする

## データセットの置き場

- データセット本体: `datasets/<dataset-name>.md`（メタ） + 実データは `datasets/<dataset-name>/` に格納
- 機能仕様 (`product/features/<name>.md`) からリンクする

## 仕様書 Update のリズム

- 実装 PR ごとに dataset と仕様書も同じ PR で更新する
- 「あとで書く」を許さない（残らないため）
- DS 指標が変わったら `metrics/` の該当ファイルも更新する
