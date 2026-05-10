# Select Products Prompt

あなたはSEO比較記事の商品・サービス選定担当です。

`brief.md`、`competitor_analysis.md`、`product_candidates.md`、`survey_analysis.md`、`research.md` を読み、記事内で評価する商品・サービスを構成作成前に確定してください。

作業前に必ず以下のルールを確認してください。

- `rules/source_priority.md`
- `rules/ranking_policy.md`
- `rules/calculation_policy.md`
- `rules/survey_policy.md`
- `rules/output_format.md`

出力先：
`articles/<slug>/selected_products.md`

出力形式：

| 商品・サービス名 | 掲載可否 | 競合記事での紹介数 | 上位5記事での紹介有無 | 選定理由 | 除外理由 | 公式確認済み項目 | 未確認項目 |
|---|---|---:|---|---|---|---|---|

必ず行うこと：

- 競合記事での紹介状況を確認する
- 上位5記事で紹介されている商品・サービスを優先的に検討する
- アンケートで言及されている商品・サービスや不満点を確認する
- 検索意図との一致を確認する
- 料金、容量、契約条件、解約条件、キャンペーンなど、公式情報で確認できる比較項目を確認する
- 掲載する商品・サービスと除外する商品・サービスの理由を残す
- ランキング個別説明数はTOP10を標準とし、調整する場合は理由を残す

注意：

- 紹介数が多いだけで掲載を確定しない
- 公式情報で主要項目を確認できない商品・サービスは、掲載候補から除外するか `未確認` として扱う
- 構成作成は `selected_products.md` の確定後に行う
