# WSL+Ubuntu(2022.10.21)

- [1. WSLを有効化](#1-wslを有効化)
- [2. Ubuntsuのインストール](#2-ubuntsuのインストール)
- [3. Ubuntuの導入](#3-ubuntuの導入)
- [4. Daily Notice のエラー](#4-daily-notice-のエラー)
- [5. ターミナルの設定](#5-ターミナルの設定)
- [6. VSCodeで使う](#6-vscodeで使う)

## 1. WSLを有効化
1. PowerShellを管理者として実行し，次のコマンドを実行
   ```PowerShell
   Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
   ```
2. 再起動
   
## 2. Ubuntsuのインストール
1. Microsoft Storeで，Ubuntuを検索
2. `Ubuntu 22.04.1 LTS`をインストール

## 3. Ubuntuの導入
1. インストールしたUbuntuを起動
2. 言語やユーザー名，パスワード等を求められるので入力
3. マウント先はいじらない
4. リポジトリ参照先の変更  
   Ubuntuのコンソールで以下を実行
      ```bash
      sudo sed -i -e 's%http://.*.ubuntu.com%http://ftp.jaist.ac.jp/pub/Linux%g' /etc/apt/sources.list
      ```
5. インストールされているソフトの更新  
   Ubuntuのコンソールで以下を実行
      ```bash
      sudo apt update
      sudo apt upgrade
      ```
    ※次のような出力が得られることがあるが，気にしない．WSL2の仕様の問題らしい．
    ```bash
    Scanning linux images...

   Failed to retrieve available kernel versions.

   Failed to check for processor microcode upgrades.

   No services need to be restarted.

   No containers need to be restarted.

   User sessions running outdated binaries:
   root @ /dev/pts/0: apt[399,1563]

   No VM guests are running outdated hypervisor (qemu) binaries on this host.
    ```

## 4. Daily Notice のエラー


エラー内容
```bash
/etc/update-motd.d/50-landscape-sysinfo: 17: cannot create /var/lib/landscape/landscape-sysinfo.cache: Permission denied
```
解決方法：[参考サイト](https://askubuntu.com/questions/1414483/landscape-sysinfo-cache-permission-denied-when-i-start-ubuntu-22-04-in-wsl)
1. landscape-common(linux serverで使用されるがWSLでは使われないもの)を削除
   ```bash
   sudo apt remove landscape-common
   ```
2. その他使われていないパッケージの削除
   ```bash
   sudo apt autoremove
   ```
3. 不要ファイル削除
   ```bash
   rm ~/.motd_shown
   ```


## 5. ターミナルの設定
1. ファイル/ディレクトリ名の自動補完で，大文字小文字を区別しないようにする  
   `.inputrc`ファイルを作成し，以下を追加
   ```
   set completion-ignore-case on
   ```

## 6. VSCodeで使う
- [/VSCode/wsl.md](/VSCode/wsl.md)にしたがって設定を行う