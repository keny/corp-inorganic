---
name: pipeline
description: M&Aパイプラインの確認・更新を行う。案件の状況一覧、新規案件の追加、ステージ変更、進捗更新、停滞案件のチェック。「案件の状況は?」「〇〇をNDAステージに進めて」「新しい案件を登録して」で使用。
argument-hint: "[status | add <会社名> | update <案件ID> | health]"
---

# パイプライン管理

`pipeline/pipeline.yaml` に対する参照・更新を deal-desk エージェント経由で行う。

## サブコマンド(引数なしの場合は status)

- **status**: ステージ別サマリー、優先案件、今週の next_action 一覧を表示
- **add <会社名>**: 新規案件の登録。登録前に重複確認。必須フィールド(type, stage, owner, thesis_pillar, next_action)が埋まるようユーザーから不足情報を聞き取る
- **update <案件ID or コードネーム>**: ステージ遷移・フィールド更新。変更内容を history に記録
- **health**: 鮮度チェック(停滞案件)、next_action 欠落、整合性エラーの一覧と推奨対応

## 手順

1. 引数を解釈し、deal-desk エージェント(subagent_type: deal-desk)に具体的な指示を渡して起動する。
2. 結果をユーザーに報告する。更新系の場合は変更差分を明示する。
3. health で問題が出た場合、そのまま修正まで行うかユーザーに確認して deal-desk で対応する。

## 注意

- pipeline.yaml をメインセッションで直接編集しない。必ず deal-desk 経由(単一書き手の原則)。
- 案件の削除は行わない。見送りは dropped ステージへの遷移として扱う。
