# 100 Pages

1ページ1コンセプトで作る100枚のウェブページ。すべて日本語で読める。

ルール：目を奪うこと（look stunning）／同じデザインを二度使わないこと（zero repetitive designs）／全力で遊ぶこと（go full creative mode）。

## 構成

- `index.html` … ギャラリー（ルート）。ページを追加したら `pages` 配列に1行足す
- `pages/NN-slug.html` … 各ページ。外部依存は Google Fonts のみ、他はすべて単一ファイルに内包
- `.nojekyll` … GitHub Pages で Jekyll 処理を止める

## GitHub Pages で公開する手順

1. このフォルダで `git init` → `git add -A` → `git commit -m "feat: first 10 pages"`
2. GitHub にリポジトリを作成し `git remote add origin ...` → `git push -u origin main`
3. リポジトリの Settings → Pages → Source を「Deploy from a branch」、Branch を `main` / `/ (root)` にして保存
4. 数分後 `https://<user>.github.io/<repo>/` で `index.html` が表示される

各ページはルート相対ではなく相対パス（`pages/...`）でリンクしているので、サブパス配信でもそのまま動く。
