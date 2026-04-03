---
id: SCHEMA-CHAR
name: "グローバル人物スキーマ"
type: schema
description: "db/characters/ に配置するグローバル人物ファイルの必須構造"
---

# グローバル人物スキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `CHAR-G-0001_kurokawa-ren.md`

## ID規則
- グローバル人物: `CHAR-G-{4桁連番}`
- シリーズ起源の場合は `origin_series` に元シリーズIDを記録

## YAMLフロントマター必須構造

```yaml
---
id: CHAR-G-0001
name: "黒川 蓮"
aliases: ["レン", "R", "kuro"]
type: character
species: human
tags: [若手, 裏社会, 情報屋]
origin_series: SR01
status: active
public_role: "配送会社の契約ドライバー"
hidden_role: "非公式情報仲介者"
affiliation: [ORG-G-0001]
base_location: [LOC-G-0001]
first_appearance: SR01-EP001
visibility: public
knowledge_level: medium
related_ids: [ORG-G-0001, LOC-G-0001, EVT-G-2025-0001]
promotion_from_local: null
notes: ""
canon: true
---
```

## 必須フィールド
- `id`: 一意のグローバルID
- `name`: 表示名（日本語）
- `type`: 常に `character`
- `species`: human / non-human / unknown 等
- `status`: status_values.md に準拠
- `visibility`: public / series-internal / author-only
- `canon`: true / false

## 本文セクション構造

```markdown
# 概要
（1〜3行の要約）

# 外見
（外見の特徴）

# 口調
（話し方の特徴、一人称、語尾など）

# 能力・技能
（持っている能力や技能）

# 対人関係
（主要な人間関係）

# 知っていること
（このキャラクターが知っている秘密・情報）

# 知られていること
（他のキャラクターや社会がこのキャラについて知っていること）

# 禁止事項
（このキャラクターに関して作者として避けるべきこと）

# 登場履歴
（エピソードIDと簡潔な役割）
```

## 昇格規則
シリーズローカルから昇格した場合:
- `promotion_from_local` にローカルIDを記録
- ローカルファイル側に `promoted_to: CHAR-G-XXXX` を追記
- 既存の参照は破壊しない
