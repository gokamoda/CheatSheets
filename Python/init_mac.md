# MacでPython

- [1. 前提](#1-前提)
- [2. pyenvのインストール](#2-pyenvのインストール)
- [3. Pythonのインストール](#3-pythonのインストール)
- [4. コードを書く](#4-コードを書く)

## 1. 前提
- Homebrewがインストールされている

## 2. pyenvのインストール
```zsh
$ brew install pyenv
$ echo 'eval "$(pyenv init --path)"' >> ~/.zprofile
$ echo 'eval "$(pyenv init -)"' >> ~/.zshrc
$ exec $SHELL
```

## 3. Pythonのインストール
1. インストール可能なバージョンを確認  
    ```zsh
    pyenv install --list
    ```
2. インストール（コマンドは例）  
    ```zsh
    pyenv install miniconda-4-4.7.12
    ```
3. インストール済み環境の確認  
    ```zsh
    pyenv versions
    ```
4. 環境の変更
    ```zsh
    pyenv activate <バージョン名/環境名>
    ```

## 4. コードを書く
- VSCodeで書く（おすすめ）
- 詳しくは`/VSCode/python.md`