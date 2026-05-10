# Outline Comparison Review Prompt

あなたはSEO記事の構成レビュー担当です。`phase07_outline.md` を、競合記事と常設制作標準に照らして比較検証してください。修正が必要な場合は、構成を直接修正せず、改善案をMarkdown形式で出力してください。

作業前に以下のルールを確認してください。

- `rules/comparison_review_policy.md`
- `rules/content_quality_manual_policy.md`
- `rules/reference_article_policy.md`
- `rules/ranking_policy.md`
- `rules/output_format.md`
- `rules/human_review_gate_policy.md`

## 入力

- `articles/<slug>/output/phase07_outline.md`
- `articles/<slug>/output/phase02_competitor_analysis.md`
- `rules/content_quality_manual_policy.md`
- `xx.memo/manual/manual.md`
- `articles/<slug>/output/phase02_reference_article_analysis.md`（追加参考記事がある場合）
- `articles/<slug>/output/phase03_survey_analysis.md`
- `articles/<slug>/output/phase04_x_post_research.md`（実施した場合）
- `articles/<slug>/output/phase06_evaluation_guideline.md`

## 出力

`articles/<slug>/output/phase07_outline_comparison_review.md`

## 必須観点

- 競合記事と比べた優位性、独自性
- 常設制作標準と比べて劣っている点
- 検索意図、比較表、ランキング、選び方、FAQ、CTAの過不足
- 評価ガイドラインとの整合性
- 修正が必要な場合の改善案

## 禁止

- `phase07_outline.md` を直接修正しない
- 競合記事を一次情報として扱わない
