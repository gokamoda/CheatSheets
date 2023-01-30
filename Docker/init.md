# UbuntuにDockerを入れる

1. 既存ライブラリアップデート
   ```bash
   sudo apt update
   ```
   ```bash
   sudo apt upgrade
   ```
2. インストール
   ```bash
   curl -fsSL https://get.docker.com -o get-docker.sh
   ```
   ```bash
   sudo sh get-docker.sh
   ```
3. 権限付与
   ```bash
   sudo groupadd docker
   ```
   ```bash
   sudo usermod -aG docker $USER
   ```
   ```bash
   docker run hello-world
   ```
