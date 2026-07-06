---
name: deep-dive
description: 買収・出資候補企業1社の詳細調査を実行する。target-analystによるプロファイル作成・スコアリング → devils-advocateによる反証 → 統合ビューの提示 → パイプライン反映まで。「〇〇社を調べて」「候補を深掘りして」で使用。
argument-hint: "<会社名> [追加の観点や既知情報]"
---

# 候補企業の深掘り調査(deep-dive)

指定された 1 社について、分析 → 反証 → 統合 → パイプライン反映のフルサイクルを回す。

## 手順

1. **対象確認**: 引数から会社名を特定する。`pipeline/pipeline.yaml` と `research/targets/` を確認し、既存案件なら更新モード(既存プロファイルの日付を伝える)。会社名が曖昧なら着手前にユーザーに確認する。
2. **プロファイル作成**: target-analyst エージェントを起動(subagent_type: target-analyst)。会社名、既存プロファイルの有無、ユーザーが指定した追加観点を渡す。
3. **反証**: target-analyst 完了後、devils-advocate エージェントを起動(subagent_type: devils-advocate)。作成されたプロファイルのパスを渡し、反証メモの作成を依頼する。
4. **統合ビューの提示**: 両者の結果をユーザーに報告する:
   - TL;DR(会社概要と戦略適合性)
   - 加重スコアと、devils-advocate の結論(proceed / proceed-with-conditions / stop)
   - 両者の見解が食い違う点(あれば明示。これが最も価値のある情報)
   - 推奨ネクストアクション
5. **パイプライン反映**: ユーザーの同意を得て deal-desk エージェントで反映する:
   - 未登録なら新規案件として追加(ステージはスコアに応じて 00_sourcing または 10_screening)
   - 登録済みなら score / next_action / history を更新

## 注意

- 手順 2 と 3 は直列(反証はプロファイルを読む必要がある)。
- スコアが `strategy/evaluation-criteria.md` の見送り基準(3.2 未満)やキルクライテリアに該当する場合も、判断はユーザーに委ねる。エージェントの推奨は判断材料であり決定ではない。
