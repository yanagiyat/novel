---
id: SCHEMA-LOCAL-LOC
name: "シリーズローカル地名スキーマ"
type: schema
description: "シリーズ固有の地名ファイルの必須構造"
---

# シリーズローカル地名スキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `LOC-SR01-0001_sakura-cafe.md`

## ID規則
- シリーズ地名: `LOC-{シリーズID}-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: LOC-SR01-0001
name: ""
type: location
tags: []
series_id: SR01
parent_region: ""
real_world_anchor: ""
public_description: ""
hidden_function: ""
controlling_org: []
danger_level: 1
visibility: series-internal
related_ids: []
promoted_to: null
canon: false
---
```

## 本文セクション
グローバル地名スキーマと同一構造を使用する。
