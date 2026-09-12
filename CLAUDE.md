# CLAUDE.md

## 概要

これは個人のナレッジベース（Zettelkasten風のPKM）リポジトリ。ビルド・テスト・lintの対象となるソフトウェアではなく、Markdownノートとその関連図（SVG）の集合。

## ノートの書き方

説明している概念にすでに定まった名称（手法名・理論名など）がある場合は、その名称を明記する。

## 図の使い方

関係性・階層・フロー・分布など、文章より図の方が伝わる内容はSVGで表現し `notes/resources/` に配置してノートから埋め込む（例: `dns-hierarchy.svg` = 階層構造、`risk-map.svg` = 象限マップ、`critical-path.svg` = 依存関係のフロー、`risk-process-cycle.svg` = サイクル図）。

- 既存SVGは `viewBox` を使ったシンプルな構成（背景`rect` + `text` + 図形）で、`font-family="Noto Sans CJK JP, sans-serif"` を指定し日本語ラベルを直接埋め込んでいる
- 埋め込みは通常のMarkdown画像記法 `![name.svg](./resources/name.svg)` を使う
