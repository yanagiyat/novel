---
id: SCHEMA-LOCAL-ITEM
name: "シリーズローカルアイテムスキーマ"
type: schema
description: "シリーズ固有のアイテムファイルの必須構造"
---

# シリーズローカルアイテムスキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `ITEM-SR01-0001_old-compass.md`

## ID規則
- シリーズアイテム: `ITEM-{シリーズID}-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: ITEM-SR01-0001
name: ""
type: item
tags: []
series_id: SR01
status: active
owner: null
related_ids: []
visibility: series-internal
promoted_to: null
canon: false
---
```

## 本文セクション
グローバルアイテムスキーマと同一構造を使用する。
