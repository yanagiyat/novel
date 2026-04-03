---
id: SCHEMA-CORELORE
name: "コアロアスキーマ"
type: schema
description: "db/_core_lore/ に配置する作者専用の最上位真相保管ファイルの構造"
---

# コアロアスキーマ

`db/_core_lore/` は作者専用の最上位真相保管領域である。
ここには未公開の世界法則、上位存在、系統間の相互関係、長期構想、仮説、保留事項を記録する。

## 運用原則

- **最初から全部埋めないこと**。空欄、保留、仮説を許容する
- 確定事項と仮説を明確に区別すること
- Claude Codeはここに独断で確定事項を追加してはならない
- 追加・変更は提案としてユーザーに提示すること

## YAMLフロントマター構造

```yaml
---
id: LORE-001
name: "ファイルタイトル"
type: core_lore
status: confirmed / hypothesis / reserved / placeholder
visibility: author-only
last_updated: 2025-01-01
canon: true / false
---
```

## 本文構造

自由形式だが、以下の区分を推奨する:

```markdown
# 確定事項
（ユーザーが確定した設定）

# 仮説
（まだ確定していない案）

# 保留
（今後決定する予定の事項）

# メモ
（その他の覚書）
```
