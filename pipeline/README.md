# パイプライン運用ルール

`pipeline.yaml` が案件管理の単一の情報源(single source of truth)。**変更は deal-desk エージェント経由のみ**(単一書き手の原則。手動編集した場合は次回の health チェックで整合性を検証すること)。

## ステージ定義

| ステージ | 名称 | 内容 | 入口条件 | 停滞閾値 |
|---|---|---|---|---|
| `00_sourcing` | ソーシング | ロングリスト。発掘したばかりの候補 | ピラー該当 + 注目理由の記録 | なし(棚卸しは四半期毎) |
| `10_screening` | スクリーニング | 初期評価中 | 簡易調査に値すると判断 | 21日 |
| `20_deep_dive` | 詳細調査 | プロファイル作成・スコアリング・反証 | スコアカード適用開始 | 14日 |
| `30_outreach` | コンタクト | 初期接触・関係構築 | スコア 3.2 以上 + 経営の接触承認 | 14日 |
| `40_nda` | NDA・情報交換 | NDA 締結、非公開情報での検証 | NDA 締結 | 14日 |
| `50_loi` | LOI・基本合意 | 意向表明、条件交渉 | 経営会議の推進決議 | 7日 |
| `60_dd` | デューデリジェンス | 本格 DD(外部アドバイザー含む) | LOI 締結 | 7日 |
| `70_execution` | 最終契約 | SPA 交渉、クロージング準備 | DD 完了判断 | 7日 |
| `80_pmi` | 統合 | クロージング後の統合実行 | クロージング | 30日 |
| `on_hold` | 保留 | 意図的な一時停止 | 保留理由 + 再開条件の記録 | 90日(再開判断) |
| `dropped` | 見送り | 検討終了 | 見送り理由の記録 | — |

- 停滞閾値: `history` の最終更新からの経過日数がこれを超えると deal-desk が停滞として報告する(`meta.stale_threshold_days` は全体のデフォルト値。上表が優先)。
- 30_outreach 以降への遷移は必ず人間の承認を history に記録する。エージェントが自律的に遷移させてよいのは 20_deep_dive まで。

## スキーマ

```yaml
meta:
  updated: "YYYY-MM-DD"        # deal-desk が更新時に書き換える
  stale_threshold_days: 14     # デフォルト停滞閾値

deals:
  - id: "2026-001"             # 年-連番。再利用禁止
    codename: aurora           # 機微案件はコードネーム運用(小文字1単語)
    company: "会社名"           # 実名記載の可否は案件責任者判断(機微案件は空欄可)
    type: acquisition          # acquisition | investment | partnership
    stage: "20_deep_dive"      # 上表のステージID
    priority: A                # A(最優先) / B / C
    owner: "担当者名"           # 人間の案件責任者
    thesis_pillar: "P1"        # strategy/ma-thesis.md のピラーID(P1〜P5)
    source: "発掘経路"          # 例: market-scan 2026-07, 紹介, インバウンド
    score: 3.8                 # evaluation-criteria.md の加重スコア(未評価は null)
    next_action: "次にやること" # アクティブ案件では必須
    next_action_due: "YYYY-MM-DD"
    profile: "research/targets/<slug>/profile.md"  # 作成済みの場合
    history:                   # 全イベントを日付付きで記録(新しいものを下に)
      - { date: "YYYY-MM-DD", event: "内容" }
    notes: ""                  # 自由記述
```

## 機微情報の扱い

- 交渉中・未公表の案件は `codename` のみで運用し、実名は書かない選択ができる。
- 具体的な金額・条件は、リポジトリ記載の明示的な許可がある場合のみ記録する。
- NDA 下で得た情報は出所を明記し、公開情報と混ぜない。
