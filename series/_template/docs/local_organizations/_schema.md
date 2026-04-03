---
id: SCHEMA-LOCAL-ORG
name: "シリーズローカル組織スキーマ"
type: schema
description: "シリーズ固有の組織ファイルの必須構造"
---

# シリーズローカル組織スキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `ORG-SR01-0001_local-shop.md`

## ID規則
- シリーズ組織: `ORG-{シリーズID}-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: ORG-SR01-0001
name: ""
aliases: []
type: organization
tags: []
series_id: SR01
public_function: ""
hidden_purpose: ""
area_of_operation: []
secrecy_level: public
related_characters: []
related_locations: []
related_events: []
visibility: series-internal
promoted_to: null
canon: false
---
```

## 本文セクション
グローバル組織スキーマと同一構造を使用する。
