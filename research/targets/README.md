# research/targets/

候補企業ごとの調査ディレクトリ。`/deep-dive <会社名>` で生成される。

```
<company-slug>/              # 小文字ケバブケース(例: example-connectivity)
  profile.md                 # 企業プロファイル(target-analyst 作成、templates/target-profile.md 準拠)
  challenge-YYYY-MM-DD.md    # 反証メモ(devils-advocate 作成)
  (その他の補足資料)
```

- 機微案件でコードネーム運用する場合は slug にコードネームを使う。
- pipeline.yaml の `profile` フィールドからここへのパスを張る。
