# VSCodeでC

- [1. 前提](#1-前提)
- [2. 拡張機能のインストール・設定](#2-拡張機能のインストール設定)
- [3. コードを書く・実行する](#3-コードを書く実行する)

## 1. 前提
- [/C/init_windows.md](/C/init_windows.md)にしたがってコンパイラをインストール済み
- [/VSCode/init.md](/VSCode/init.md)にしたがってVSCodeを設定済み

## 2. 拡張機能のインストール・設定
- コマンドプロンプトを起動し，以下のコマンドを実行
- C/C++
  ```cmd
  code --install-extension ms-vscode.cpptools
  ```
- Code Runner
  ```cmd
  code --install-extension formulahendry.code-runner
  ```
- Code Runnerの設定を開く
- `Code-runner: Run In Terminal`にチェックを入れる

## 3. コードを書く・実行する
- 拡張子`.c`でファイルを作成
- コードを書いたら，右上の $\triangleright$ をクリックし，実行