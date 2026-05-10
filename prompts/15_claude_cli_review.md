# Claude CLI二次チェック用プロンプト作成

対象工程の成果物について、Claude CLIに貼り付ける二次チェック依頼プロンプトを作成してください。

作業前に必ず以下のルールを確認してください。

- `rules/claude_cli_review_policy.md`
- 対象工程に対応する `rules/` ファイル
- `rules/source_priority.md`
- `rules/hallucination_policy.md`

## 入力

- 記事slug
- 対象工程
- 対象ファイル
- Codex側で特に確認したい論点

## 出力

ユーザーがClaude CLIにそのまま貼り付けられる形で、以下を含むプロンプトを作成する。

1. Claudeに期待する役割
2. 対象工程と対象ファイル
3. レビュー観点
4. 重要度順の指摘形式
5. 公式情報・一次情報を優先し、出典不明の事実を断定しない注意
6. Codexへ貼り戻すための回答フォーマット

## 回答フォーマット

```markdown
以下をClaude CLIに貼り付けてください。

---
<Claude CLI用プロンプト>
---

Claudeの回答が返ってきたら、そのままCodexに貼ってください。Codex側で `rules/` と公式情報に照合して、反映可否を判断します。
```

## 注意

- Claude APIの利用を促さない
- Claude CLIの自動実行を前提にしない
- Claudeの回答を一次情報として扱わせない
- 対象ファイルが長すぎる場合は、Codex側で要約または該当抜粋を付けて渡す
