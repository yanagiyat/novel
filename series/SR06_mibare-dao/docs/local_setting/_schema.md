---
id: SCHEMA-LOCAL-SETTING
name: "シリーズローカル設定スキーマ"
type: schema
description: "シリーズ固有の世界設定・ルールを記録するファイルの構造"
---

# シリーズローカル設定スキーマ

シリーズ固有の世界観ルール、魔法体系、技術体系、社会構造などを個別ファイルで管理する。

## ファイル名規則
`{トピック名のascii-slug}.md`
例: `magic-system.md`, `school-rules.md`

## YAMLフロントマター必須構造

```yaml
---
name: ""
type: local_setting
series_id: SRXX
tags: []
visibility: series-internal
canon: false
---
```

## 本文構造
自由形式。シリーズの必要に応じて構成する。
