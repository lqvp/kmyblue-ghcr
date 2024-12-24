# kmyblue-ghcr
kmyblueのビルド済みイメージを作るところ

下のやつを`docker-compose.yml`で指定してあげれば使えます。

- Main application (web & sidekiq):
  - `ghcr.io/lqvp/kmyblue-ghcr:latest-16`
- Streaming service:
  - `ghcr.io/lqvp/kmyblue-ghcr-streaming:latest-16`

個人的なメモ程度ですが以下に実際に使って立ち上げた際の記事を載せておきます
https://zenn.dev/il/articles/cf3fb397a07b8a
