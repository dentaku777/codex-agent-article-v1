# Output Format

記事制作時の各成果物は、後工程で参照しやすい形式に揃える。

## 成果物命名規則

- 各フェーズの成果物は、原則として `articles/<slug>/output/` 直下へ保存する
- ファイル名には、どのフェーズの成果物か分かるように `phaseXX_` 接頭辞を付ける
- 例: `phase01_brief.md`, `phase02_competitor_targets.md`, `phase02_competitor_analysis.md`, `phase03_survey_analysis.md`
- Claude CLIレビューなど複数フェーズにまたがる補助ログは `phase_meta_` 接頭辞を使う

## 文字コード

- 成果物は `rules/encoding_policy.md` に従い、UTF-8で保存する
- PowerShellなどでファイルを書き込む場合は、文字コード指定を省略しない

## phase05_research.md

- 公式情報、料金、キャンペーン、契約条件、仕様を表で管理する
- 各行に出典URLと確認日を入れる
- 未確認情報は `未確認` と書く
- Webフェッチや検索APIを使った場合は、確認に使った直接URL、確認日、取得対象が公式ページか一次情報かを備考に残す

## phase02_reference_article_analysis.md

- 参考記事の構成、記事内容、比較表、ランキング、画像、CTA、FAQの型を記録する
- 本文や画像は流用せず、汎用パターンに抽象化する

## phase02_competitor_analysis.md

- 競合記事ごとに、URL、見出し構成、比較軸、ランキング基準、強み、弱みを記録する
- 指定キーワードおよび類似キーワードで上位表示される記事20件を対象にする
- 同一ドメイン重複と商品・サービス公式サイトは除外する
- 上位5位の記事は `優先度：高` として扱う
- 記事構成、記事内容、推定文字数、優位性・独自性、SEO観点、AIO観点を記録する
- 外部リンクの有無、外部リンク先の種類、政府機関・公的機関へのリンク有無を記録する
- 競合情報は一次情報ではないことを明記する

## phase03_survey_analysis.md

- アンケート概要、回答者属性、回答数、実施時期、設問、主要回答を記録する
- 読者ニーズ、比較軸、満足点、不満点、FAQ候補、ランキング評価軸への反映案を記録する
- アンケート条件が不明な場合は `未確認` と書く

## phase02_competitor_targets.md

- 競合記事20件の収集リストを記録する
- 検索キーワード、検索順位、タイトル、URL、ドメイン、採用/除外、除外理由を入れる
- 同一ドメイン重複、公式サイト除外の判断理由を残す
- 検索日時、検索手段、検索クエリを記録する

## phase05_selected_products.md

- 記事内で評価する商品・サービスの確定リストを記録する
- 競合記事での紹介数、上位5記事での紹介有無、選定理由、公式確認の必要項目を入れる
- phase07_outline.md 作成前に確定する

## phase06_evaluation_guideline.md

- `phase05_selected_products.md` 確定後、`phase07_outline.md` 作成前に作成する
- 評価指標、各20点満点の採点基準、総合評価100点満点の計算式、同点時の順位決定ルールを記録する
- 評価指標は原則5つとし、商材特性に応じてユーザー指定または競合分析・アンケート・公式情報から提案する
- PDF化はMarkdown確認後に行い、`phase06_evaluation_guideline.pdf` として保存する

## phase02_product_candidates.md

- 競合分析から抽出した商品・サービス候補を記録する
- 競合記事での紹介数、上位5記事での紹介有無、候補理由、公式確認の必要項目を入れる
- phase05_research.md と phase05_selected_products.md の前工程として扱う

## phase07_outline.md

- h2/h3、各見出しの役割、想定文字数、必要な表、必要な画像、参照すべき出典、アンケート反映箇所、外部リンク候補を入れる
- 本文は書かない

## phase08_draft_<section>.md

- 1ファイル1セクションを原則にする
- 冒頭に対象見出しと参照したresearch項目を書く

## phase08_merged_article.md

- outlineの順に結合する
- ファクトチェック前のため最終成果物にしない

## phase09_fixed_article.md

- phase09_factcheck_report.mdの指摘反映後の本文
- テンプレート変換はこのファイルを対象にする

## phase09_truthcheck_report.md

- 成果物全体の真偽、根拠不足、ハルシネーションの有無を記録する
- 判定、根拠、対応方針を残す

## phase_meta_claude_review_notes.md

- Claude CLI二次チェックを実施した工程、確認日、依頼プロンプト、Claude回答の要約、Codexでの反映判断を記録する
- Claude回答は補助的なレビュー結果として扱い、一次情報や公式情報の代替にしない
- 反映しない指摘がある場合は、理由を短く残す

## phase10_image_prompts.md

- 画像仕様書と画像生成用プロンプトを記録する
- 使用箇所、目的、サイズ、画像内テキスト、参照元、更新リスク、代替テキストを入れる

## phase11_*_blocks.html

- WordPressブロックエディタ投入用コードを記録する
- 現状の標準出力は `output/phase11_swell_blocks.html`
- SWELL以外のテンプレートを指定する場合は `output/phase11_<template>_blocks.html` とする
