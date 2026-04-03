---
id: SCHEMA-EVT
name: "グローバルイベントスキーマ"
type: schema
description: "db/events/ に配置するグローバルイベントファイルの必須構造"
---

# グローバルイベントスキーマ

## ファイル名規則
`{ID}_{ascii-slug}.md`
例: `EVT-G-2025-0001_kasumizaki-disappearance.md`

## ID規則
- グローバルイベント: `EVT-G-{年}-{4桁連番}`

## YAMLフロントマター必須構造

```yaml
---
id: EVT-G-2025-0001
name: "霞崎駅前集団失踪未遂"
type: event
date_start: 2025-03-14
date_end: 2025-03-14
public_explanation: "駅前の一時的な通信障害と群衆混乱"
true_summary: "局所異界侵食による大規模誘導事案"
involved_ids: [LOC-G-0001, ORG-G-0003]
affected_series: [SR01, SR04]
aftermath: "監視強化と報道統制"
canon: true
visibility: series-internal
---
```

## 必須フィールド
- `id`: 一意のグローバルID
- `name`: イベント名
- `type`: 常に `event`
- `date_start`: 開始日
- `date_end`: 終了日
- `public_explanation`: 一般社会での説明
- `true_summary`: 真相の要約
- `canon`: true / false
- `visibility`: public / series-internal / author-only

## 本文セクション構造

```markdown
# 概要
（1〜3行の要約）

# 公的記録
（一般社会に知られている情報）

# 真相
（実際に何が起きたか）

# 影響
（事件後にどのような変化があったか）

# 関連話数
（どのシリーズのどのエピソードで扱われるか）
```
