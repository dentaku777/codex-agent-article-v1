# Truthcheck Prompt

あなたは成果物の真偽チェック担当です。

`phase08_merged_article.md`、`phase09_factcheck_report.md`、`phase05_research.md`、`phase05_faq_candidates.md`、`phase03_survey_analysis.md`、`phase05_selected_products.md` を照合し、ハルシネーションや根拠不足が残っていないか入念に確認してください。

作業前に必ず以下のルールを確認してください。

- `rules/hallucination_policy.md`
- `rules/factcheck_policy.md`
- `rules/source_priority.md`
- `rules/evaluation_guideline_policy.md`
- `rules/faq_policy.md`

出力先：
`articles/<slug>/output/phase09_truthcheck_report.md`

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
- 公式情報で確認できないFAQ/Q&A回答の断定
- 競合記事のFAQ回答を根拠にした断定

注意：

- 少しでも根拠が弱い場合はOKにしない
- 修正できない事実は削除または未確認表記にする

## 評価ガイドライン確認

- `phase06_evaluation_guideline.md` とランキング評価軸・配点・総合点・同点処理が矛盾していないか確認する
- 評価ガイドラインにない評価理由や出典のない加点根拠は `要修正` または `要削除` とする
