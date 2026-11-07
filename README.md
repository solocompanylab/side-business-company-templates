# 副業を“会社化”するテンプレート集

Zenn の本「**Claude Code で副業を“会社化”して自動運転する**」の第10章で紹介しているテンプレートのダウンロード版です。

コピーして、`<事業名>` などの部分を自分の事業に置き換えて使ってください。使い方と、なぜこの形にしているかは本で説明しています。

## 中身

| ファイル | 何に使うか |
|---|---|
| `templates/CLAUDE.template.md` | リポジトリの最初に置く「絶対ルール」 |
| `templates/COMPANY.template.md` | 社内規定（組織・決裁権限・共有ファイル） |
| `templates/role-ops.template.md` | 役職の手順書の例（運用・成長部長） |
| `templates/weekly-report.template.md` | 社長に届く週次報告の型 |
| `templates/work-queue.schema.json` | 部署間で仕事を渡すキューの形式 |

## 使い方（最小構成）

1. 自分の事業のリポジトリを作り、`CLAUDE.template.md` を `CLAUDE.md`、`COMPANY.template.md` を `COMPANY.md` としてコピーする
2. `<...>` の部分を埋める。特に「やってはいけないこと」と「お金・アカウントは社員に触らせない」は削らない
3. 役職は「事業部長・開発・品質管理・運用・成長」の4人から始める。`role-ops.template.md` を見本に、役職ごとに手順書を書く
4. 週に1回、`weekly-report.template.md` の型で報告が届くようにする

## ライセンス

MIT License（`LICENSE`）。自分の事業で自由に使い、書き換えてかまいません。
