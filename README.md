# kmyblue-ghcr
[kmyblue](https://github.com/kmycode/mastodon)のビルド済みイメージを作るところ

下のやつを`docker-compose.yml`で指定してあげれば使えます。

# kmyblue-16.x
- Main application (web & sidekiq):
  - `ghcr.io/lqvp/kmyblue-ghcr:latest-16`
- Streaming service:
  - `ghcr.io/lqvp/kmyblue-ghcr-streaming:latest-16`
 
# kmyblue-15-lts
- Main application (web & sidekiq):
  - `ghcr.io/lqvp/kmyblue-ghcr:latest-15`
- Streaming service:
  - `ghcr.io/lqvp/kmyblue-ghcr-streaming:latest-15`
 
## ElasticSearch+Sudachi
- `ghcr.io/lqvp/elasticsearch-7.17.8-3.3.0:latest`

これを使えばそのまま読み込むるはず(検証済み)

個人的なメモ程度ですが以下に実際に使って立ち上げた際の記事を載せておきます

https://zenn.dev/il/articles/cf3fb397a07b8a
