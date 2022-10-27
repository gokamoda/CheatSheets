# VSCodeのインストールと初期設定
- [1. インストール](#1-インストール)
- [2. オートセーブ設定](#2-オートセーブ設定)
- [3. 改行コードの設定](#3-改行コードの設定)
- [3. 【Mac】codeコマンドのインストール](#3-maccodeコマンドのインストール)

## 1. インストール
https://azure.microsoft.com/ja-jp/products/visual-studio-code/
- コンテキストメニューへの追加はすべし
## 2. オートセーブ設定
1. Ctrl + , で設定を開く
2. 検索窓に`files.autosave`と入れる
3. Auto save を After Delayに変更

## 3. 改行コードの設定
1. Ctrl + , で設定を開く
2. 検索窓に`files.eol`と入れる
3. Eolの設定を`/n`に変更する

## 3. 【Mac】codeコマンドのインストール
1. ⌘⇧P でコマンドパレットを開く
2. `code` と入力する
3. `Shell Command: install 'code' command in Path`を選択
4. `code --list-extensions`でインストールされている拡張機能を確認できる