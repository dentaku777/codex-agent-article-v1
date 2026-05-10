# Claude CLI Review Policy

Claude CLIは、記事制作における補助的な二次チェックとして使う。Claude APIの自動呼び出しは原則行わず、ユーザーがClaude Maxプランで認証済みのClaude CLIへ手動で貼り付けて実行する。

## 基本方針

- Codexは必要なタイミングで、Claude CLIに貼り付けるレビュー依頼プロンプトを提示する
- CodexからClaude APIやClaude CLIを自動実行しない
- Claudeの回答は、編集上のセカンドオピニオンとして扱う
- 料金、キャンペーン、スペック、契約条件、解約条件などの事実確認は、Claude回答ではなく公式情報と一次情報を優先する
- Claude回答に出典URLがない事実は断定しない
- Claude回答を反映する場合も、既存の `rules/` と公式情報リサーチ結果を優先する

## 推奨実施タイミング

以下の工程では、原則としてClaude CLI二次チェックの実施を提案する。

1. `phase02_competitor_analysis.md` 作成後
   - 競合分析の抜け漏れ、比較軸の偏り、上位記事の共通要素を確認する
2. `phase05_selected_products.md` 確定前
   - 評価対象サービスの選定妥当性、除外理由、公式確認が必要な項目を確認する
3. `phase06_evaluation_guideline.md` 作成後、PDF化前
   - 評価指標、配点、採点基準、同点処理の妥当性を確認する
4. `phase07_outline.md` 作成後
   - 検索意図との一致、見出しの過不足、重複、読者導線を確認する
5. 主要な `phase08_draft_<section>.md` 作成後
   - 読者目線、比較の説得力、誇大表現、不自然な誘導を確認する
6. `phase09_factcheck_report.md` と `phase09_truthcheck_report.md` 作成後
   - 追加で見るべき真偽チェック観点、根拠不足、表と本文の矛盾を確認する

軽微な修正や単純な整形では、Claude CLI二次チェックを省略してよい。

## Codexが提示する内容

Claude CLI二次チェックを提案する場合、Codexは以下を提示する。

- 実施目的
- Claude CLIへ貼り付けるプロンプト
- Claudeに渡す対象ファイルや要約
- Claudeの回答を受け取った後にCodexへ貼り戻す依頼文

プロンプトには、Claude回答を公式情報の代替にしないこと、出典不明の事実を断定しないこと、指摘は重要度順に出すことを含める。

## 記録方法

Claude CLI二次チェックを実施した場合は、`articles/<slug>/output/phase_meta_claude_review_notes.md` に記録する。

記録項目：

- 実施日
- 対象工程
- 対象ファイル
- Codexが作成した依頼プロンプト
- Claude回答の要約
- 反映した指摘
- 反映しなかった指摘と理由
- 追加確認が必要な項目

## 反映判断

- Claudeの指摘はそのまま採用せず、Codexが `rules/`、公式情報、既存成果物と照合して反映可否を判断する
- 公式情報と矛盾する指摘は採用しない
- 競合記事由来の情報は一次情報ではないため、本文へ断定的に反映しない
- 反映により評価指標、順位、点数、比較表が変わる場合は、根拠と計算式も更新する
