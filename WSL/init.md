# WSL+Ubuntu(2022.10.21)

- [1. WSLを有効化](#1-wslを有効化)
- [2. 仮想マシンプラットフォーム有効化](#2-仮想マシンプラットフォーム有効化)
- [3. WSL2をデフォルトに設定](#3-wsl2をデフォルトに設定)
- [4. WSLの更新](#4-wslの更新)
- [5. Ubuntsuのインストール](#5-ubuntsuのインストール)
- [6. windows terminalのインストール](#6-windows-terminalのインストール)
- [7. Ubuntuの導入](#7-ubuntuの導入)
- [8. Ubuntuの利用をはじめる](#8-ubuntuの利用をはじめる)
- [9. Daily Notice のエラー (windows11)](#9-daily-notice-のエラー-windows11)
- [10. ターミナルの設定](#10-ターミナルの設定)
- [11. VSCodeで使う](#11-vscodeで使う)

## 1. WSLを有効化
1. PowerShellを管理者として実行し，次のコマンドを実行
   ```PowerShell
   Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
   ```
2. 再起動
   
## 2. 仮想マシンプラットフォーム有効化
1. PowerShellを管理者として実行し，次のコマンドを実行
   ```PowerShell
   Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
   ```
2. 再起動

## 3. WSL2をデフォルトに設定
1. PowerShellを管理者として実行し，次のコマンドを実行
   ```PowerShell
   wsl --set-default-version 2
   ```

## 4. WSLの更新
1. 引き続き管理者として実行したPowerShellで次のコマンドを実行
   ```PowerShell
   wsl --update
   ```


## 5. Ubuntsuのインストール
1. Microsoft Storeで，Ubuntuを検索
2. `Ubuntu 22.04.1 LTS`をインストール

## 6. windows terminalのインストール
1. Microsoft StoreでWindows Terminalを検索
2. `Windows Terminal`をインストール

## 7. Ubuntuの導入
1. インストールしたUbuntuを起動
2. 指示に従って初期設定を行う
3. マウント先はいじらない（windows11）

## 8. Ubuntuの利用をはじめる
1. Windows Terminalを開く
2. タブの右の`⋁`をクリック
3. `Ubuntu 22.04.1 LTS`をクリック
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
    ※次のような出力が得られることがあるが，気にしない．WSL2の仕様の問題らしい．(windows11)
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

## 9. Daily Notice のエラー (windows11)
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


## 10. ターミナルの設定
1. ファイル/ディレクトリ名の自動補完で，大文字小文字を区別しないようにする  
   `.inputrc`ファイルを作成し，以下を追加
   ```
   set completion-ignore-case on
   ```

## 11. VSCodeで使う
- [/VSCode/wsl.md](/VSCode/wsl.md)にしたがって設定を行う