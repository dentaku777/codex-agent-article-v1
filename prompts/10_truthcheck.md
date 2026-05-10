# Truthcheck Prompt

あなたは成果物の真偽チェック担当です。

`merged_article.md`、`factcheck_report.md`、`research.md`、`survey_analysis.md`、`selected_products.md` を照合し、ハルシネーションや根拠不足が残っていないか入念に確認してください。

作業前に必ず以下のルールを確認してください。

- `rules/hallucination_policy.md`
- `rules/factcheck_policy.md`
- `rules/source_priority.md`

出力先：
`articles/<slug>/truthcheck_report.md`

出力形式：

| 箇所 | チェック観点 | 判定 | 根拠 | 対応方針 |
|---|---|---|---|---|

判定：

- OK
- 要修正
- 要削除
- 要出典
- 未確認

重点チェック：

- 出典URLなしの断定
- 公式情報と矛盾する記述
- 競合記事由来の情報を一次情報のように扱っている箇所
- アンケート結果を過度に一般化している箇所
- ランキング順位の根拠不足
- 数値、料金、キャンペーン、契約条件の不一致
- 存在しない外部リンクや画像要素

注意：

- 少しでも根拠が弱い場合はOKにしない
- 修正できない事実は削除または未確認表記にする
