# WSL+UbuntuでPython

- [1. 前提](#1-前提)
- [2. pyenvの導入](#2-pyenvの導入)

## 1. 前提
- [/WSL/init.md](/WSL/init.md)でUbuntuを導入済み

## 2. pyenvの導入
1. Ubuntuのbashを開く
2. pyenvのインストール
   ```bash
   curl https://pyenv.run | bash
   ```
3. .bashrcに以下を追記
   ```.bashrc
   export PYENV_ROOT="$HOME/.pyenv"
   command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
   eval "$(pyenv init -)"
   ```
4. インストールの確認
   ```bash
   pyenv --version
   ```
   