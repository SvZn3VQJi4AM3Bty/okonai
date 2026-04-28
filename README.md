# Pomodoro (GitHub Pages)

GitHub Pages で動く、静的ファイル（HTML/CSS/JSのみ）のポモドーロタイマーです。

## 使い方（ローカル）

このプロジェクトはビルド不要です。

- `index.html` をブラウザで開く
- もしくは簡易サーバーで起動（例: VS Code / Cursor の Live Server など）

## GitHub Pages で公開

1. GitHub のリポジトリを開く
2. Settings → Pages
3. Build and deployment → Source を **Deploy from a branch** に設定
4. Branch を `main` / `/(root)` に設定して保存

しばらくすると `https://<user>.github.io/<repo>/` で公開されます。

## 「できるだけ知られない」設定について（重要）

GitHub Pages は **公開Webサイト**なので、URLを知っている人はアクセスできます（完全な非公開にはできません）。
それでも「検索に出にくくする」ために、このプロジェクトでは以下を設定しています。

- `robots.txt` でクローラーを拒否
- `index.html` に `noindex`（検索結果に出さない）を指定

より確実に「第三者に見られない」ようにしたい場合は、次のどれかが必要です。

- **リポジトリを private にして Pages を使う**（GitHub のプラン/設定によって可否が変わります）
- **認証付きで配信**（Cloudflare Access / Basic認証できるホスティング等）
- **ローカル専用で使う**（端末内だけで完結）

## セキュリティ（最低限）

- 設定は `localStorage` に保存され、サーバーへ送信しません
- 外部ライブラリ依存なし（サプライチェーンリスクを小さく）

