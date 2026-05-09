# 名古屋大学ファンクラブ — 公式サイト

> 卒業生を中心とした、名古屋大学を「見続ける」ためのささやかな会のサイト。

## 構成（最小構成・ビルド不要）

```
site/
├── index.html       … トップページ（全7セクション）
├── styles.css       … 全スタイル
├── netlify.toml     … デプロイ設定（キャッシュ・セキュリティヘッダ）
├── assets/
│   ├── logo.jpg     … ファンクラブ ロゴ
│   └── cover.jpg    … 会報「I saw」第一号 表紙
└── README.md
```

ビルド・依存関係なし。`index.html` をそのままブラウザで開けば動きます。

## ローカルプレビュー

任意の静的サーバで開いてください。例：

```bash
# Python
python3 -m http.server 5173

# Node (npx)
npx serve .
```

http://localhost:5173 を開く。

## デプロイ（Netlify + GitHub）

`DEPLOY.md` を参照（リポジトリのルートにあります）。

## デザイン方針

- **新聞風グリッド（Times-grid）案を採用**
- 紙：`#f1ecdd` クリーム
- 墨：`#1a1a12` 文字
- 緑：`#0f3d2e`（会報「I saw」表紙の森林緑）
- 炎：`#c95a25` 差し色
- 和文：Shippori Mincho（明朝）
- 欧文：Cormorant Garamond（イタリックを多用）
- 等幅：JetBrains Mono（メタ情報）

詳細仕様は `DESIGN_SPEC.md` を参照。

## セクション構成（7段）

1. **Masthead** — 新聞題字。日付・号数・「The Nagoya Univ. Fanclub Times」
2. **Lead strip** — リード記事「外野は、いま24名になりました。」＋ 3カラム本文＋FACT BOX
3. **Letter** — 会長まえがき
4. **I saw** — 会報の表紙＆紹介
5. **Index** — 会のあゆみ（時系列、点線リーダー）
6. **Join** — 緑ベタの入会CTA
7. **Colophon** — 奥付・連絡先

## 編集ガイド

- `index.html` 内の各セクションは `<!-- ============ NN · NAME ============ -->` でラベル分けしてあります。該当ブロックだけを編集してください。
- 記録（INDEX）に項目を追加：`<ol class="toc">` 内に `<li class="toc__row">` をコピーして増やすだけ。
- 会報の号を増やす場合は、cover画像を `/assets/cover-vol-2.jpg` などで足し、`§04 I saw` ブロックを複製。
