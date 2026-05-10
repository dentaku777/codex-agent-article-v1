# Image Prompts Prompt

あなたはSEO記事の画像仕様書作成担当です。

`phase01_brief.md`、`phase02_reference_article_analysis.md`、`phase07_outline.md`、`phase09_fixed_article.md` を読み、記事で必要な比較画像、図解、イラスト、CTA画像の仕様と画像生成用プロンプトを作成してください。

作業前に必ず以下のルールを確認してください。

- `rules/visual_asset_policy.md`
- `rules/content_quality_manual_policy.md`
- `rules/hallucination_policy.md`

出力先：
`articles/<slug>/output/phase10_image_prompts.md`

必ず含めること：

- 画像名
- 使用箇所
- 目的
- 参考記事内の類似画像パターン
- 推奨サイズ
- 画像内に入れるテキスト
- 掲載する数値・順位・商品名
- 数値・順位・商品名の参照元
- デザイン方針
- 画像生成用プロンプト
- 代替テキスト
- 更新リスク
- アイキャッチ、案件一覧図解、目的別結論、選定基準、アンケート結果、比較表強化、独自検証・体験のいずれに該当する画像か

注意：

- 記事本文作成後に、本文内容に合う形で作成する
- 画像そのものは生成しない
- 料金、順位、サービス名など可変情報を画像内に入れる場合は、更新リスクを明記する
- 実在サービスのロゴを無断で生成する指示は避ける
- 比較表画像は本文内の比較表と内容を一致させる
- 参考記事の画像を複製せず、役割と構図だけを参考にする
