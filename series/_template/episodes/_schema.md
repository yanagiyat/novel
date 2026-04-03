---
id: SCHEMA-EPISODE
name: "エピソードスキーマ"
type: schema
description: "エピソード本文ファイルの必須構造"
---

# エピソードスキーマ

## ファイル名規則
`{エピソードID}_{ascii-slug}.md`
例: `SR01-EP001_first-delivery.md`

## YAMLフロントマター必須構造

```yaml
---
episode_id: SRXX-EP001
series_id: SRXX
title: ""
arc: "arc_001_010"
date_start: 2025-01-01
date_end: 2025-01-01
time_band: afternoon
pov: ""
locations: []
characters: []
organizations: []
events: []
spoiler_scope: series-only
canon: false
status: drafted
summary: ""
new_elements_introduced: []
---
```

## 必須フィールド
- `episode_id`: エピソード一意ID
- `series_id`: 所属シリーズ
- `title`: エピソードタイトル
- `status`: 以下のいずれか
  - `planned`: 企画段階
  - `drafted`: 初稿執筆済み
  - `revised`: 改稿済み
  - `canonized`: 正史化
  - `published`: 公開済み
- `spoiler_scope`: 以下のいずれか
  - `public`: ネタバレなし、公開可能
  - `series-only`: シリーズ内のネタバレを含む
  - `author-only`: 作者のみが知る情報を含む
- `canon`: true / false（canonized以上でtrueにする）

## time_band の許容値
- early_morning（早朝）
- morning（午前）
- afternoon（午後）
- evening（夕方）
- night（夜）
- late_night（深夜）
- dawn（明け方）
- multiple（複数の時間帯にまたがる）

## 本文構造

```markdown
# 本文

（小説本文をここに記述する）
```

## 運用ルール
- `drafted` → `revised` → `canonized` → `published` の順で昇格
- `canonized` 以降は重大修正禁止
- 新規要素は `new_elements_introduced` に記録し、対応するdocsファイルを作成すること
