# Math Practice — 法務ページ（公開用）

iOS アプリ「算数練習」の**サポート・法務ページのみ**を GitHub Pages で公開するリポジトリです。

アプリ本体（`FunakiTakuya/Math-Practice`）は Private のままにし、本リポジトリだけ Public にします。

## 公開 URL（想定）

ベース: `https://funakitakuya.github.io/Math-Practice-Legal/`

| ページ | URL |
|--------|-----|
| トップ（一覧） | `…/` または `…/index` |
| サポート | `…/support` |
| プライバシーポリシー | `…/privacy-policy` |
| 利用規約 | `…/terms-of-use` |
| 特定商取引法に基づく表記 | `…/tokushoho` |

## 初回セットアップ（GitHub）

1. GitHub で **Public** リポジトリ `Math-Practice-Legal` を作成
2. ローカルから push:

```bash
cd "/Users/takuya/iPhoneApp/Math-Practice-Legal"
git remote add origin git@github.com:FunakiTakuya/Math-Practice-Legal.git
git branch -M main
git push -u origin main
```

3. **Settings → Pages** → Branch: `main`、Folder: **`/ (root)`** → Save
4. 1〜3 分後、上記 URL がブラウザで開けることを確認

## 文言の更新

正本は Private リポジトリ `iOS_app/Math Practice` の `Legal/` です。

```bash
cd "/Users/takuya/iPhoneApp/iOS_app/Math Practice"
./scripts/sync-legal-to-public-repo.sh
cd "/Users/takuya/iPhoneApp/Math-Practice-Legal"
git add -A && git commit -m "Update legal pages" && git push
```

## ファイル構成

- `index.md` — 4 ページへのリンク一覧
- `support.md` / `privacy-policy.md` / `terms-of-use.md` / `tokushoho.md`
