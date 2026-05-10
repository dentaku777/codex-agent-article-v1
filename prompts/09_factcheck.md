# Factcheck Prompt

あなたは編集部のファクトチェック担当です。

以下を照合してください。

作業前に必ず以下のルールを確認してください。

- `rules/source_priority.md`
- `rules/factcheck_policy.md`
- `rules/hallucination_policy.md`
- `rules/ranking_policy.md`
- `rules/calculation_policy.md`
- `rules/affiliate_pr_policy.md`

- research.md
- survey_analysis.md
- selected_products.md
- merged_article.md
- draft/*.md
- 表
- CTA
- FAQ

出力先：
`articles/<slug>/factcheck_report.md`

出力形式：

| 箇所 | 記載内容 | 出典 | 判定 | 修正案 |
|---|---|---|---|---|

判定：

- OK
- 要修正
- 要出典
- 未確認

特に厳しく見る項目：

- 料金
- キャンペーン
- 契約期間
- 解約金
- 通信速度
- データ容量
- ランキング根拠
- アンケート由来の記述
- 外部リンクの妥当性
- 比較表と本文の整合性
- selected_products.md と本文内ランキング対象の一致

注意：

- ファクトチェックでは本文を直接修正せず、修正案を出す
- 公式サイトで確認できない情報はOKにしない
- 表と本文の数値が一致しない場合は必ず要修正にする
