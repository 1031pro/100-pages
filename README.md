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

## 制作モデルの区分

- **001〜012：Fable 5.1** — 既存12作品。各HTMLは変更していない。
- **013〜024：Astraの制作範囲** — 初稿12作は不採用。ユーザーの依頼により現行版を比較公開。再制作版は別管理。

制作順・状態は [Astra制作記録](docs/ASTRA-013-024.md)。旧案「継ぎ目」は不採用で完成数に含めない。`_archive/07-suminagashi.html` は退避のまま。

Cloudの開始点 `25debb6` ではトップ名が `Fable 5.1 Studies`。Windows記録の「百景」との差異を残し、トップ名は変更していない。

Astraの作品は外部フォント・外部画像・スクリプト・APIに依存しない単独HTML。操作中心だけでなく情景中心の作品も制作する。候補ごとの画像・短い動画・単独HTML・検証結果を保存し、ソースのチェックポイントは動画と分ける。

2026-10-04、ユーザーの明示依頼により初稿12作の現行版を既存GitHub Pagesへ比較公開する。22のモバイル配置修正を含む。再制作途中の作品は公開対象に含めない。

公開先：https://1031pro.github.io/100-pages/
公開経路：既存の main ブランチ → GitHub Pages の pages build and deployment。
