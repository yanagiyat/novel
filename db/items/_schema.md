---
id: SCHEMA-ITEM
name: "グローバルアイテムスキーマ"
type: schema
description: "db/items/ に配置するグローバルアイテムファイルの必須構造"
---

# グローバルアイテムスキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `ITEM-G-0001_fuukyo-zero.md`

## ID規則
- グローバルアイテム: `ITEM-G-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: ITEM-G-0001
name: "封匣零式"
type: item
tags: [封印技術, 危険物, 携行品]
origin_series: null
status: active
owner: null
related_ids: [ORG-G-0004, EVT-G-2025-0003]
visibility: author-only
canon: false
---
```

## 必須フィールド
- `id`: 一意のグローバルID
- `name`: 表示名（日本語）
- `type`: 常に `item`
- `status`: status_values.md に準拠
- `visibility`: public / series-internal / author-only
- `canon`: true / false

## 本文セクション構造

```markdown
# 概要
（1〜3行の要約）

# 機能
（何ができるか）

# 制約
（使用条件、制限）

# 危険性
（使用に伴うリスク）

# 所有履歴
（誰が持っていたか）

# 備考
（補足事項）
```
