---
id: SCHEMA-LOC
name: "グローバル地名スキーマ"
type: schema
description: "db/locations/ に配置するグローバル地名ファイルの必須構造"
---

# グローバル地名スキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `LOC-G-0001_kasumizaki-ward.md`

## ID規則
- グローバル地名: `LOC-G-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: LOC-G-0001
name: "霞崎区"
type: location
tags: [東京, 架空区画, 都心]
parent_region: "東京都内"
real_world_anchor: "新宿区西側相当"
public_description: "再開発地区と旧来街区が同居する都心の架空区"
hidden_function: "複数組織が管理する緩衝帯"
controlling_org: [ORG-G-0003]
danger_level: 3
visibility: public
related_ids: [ORG-G-0003, EVT-G-2025-0001]
canon: true
---
```

## 必須フィールド
- `id`: 一意のグローバルID
- `name`: 表示名（日本語）
- `type`: 常に `location`
- `parent_region`: 上位地域
- `real_world_anchor`: 現実世界での対応位置
- `visibility`: public / series-internal / author-only
- `canon`: true / false
- `danger_level`: 1-5（1=安全, 5=極度に危険）

## 本文セクション構造

```markdown
# 概要
（1〜3行の要約）

# 表の構造
（一般に知られている地理・施設）

# 裏の構造
（秘匿された施設・機能・異常）

# 立入条件
（誰がどのように入れるか）

# 注意事項
（執筆時に注意すべきこと）

# 関連事件
（この場所で起きた重要事件）
```
