# DifyTestServerの環境構築

#### VPSにサーバー追加
- Ubuntu 24.04 (x86_64)
- サービス: VPS
- CPU: 4Core
- メモリ: 4GB
- SSD: 100GB
- セキュリティグループ
  - default
  - IPv4v6-SSH
  - IPv4v6-Web
 
#### システムアップデート
- `sudo apt update && sudo apt upgrade -y`

#### DockerとDocker Composeのインストール
- Docker
  - `sudo curl -fsSL https://get.docker.com -o get-docker.sh`
  - `sudo sh get-docker.sh`
- Docker Compose
  - `sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
  - `sudo chmod +x /usr/local/bin/docker-compose`

#### Difyのダウンロードと環境設定
- `git clone https://github.com/langgenius/dify.git`
- `cd dify/docker`
- `cp .env.example .env`
- パスワード変更

#### Difyの起動
- `sudo docker-compose up -d`
- 開く
  - `http://host_ip`
