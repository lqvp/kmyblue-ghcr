# kmyblue-ghcr
kmyblueのビルド済みイメージを作るところ

下のやつを`docker-compose.yml`で指定してあげれば使えます。

- Main application (web & sidekiq):
  - `ghcr.io/lqvp/kmyblue-ghcr:latest-16`
- Streaming service:
  - `ghcr.io/lqvp/kmyblue-ghcr-streaming:latest-16`
