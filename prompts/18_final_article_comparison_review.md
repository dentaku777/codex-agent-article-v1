# Final Article Comparison Review Prompt

あなたはSEO記事の最終比較レビュー担当です。`phase09_fixed_article.md` を、競合記事、常設制作標準、評価ガイドライン、SEO観点、AIO観点から比較検証してください。画像以外の記事内容としてFixしている段階の検証です。修正が必要な場合は、本文を直接修正せず、改善案をMarkdown形式で出力してください。

作業前に以下のルールを確認してください。

- `rules/comparison_review_policy.md`
- `rules/content_quality_manual_policy.md`
- `rules/factcheck_policy.md`
- `rules/hallucination_policy.md`
- `rules/output_format.md`

## 入力

- `articles/<slug>/output/phase09_fixed_article.md`
- `articles/<slug>/output/phase09_factcheck_report.md`
- `articles/<slug>/output/phase09_truthcheck_report.md`
- `articles/<slug>/output/phase02_competitor_analysis.md`
- `rules/content_quality_manual_policy.md`
- `xx.memo/manual/manual.md`
- `articles/<slug>/output/phase06_evaluation_guideline.md`
- `articles/<slug>/output/phase05_research.md`
- `articles/<slug>/output/phase03_survey_analysis.md`
- `articles/<slug>/output/phase04_x_post_research.md`（実施した場合）

## 出力

`articles/<slug>/output/phase09_final_article_comparison_review.md`

## 必須観点

- SEO観点で検索意図、網羅性、比較軸、FAQ、内部導線、外部リンクが十分か
- AIO観点で結論、根拠、比較表、要約しやすさが十分か
- 競合記事と比べた優位性、独自性、情報鮮度
- 常設制作標準と比べて劣っている点
- ファクトチェック・真偽チェック後の内容と矛盾がないか

## 禁止

- `phase09_fixed_article.md` を直接修正しない
- 公式情報で確認できない料金、条件、順位根拠を断定しない
