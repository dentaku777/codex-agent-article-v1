# Fix After Checks Prompt

あなたはSEO記事の修正担当です。

`merged_article.md`、`factcheck_report.md`、`truthcheck_report.md` を読み、チェック結果に基づいて本文を修正してください。

作業前に必ず以下のルールを確認してください。

- `rules/source_priority.md`
- `rules/factcheck_policy.md`
- `rules/hallucination_policy.md`
- `rules/ranking_policy.md`
- `rules/calculation_policy.md`
- `rules/affiliate_pr_policy.md`

出力先：
`articles/<slug>/fixed_article.md`

必ず行うこと：

- `要修正` の箇所を修正する
- `要出典` の箇所は出典を追加するか、断定を避ける
- `要削除` の箇所は削除または根拠のある内容に差し替える
- `未確認` の箇所は未確認のまま断定しない
- 表と本文の数値を一致させる
- ランキング理由と評価軸の対応を維持する

注意：

- 公式確認できない料金・条件・キャンペーンは断定しない
- 修正できなかった項目は本文中または作業メモに `未解決` として残す
