---
id: SCHEMA-LOCAL-CHAR
name: "シリーズローカル人物スキーマ"
type: schema
description: "シリーズ固有の人物ファイルの必須構造"
---

# シリーズローカル人物スキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `CHAR-SR01-0001_tanaka-yui.md`

## ID規則
- シリーズ人物: `CHAR-{シリーズID}-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: CHAR-SR01-0001
name: "田中 結衣"
aliases: []
type: character
species: human
tags: []
series_id: SR01
status: active
public_role: ""
hidden_role: ""
affiliation: []
base_location: []
first_appearance: SR01-EP001
visibility: series-internal
knowledge_level: low
related_ids: []
promoted_to: null
notes: ""
canon: false
---
```

## 本文セクション
グローバル人物スキーマと同一構造を使用する。

## 昇格
グローバルに昇格する場合、`promoted_to` にグローバルIDを記録する。
このファイルは削除せず、参照ポインタとして残す。
