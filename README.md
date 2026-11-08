# 副業を“会社化”するテンプレート集

Zenn の本「**Claude Code で副業を“会社化”して自動運転する**」の第10章で紹介しているテンプレートのダウンロード版です。

コピーして、`<事業名>` などの部分を自分の事業に置き換えて使ってください。使い方と、なぜこの形にしているかは本で説明しています。

## 中身

| ファイル | 何に使うか | 置き場所の例 |
|---|---|---|
| `templates/CLAUDE.template.md` | リポジトリの最上位に置く「絶対ルール」（Claude Code が起動時に自動で読む） | `CLAUDE.md` |
| `templates/COMPANY.template.md` | 会社の仕組み（組織・連携・決裁権限・共有ファイル） | `COMPANY.md` |
| `templates/role-head.template.md` | 事業部長の手順書（週1回・月曜） | `docs/roles/head.md` |
| `templates/role-dev.template.md` | 開発部長の手順書（週2回） | `docs/roles/dev.md` |
| `templates/role-qa.template.md` | 品質管理部長の手順書（週2回。あとから足す） | `docs/roles/qa.md` |
| `templates/role-growth.template.md` | 運用・成長部長の手順書（週3回） | `docs/roles/growth.md` |
| `templates/priorities.template.md` | 今週の優先順位（事業部長が毎週書く） | `priorities.md` |
| `templates/requests.template.md` | 部署間の依頼 | `requests.md` |
| `templates/decisions.template.md` | 社長の判断の記録 | `decisions.md` |
| `templates/weekly-report.template.md` | 社長に届く週次報告の型 | `reports/weekly-YYYY-MM-DD.md` の型 |
| `templates/work-queue.schema.json` | 承認ゲート用キュー（review → pending → published、落ちたら blocked） | `work-queue.json` |

## 使い方（最小構成）

1. 自分の事業のリポジトリを作り、`CLAUDE.template.md` を `CLAUDE.md`（この名前のまま）、`COMPANY.template.md` を `COMPANY.md` としてコピーする
2. `<...>` の部分を埋める。特に「やってはいけないこと」と「お金・アカウントは社員に触らせない」は削らない
3. 役職は事業部長、開発部長、運用・成長部長の3人から始める。`role-head` / `role-dev` / `role-growth` を上の置き場所にコピーして埋める（3人のあいだは、検収を運用・成長部長が兼ねる）
4. `priorities.template.md` / `requests.template.md` / `decisions.template.md` / `work-queue.schema.json` を共有ファイルとして置き、最初の週の優先順位を自分で書く
5. 各役職をクラウドの定期実行（Claude Code のルーティンなど）に登録し、頻度・モデル・手順書を読ませるプロンプトを指定する
6. 週に1回、`weekly-report.template.md` の型で報告が届くようにする
7. 商品が増えて検収まで手が回らなくなったら、`role-qa` を足して4人体制にする

## ライセンス

MIT License（`LICENSE`）。自分の事業で自由に使い、書き換えてかまいません。
