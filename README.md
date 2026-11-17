Public landing page for the Ops Panel (store operations panel).

Source of truth: `mission-control/docs/sales/site/` — edit there, then copy here and push.

| ファイル | 正本 | 備考 |
|---|---|---|
| `index.html` | `docs/sales/site/index.html` | LP 本体 (日英) |
| `og.png` | `docs/sales/site/og.png` | OGP 画像 1200x630。版下は `og.html`、生成は `node scripts/og-render.mjs` |
| `robots.txt` | `docs/sales/site/robots.txt` | 検索は塞いだまま、広告審査とプレビューのクローラだけ通す |

独自ドメインへ移すとき:
1. このリポジトリに `CNAME` (中身はドメイン1行) を置く → GitHub Pages の設定で Custom domain を指定
2. `index.html` の `og:url` / `canonical` / `og:image` / `twitter:image` の 4 行を新ドメインに書き換える
3. 検索にも載せるなら `robots.txt` の `Disallow: /` を外す
