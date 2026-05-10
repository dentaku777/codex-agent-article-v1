# Comparison Review Policy

フェーズ7の構成作成後とフェーズ9の記事内容Fix後に、競合記事および常設制作標準との差分を比較検証する。

## フェーズ7: 構成比較検証

入力:

- `articles/<slug>/output/phase07_outline.md`
- `articles/<slug>/output/phase02_competitor_analysis.md`
- `xx.memo/manual/manual.md`
- `rules/content_quality_manual_policy.md`
- `articles/<slug>/output/phase02_reference_article_analysis.md`（追加参考記事がある場合）
- `articles/<slug>/output/phase03_survey_analysis.md`（ある場合）
- `articles/<slug>/output/phase04_x_post_research.md`（実施した場合）
- `articles/<slug>/output/phase06_evaluation_guideline.md`

出力:

- `articles/<slug>/output/phase07_outline_comparison_review.md`

検証観点:

- 競合記事と比べた優位性、独自性、網羅性
- 常設制作標準と比べて不足している導入、比較表、体験・一次情報風の見せ方、結論ファースト、目的別導線
- 評価ガイドラインと見出し構成の整合性
- FAQ、選び方、注意点、CTAの過不足

## フェーズ9: Fix後記事比較検証

入力:

- `articles/<slug>/output/phase09_fixed_article.md`
- `articles/<slug>/output/phase09_factcheck_report.md`
- `articles/<slug>/output/phase09_truthcheck_report.md`
- `articles/<slug>/output/phase02_competitor_analysis.md`
- `xx.memo/manual/manual.md`
- `rules/content_quality_manual_policy.md`
- `articles/<slug>/output/phase06_evaluation_guideline.md`
- `articles/<slug>/output/phase05_research.md`
- `articles/<slug>/output/phase03_survey_analysis.md`（ある場合）
- `articles/<slug>/output/phase04_x_post_research.md`（実施した場合）

出力:

- `articles/<slug>/output/phase09_final_article_comparison_review.md`

検証観点:

- SEO観点: 検索意図充足、見出し網羅性、比較表、FAQ、内部導線、外部リンク妥当性
- AIO観点: 結論の明確さ、根拠の明示、要約しやすい構造、比較軸の一貫性
- 競合記事と比べた独自性、説得力、情報鮮度
- 常設制作標準との一致
- 事実・数値・順位がチェック結果と矛盾していないか

## 出力形式

- 直接 `phase07_outline.md` または `phase09_fixed_article.md` を修正しない
- 修正が必要な場合は、Markdown形式で改善案を出す
- 各改善案には「対象箇所」「問題点」「改善内容」「優先度」「反映時の注意」を含める
