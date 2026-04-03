---
id: SCHEMA-ORG
name: "グローバル組織スキーマ"
type: schema
description: "db/organizations/ に配置するグローバル組織ファイルの必須構造"
---

# グローバル組織スキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `ORG-G-0001_hakoniwa-logistics.md`

## ID規則
- グローバル組織: `ORG-G-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: ORG-G-0001
name: "箱庭物流"
aliases: ["Hakoniwa", "HLX"]
type: organization
tags: [物流, 巨大インフラ, 都市基盤]
public_function: "全国対応の高機能配送ネットワーク"
hidden_purpose: "都市秘匿輸送と異常物件封緘"
area_of_operation: [東京, 関東]
secrecy_level: layered_secret
related_characters: [CHAR-G-0001]
related_locations: [LOC-G-0002]
related_events: [EVT-G-2025-0002]
visibility: public
canon: true
---
```

## 必須フィールド
- `id`: 一意のグローバルID
- `name`: 表示名（日本語）
- `type`: 常に `organization`
- `public_function`: 表向きの機能
- `secrecy_level`: secrecy_levels.md に準拠
- `visibility`: public / series-internal / author-only
- `canon`: true / false

## 本文セクション構造

```markdown
# 概要
（1〜3行の要約）

# 表の顔
（一般社会に見える姿）

# 裏の顔
（秘匿された目的や活動）

# 歴史
（設立経緯、重要な転換点）

# 組織構造
（内部構造、階層、部署）

# 関係勢力
（協力・対立関係にある他組織）

# 備考
（補足事項）
```
