# WSL+Ubuntu上でC

- [前提](#前提)
- [コンパイラのインストール](#コンパイラのインストール)

## 前提
- [WSL+Ubuntuの設定](/WSL/init.md)が完了している

## コンパイラのインストール
1. Ubuntuのbashを開く
2. インストール済みパッケージのアップデート
   ```bash
   sudo apt update
   ```
   ```bash
   sudo apt upgrade
   ```
3. コンパイラのインストール
   ```bash
   sudo apt install gcc
   ```
4. インストールの確認
   ```bash
   gcc --version
   ```