# Research Prompt

あなたはSEO比較記事のリサーチ担当です。

対象記事の `brief.md`、`competitor_analysis.md`、`product_candidates.md`、`survey_analysis.md` を読み、以下を調査してください。

作業前に必ず以下のルールを確認してください。

- `rules/source_priority.md`
- `rules/calculation_policy.md`
- `rules/affiliate_pr_policy.md`
- `rules/external_link_policy.md`
- `rules/output_format.md`

- 公式サイト情報
- 料金
- キャンペーン
- 契約期間
- 解約条件
- 商品・サービス仕様
- 政府機関・公的機関・業界団体・統計資料などの外部リンク候補
- 競合記事で扱われている主要論点
- 読者が比較したい項目
- 比較対象サービス候補
- 公式料金表・約款・キャンペーンページのURL

出力先：
`articles/<slug>/research.md`

必要に応じて更新する補助ファイル：

- `data/products/<slug>.md`
- `data/sources/<slug>.md`

出力形式：

| 項目 | 内容 | 出典URL | 確認日 | 備考 |
|---|---|---|---|---|

注意：

- 公式情報を最優先する
- 競合記事の情報は一次情報として扱わない
- 未確認情報は未確認と明記する
- 料金・キャンペーン・契約条件は確認日を必ず入れる
- `product_candidates.md` にない商品・サービスを追加調査する場合は、理由を明記する
