# げいのう労災伝説 ランディングページ

芸能従事者向け労災特別加入制度の解説マンガ「げいのう労災伝説」を SNS 等で広く共有するための GitHub Pages 用ランディングページです。

## 公開 URL（GitHub Pages 有効化後）

```
https://yabemasaru23-source.github.io/rousai02/
```

PDF 直リンク：
```
https://yabemasaru23-source.github.io/rousai02/geinou-rousai.pdf
```

## ファイル構成

```
rousai02/
├─ index.html         ランディングページ（OGP / Twitter Card / JSON-LD / GA4 入り）
├─ geinou-rousai.pdf  本体パンフレット（15ページ・約18MB）
├─ og-image.jpg       OGP / Twitter Card 用サムネイル（1200×630）
├─ hero.jpg           ヒーロー画像（表紙）
├─ pages/             マンガ全15ページのサムネイル
│   └─ page-01.jpg 〜 page-15.jpg
├─ README.md
└─ .gitignore
```

## 公開前にやること

### 1. GitHub にプッシュ

ローカルの作業フォルダで：

```bash
cd path/to/rousai02
git init
git add .
git commit -m "Initial publish: げいのう労災伝説 landing page"
git branch -M main
git remote add origin https://github.com/yabemasaru23-source/rousai02.git
git push -u origin main
```

### 2. GitHub Pages を有効化

1. https://github.com/yabemasaru23-source/rousai02/settings/pages を開く
2. **Source** を `Deploy from a branch` に
3. **Branch** を `main` / `/(root)` に設定して **Save**
4. 数十秒後、`https://yabemasaru23-source.github.io/rousai02/` にアクセスして表示を確認

### 3. Google Analytics 4 を有効化（任意だが推奨）

1. https://analytics.google.com/ で GA4 プロパティを作成し、測定 ID（`G-XXXXXXXXXX` の形式）を取得
2. `index.html` を開き、2 か所ある `G-XXXXXXXXXX` を実際の測定 ID にすべて置換
3. 再度 `git commit` → `git push` で反映

### 4. SNS 共有時の注意

OGP 画像の URL は **絶対 URL** にしてあるため、Facebook / X どちらでも自動でリッチプレビューが表示されます。
キャッシュが残っている場合は以下のデバッガーで再取得してください：

- Facebook: https://developers.facebook.com/tools/debug/
- X (Twitter): https://cards-dev.twitter.com/validator は廃止。投稿後にプレビューを確認

## SEO チェックリスト

- [x] `<title>` / `<meta description>` 設定済み
- [x] 正規 URL `<link rel="canonical">` 設定済み
- [x] OGP（og:title / og:description / og:image / og:url）設定済み
- [x] Twitter Card（summary_large_image）設定済み
- [x] JSON-LD 構造化データ（WebSite / Article / Service）設定済み
- [x] レスポンシブ（モバイル対応）
- [x] `loading="lazy"` で画像遅延読み込み
- [ ] GA4 測定 ID の差し替え（公開前に手動）
- [ ] Google Search Console 登録（公開後に推奨）

## ライセンス・出典

- 一般社団法人 JAPAN ACTION GUILD（厚生労働省認可団体）
- 公式 加入サイト：https://rousai.or.jp/
- 法人サイト：https://japanactionguild.jp/
