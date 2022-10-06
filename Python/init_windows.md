# WindowsでPython

- [1. pyenvのインストール](#1-pyenvのインストール)
- [3. Pythonのインストール](#3-pythonのインストール)
- [3. コードを書く](#3-コードを書く)

## 1. pyenvのインストール
- 参考：https://github.com/pyenv-win/pyenv-win

1. 管理者権限でPowerShellを起動
2. アクセス許可
   ```PowerShell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
   ```
3. インストール
   ```PowerShell
   Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
   ```
3. ユーザー環境変数の追加
   1. PYENV
      ```PowerShell
      [System.Environment]::SetEnvironmentVariable('PYENV',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
      ```
   2. PYENV_ROOT  
      ```PowerShell
      [System.Environment]::SetEnvironmentVariable('PYENV_ROOT',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
      ```
   3. PYENV_HOME
      ```PowerShell
      [System.Environment]::SetEnvironmentVariable('PYENV_HOME',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
      ```
   4. PATHの追加
      ```PowerShell
      [System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv\pyenv-win\bin;" + $env:USERPROFILE + "\.pyenv\pyenv-win\shims;" + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
      ```
4. PCの再起動
5. インストールの確認
     ```cmd
     pyenv --version
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

## 3. コードを書く
- VSCodeで書く
- 詳しくは`/VSCode/python.md`