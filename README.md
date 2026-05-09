# 名古屋大学ファンクラブ — v0（最小公開版）

最速で世に出すための最小構成。3セクション・1〜1.5スクロール。

## ファイル構成

```
site-v0/
├── index.html       … 3セクション（Masthead Light / Letter Mini / Contact）
├── styles.css       … v1のサブセット
├── netlify.toml
├── .gitignore
├── README.md
└── assets/
    └── logo.jpg
```

詳細は、リポジトリ root の `V0_DESIGN_SPEC.md` と `V0_SECTIONS.md` を参照。

## v1との関係

- v1（新聞風グリッド・全7セクション）は `site-v1/` に並列保存。
- v0で公開 → v1完成後に差し替え、を想定。

## ローカル確認

```bash
cd site-v0
python3 -m http.server 5173
```

## デプロイ

リポジトリ root の `DEPLOY.md` に準じる。`site-v0/` 配下を**リポジトリのルート**にコピーする運用。
