# CLAUDE.md

このリポジトリはZenn（技術ブログプラットフォーム）への記事投稿を管理するためのリポジトリです。

## プロジェクト概要

[Zenn CLI](https://zenn.dev/zenn/articles/zenn-cli-guide) を使用してZennへの記事・本を管理します。

## ディレクトリ構成

```
.
├── articles/       # 記事ファイル（.md）
├── books/          # 本のディレクトリ
├── images/         # 画像ファイル
└── package.json
```

## よく使うコマンド

```sh
npm run add   # 新しい記事を作成（npx zenn new:article）
npm run dev   # プレビューサーバー起動（npx zenn preview）
```

## Zenn記事のフォーマット

記事ファイルは `articles/` ディレクトリに配置し、以下のフロントマターが必要です：

```yaml
---
title: "記事タイトル"
emoji: "🔥"         # 記事のアイコンとなる絵文字（1文字）
type: "tech"        # tech: 技術記事 / idea: アイデア記事
topics: ["topic1", "topic2"]  # タグ（最大5つ）
published: true     # true: 公開 / false: 下書き
---
```

### ファイル名のルール

- `articles/` 直下に配置する `.md` ファイル
- ファイル名はランダムなIDまたは任意のスラッグ（半角英数字・ハイフン・アンダースコアのみ、12〜50文字）

## カスタムスキル

`.claude/commands/` にカスタムスキルを配置しています。

| スキル | 説明 |
|--------|------|
| `/zenn-convert` | 通常のMarkdownファイルをZenn記事形式に変換する |

## 注意事項

- `published: true` にすると即座にZennへ公開されます
- 画像は `/images/` ディレクトリに配置し、`/images/ファイル名` で参照します
- トピックは既存のZennトピックタグを使用することを推奨します
