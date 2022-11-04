# WSL+Ubuntu上でC

- [前提](#前提)
- [コンパイラのインストール](#コンパイラのインストール)
- [コードを書く](#コードを書く)

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
3. コンパイラ（&色々）のインストール
   ```bash
   sudo apt install build-essential
   ```
4. インストールの確認
   ```bash
   gcc --version
   ```

## コードを書く
- [/VSCode/c_wsl.md](/VSCode/c_wsl.md)で設定を行い，VSCodeで書く/実行する