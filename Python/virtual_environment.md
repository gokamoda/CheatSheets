# 仮想環境

## pyenv venv

1. pythonのインストール
    ```Shell
    pyenv install 3.10.8
    ```
2. アクティベート
    ```
    pyenv local 3.10.8
    ```
3. 仮想環境を使うディレクトリを作成する
    ```Shell
    mkdir test
    ```
4. ディレクトリに入る
    ```Shell
    cd test
    ```
5. 仮想環境構築
    ```Shell
    python -m venv .venv
    ```
  `.venv`は仮想環境の名前．よく使われる
6. 仮想環境アクティベート
    ```Shell
    . .venv/bin/activate
    ```

## conda create