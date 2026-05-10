# codex-agent-article-v1

Codexを使ってSEO比較記事・レビュー記事・ランキング記事を制作するためのプロジェクトです。

## 基本フロー

詳細な作業フローと直列・並列工程の可視化は [docs/article_workflow.md](docs/article_workflow.md) を参照してください。

1. 開始時にSEO上位表示を狙う主キーワードを指定
2. `articles/<slug>/output/phase01_brief.md` を作成
3. 参考記事の構成・内容・画像・CTAを分析
4. 指定キーワードと類似キーワードで競合記事20件を収集
5. 競合分析
6. 利用者アンケート分析
7. 公式情報リサーチ
8. 競合記事、公式FAQ、アンケート、検索意図からFAQ/Q&A候補を抽出し、採用方針を決定
9. 競合紹介状況、アンケート、公式情報を踏まえて、記事内で評価する商品・サービスを決定
10. 評価ガイドラインをMarkdownで作成し、確認後にPDF化
11. 記事構成作成
12. セクション別本文作成
13. 本文結合
14. ファクトチェック
15. 成果物全体の真偽チェック
16. ファクトチェック結果に基づき修正
17. 画像仕様書・画像プロンプト作成
18. テンプレート変換。現状はSWELLブロック変換
19. WordPressへ手動投入

必要に応じて、重要工程の区切りでClaude CLIによる二次チェックを挟みます。CodexはClaude CLIへ貼り付ける確認プロンプトを作成し、ユーザーがClaude MaxプランのCLIで手動実行します。Claude APIの自動呼び出しは原則行いません。

## 主要フォルダ

- `articles/`: 記事ごとの作業フォルダ。各フェーズの成果物は `articles/<slug>/output/phaseXX_...` 形式で保存する
- `prompts/`: Codexへの作業指示
- `rules/`: 記事制作・ファクトチェック・評価・テンプレート変換ルール
- `scripts/`: 自動化スクリプト
- `data/`: 商品・競合・出典データ
- `assets/`: 共通素材
- `xx.memo/`: 検証用メモ・サンプル

## 主要ルール

- 料金・キャンペーン・契約条件は公式情報を最優先する
- 原則としておすすめランキング記事として制作する
- `xx.memo/manual.docx` の制作ノウハウは `rules/content_quality_manual_policy.md` に反映済み。構成・本文・画像仕様では体験、一次情報、独自情報、結論ファースト、目的別導線を重視する
- ランキング個別説明はTOP10までを標準とする
- 評価対象の商品・サービス確定後、構成作成前に評価ガイドラインを作成する
- 評価ガイドラインは原則5指標、各20点満点、総合100点満点とする
- 評価指標はユーザー指定を優先し、指定がない場合は競合分析・アンケート・公式情報から提案する
- ランキング順位、評価点、比較表の数値は根拠と計算式を残す
- 利用者アンケートがある場合は、構成作成前に分析して読者ニーズと比較軸へ反映する
- FAQ/Q&Aは `rules/faq_policy.md` に従い、競合記事で頻出する疑問、公式サイト上のFAQ・サポート情報、アンケート上の不安、検索意図から候補化し、構成作成前に採用可否と出典要件を決める
- 政府機関・公的機関などの外部リンク候補と、競合記事の外部リンク状況を確認する
- Web検索・Webフェッチ・検索API連携は `rules/web_fetch_policy.md` に従い、検索結果と公式確認済み情報を混同しない
- ランキングは `rules/ranking_policy.md` と `rules/evaluation_guideline_policy.md` に従って根拠を残す
- 実質月額は `rules/calculation_policy.md` に従って計算する
- 真偽チェックは `rules/hallucination_policy.md` に従って入念に行う
- Claude CLI二次チェックは `rules/claude_cli_review_policy.md` に従う。API課金を避けるため、原則として手動CLI運用に限定する
- PR表記や広告リンクは `rules/affiliate_pr_policy.md` に従う
- テンプレート変換は `rules/template_parse_policy.md` に従う。現状はSWELLを標準テンプレートとする
- SWELL変換では `rules/swell_custom_patterns.md` を優先し、未定義装飾は推測しない
