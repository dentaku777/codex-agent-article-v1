# Template Parse Policy

WordPressブロックエディタに貼り付け可能なHTML/ブロックコードへ変換するための共通ルール。

## 基本方針

- 現状の標準テンプレートはSWELLとする
- 将来、SWELL以外のテンプレートにも対応できるよう、テンプレート固有の装飾と共通ブロックを分けて管理する
- テンプレート指定がない場合はSWELL向けに出力する
- WordPressへの自動投稿は行わない

## 出力先

| テンプレート | 出力先 | 参照ルール |
|---|---|---|
| SWELL | `articles/<slug>/output/phase11_swell_blocks.html` | `rules/swell_default_blocks.md`、`rules/swell_custom_patterns.md` |
| その他 | `articles/<slug>/output/phase11_<template>_blocks.html` | 専用ルールファイルを追加して参照 |

## 共通変換対象

- h2/h3
- 段落
- リスト
- 表
- FAQ
- CTA
- 注意ボックス
- 比較表
- ランキング個別説明

## 未定義テンプレートの扱い

- 専用ルールがない装飾は推測しない
- 通常のWordPressブロックHTMLとして出力する
- テンプレート固有クラス名や独自ショートコードを勝手に作らない

## 品質確認

- `phase09_fixed_article.md`、`phase09_factcheck_report.md`、`phase09_truthcheck_report.md`、`phase05_faq_candidates.md` を確認してから変換する
- 未確認情報、要修正、要削除が残る場合は変換前に警告する
- 表、本文、画像仕様、CTAの数値や順位を一致させる
- FAQ/Q&Aは採用方針、公式確認状況、出典要件に反する回答が残っていないか確認する
