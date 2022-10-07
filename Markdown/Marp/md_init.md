---
marp: true
paginate: true
---


# VSCodeでMarkdown
- [1. 前提](#1-前提)
- [2. 拡張機能をインストール](#2-拡張機能をインストール)
- [3. 目次（TOC）作成](#3-目次toc作成)
- [4. PDF化](#4-pdf化)
- [5. 表などの自動フォーマット](#5-表などの自動フォーマット)


---


## 1. 前提
- `/VSCode/init.md`にしたがってvscodeを設定済み
- TOC：Table of Contents = 目次


---


## 2. 拡張機能をインストール
1. Markdown All in Oneをインストール
2. これにより、インデントやリスト、TOCの作成が簡単になる。
3. `$ code --install-extension yzhang.markdown-all-in-one` でも可
4. 拡張機能の設定を開く
5. `Markdown › Extension › Toc: Levels`を`2..6`に変更すると便利  
   （mdのタイトルがTOCから除外される）


---


## 3. 目次（TOC）作成
1. 目次を作成したい場所にカーソルを移動する
2. Ctrl + Shift + P ( ⌘ + ⇧ + P ) でコマンドパレットを開く
3. `Markdown All in One: Create Table of Contents`を選択
4. 見出し番号を振りたい場合は同じくコマンドパレットで`Markdown All in One: Add/Update ection numbers`を選択


---


## 4. PDF化
1. Ctrl + Shift + P ( ⌘ + ⇧ + P ) でコマンドパレットを開く
2. `html` と入力
3. `Markdown All in One: Print current document to HTML` を選択
4. 作成されたHTMLブラウザ（Chromeなど）で開いてPDFに印刷


---


## 5. 表などの自動フォーマット
- Shift + Alt + F （⇧ + ⌥ + F）
- Prettierによるフォーマットは崩れる可能性あり
- Markdown All in One のフォーマットを使うべし

