# Research Prompt

あなたはSEO比較記事のリサーチ担当です。

対象記事の `phase01_brief.md`、`phase02_competitor_analysis.md`、`phase02_product_candidates.md`、`phase03_survey_analysis.md` を読み、以下を調査してください。

作業前に必ず以下のルールを確認してください。

- `rules/source_priority.md`
- `rules/web_fetch_policy.md`
- `rules/calculation_policy.md`
- `rules/affiliate_pr_policy.md`
- `rules/external_link_policy.md`
- `rules/faq_policy.md`
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
- Webフェッチで取得した公式ページ本文、PDF、重要事項説明、FAQ、サポートページ
- 公式FAQ・ヘルプ・サポート・約款・重要事項説明から確認できるQ&A候補
- 競合記事のFAQ候補に対する公式確認可否

出力先：
`articles/<slug>/output/phase05_research.md`
`articles/<slug>/output/phase05_faq_candidates.md`

必要に応じて更新する補助ファイル：

- `data/products/<slug>.md`
- `data/sources/<slug>.md`

出力形式：

| 項目 | 内容 | 出典URL | 確認日 | 備考 |
|---|---|---|---|---|

## phase05_faq_candidates.md の出力形式

| FAQ候補 | 収集元 | 競合掲載状況 | 公式確認状況 | 出典URL | 確認日 | 採用/保留/除外 | 記事内配置案 | 回答方針 | 備考 |
|---|---|---|---|---|---|---|---|---|---|

FAQ候補は、競合記事の頻出FAQ、公式サイト上のFAQ・ヘルプ・サポート、アンケートで出た不安・疑問、検索意図をもとに抽出してください。競合記事由来のFAQ回答は一次情報として扱わず、公式情報または公的情報で確認できる範囲に限定して回答方針を作成してください。

Web検索APIや検索結果ページで見つけた情報は、公式ページまたは一次情報ページを直接取得してから記録する。検索APIのスニペットだけを根拠にしない。

注意：

- 公式情報を最優先する
- 競合記事の情報は一次情報として扱わない
- 未確認情報は未確認と明記する
- 料金・キャンペーン・契約条件は確認日を必ず入れる
- FAQ/Q&Aは、回答に使える出典URLと確認日を必ず入れる
- 公式情報で回答できないFAQは、採用を保留するか、回答範囲を限定する
- `phase02_product_candidates.md` にない商品・サービスを追加調査する場合は、理由を明記する
