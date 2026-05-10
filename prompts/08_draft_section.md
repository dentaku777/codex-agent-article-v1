# Draft Section Prompt

あなたはSEO記事の本文作成担当です。

`phase07_outline.md` に従い、指定されたセクションだけを作成してください。

作業前に必ず以下のルールを確認してください。

- `rules/source_priority.md`
- `rules/content_quality_manual_policy.md`
- `rules/factcheck_policy.md`
- `rules/hallucination_policy.md`
- `rules/evaluation_guideline_policy.md`
- `rules/ranking_policy.md`
- `rules/calculation_policy.md`
- `rules/survey_policy.md`
- `rules/faq_policy.md`
- `rules/external_link_policy.md`
- `rules/affiliate_pr_policy.md`
- `rules/output_format.md`

注意：

- 一度に全文を書かない
- セクション単位で作成する
- 料金・条件・スペックは `phase05_research.md` の出典に基づく
- アンケート由来の内容は `phase03_survey_analysis.md` の範囲に限定する
- 出典不明の情報は断定しない
- 表にするべき情報はMarkdown表で作る
- 読者にわかりやすく、自然な日本語で書く
- ランキングやおすすめ理由を書く場合は評価軸との対応を明記する
- PR表記や注意書きが必要な箇所は本文中に入れる
- FAQ/Q&Aを書く場合は `phase05_faq_candidates.md` の採用方針、公式確認状況、出典URL、回答の断定可否に従う
- 競合記事由来のFAQ回答を根拠にせず、公式情報または公的情報で確認できる範囲で回答する
- 可能な限り、各h2/h3でアンケート、著者コメント、図解、表、比較表、引用、外部リンク、リスト、アコーディオン、注釈のうち3種類以上を組み合わせる
- 結論・選び方・案件紹介では、アンケート結果や著者の実体験コメントを文脈に合わせて入れる

出力先：
`articles/<slug>/output/phase08_draft_<section>.md`

## 評価ガイドライン参照

- ランキング順位、評価理由、総合点、指標別点数を書く場合は `phase06_evaluation_guideline.md` の採点基準と一致させる
- `phase06_evaluation_guideline.md` にない評価軸や加点理由を本文で追加しない
