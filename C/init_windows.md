# windowsでC (MinGW編)

- [1. MinGWのインストール](#1-mingwのインストール)
- [2. PATHの設定](#2-pathの設定)
- [3. インストールの確認](#3-インストールの確認)
- [4. コードを書く](#4-コードを書く)
- [(参考)MinGWのインストール（インストーラ―版：主は失敗した）](#参考mingwのインストールインストーラ版主は失敗した)

## 1. MinGWのインストール
- https://sourceforge.net/projects/mingw-w64/files/mingw-w64/
- 上記リンクにアクセス
- 64bit版の場合はMinGW-W64 GCCのx86_64-posix-sehを選択
- ダウンロードされた7zipファイルを解凍（解凍ソフト→https://www.7-zip.org/）
- 解凍されたフォルダ（mingw64）を，`C:\ProgramFiles`に移動

## 2. PATHの設定
- Windows PowerShellを起動し，以下コマンドを実行
  ```PowerShell
  [System.Environment]::SetEnvironmentVariable('path', [System.Environment]::GetEnvironmentVariable('path', 'User') + 'C:\Program Files\mingw64\bin;','User')
  ```
- PCを再起動する

## 3. インストールの確認
- コマンドプロンプトを起動
- `gcc -v`コマンドを実行
- 最後にgccのバージョンが表示されればインストール完了

## 4. コードを書く
- [/VSCode/c_windows.md](/VSCode/c_windows.md)で設定を行い，VSCodeで書く/実行する



---
## (参考)MinGWのインストール（インストーラ―版：主は失敗した）
- https://sourceforge.net/projects/mingw-w64/files/Toolchains%20targetting%20Win32/Personal%20Builds/mingw-builds/installer/mingw-w64-install.exe/download
- 上記リンクからmingw-w64-install.exeをダウンロード
- 実行
- `Next`で開始
- 64bit版の場合は，Architectureを`x86_64`に変更
- それに伴ってExceptionがsehに勝手に変更される
- `Next`で進んでインストール開始
- `The file has been downloaded incorrectly!`と出たら，7zipバージョンを実行