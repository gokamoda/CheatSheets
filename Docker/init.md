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
   ```bash
   sudo apt install docker-compose-plugin
   ```
3. 権限付与
   ```bash
   sudo groupadd docker
   ```
   ```bash
   sudo usermod -aG docker $USER
   ```
4. 起動確認
   ```bash
   sudo service docker start
   ```
   ```bash
   docker run hello-world
   ```
