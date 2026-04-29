---
title: engineering/ 索引 — どう実装・検証するか
purpose: 実装方針・テスト戦略・アーキテクチャ判断を集約する
when_to_read: 実装方法・テスト方法・依存技術を判断する前
keywords: [エンジニアリング, アーキテクチャ, テスト, ADR, Good/Bad, Playwright]
---

# engineering/ — 実装と検証

CONSTITUTION 第6条「Good / Bad データセット駆動の開発プロセス」を運用するためのフォルダ。

## ファイル

| パス | 用途 |
| --- | --- |
| `README.md` | 本ファイル — 索引・原則 |
| [`testing.md`](./testing.md) | Good/Bad データセット運用方針・Playwright による UI/UX テスト |
| [`datasets/`](./datasets/) | Good/Bad テストデータセットの実体と管理 |
| [`decisions/`](./decisions/) | アーキテクチャ判断記録 (ADR) |

## 開発プロセスの原則

1. 機能仕様 (`product/features/<name>.md`) があるか確認する
2. Good/Bad データセットを `datasets/` に登録する
3. 期待 output と DS 評価指標を定義する
4. 実装と並行して **仕様書・データセット・ADR を常に Update**する
5. リリース後、`metrics/` の指標で評価しサイクルを回す

## アーキテクチャ判断は ADR に残す

- ライブラリ選定・データモデル変更・外部 API 採用など、**後戻りしづらい判断**は必ず [`decisions/`](./decisions/) に残す
- 口頭・チャットで決めたまま放置しない
