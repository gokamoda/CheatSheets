# povray on WSL2+Ubuntu22.04.01

## 目標
- povrayをUbuntu上にインストール
  - (個人的にWindows版PovrayのGUI,エディタが気に入らなかったため)
  - (Linux版の方がファイルサイズ小さそう)

## 前提
- [/WSL/init.md](/WSL/init.md)でUbuntuを導入済み
- 

## 手順
1. Povrayインストール
    ```Shell:Ubuntu
    sudo apt install povray
    ```
2. VSCodeの拡張機能をインストール
    ```SHell:Ubuntu
    code --install-extension jmaxwilson.vscode-povray
    ```

## 使い方
1. VSCodeで.povファイルを作成  
    例：
    ```POV-Ray SDL
    #include "colors.inc"
    #include "shapes.inc"

    camera {
      location <3, 5, -20> 
      look_at <0, 0, 0>
      angle 15  // viewing angle
    }

    light_source {
      <-3, 10, -7> color White
    }

    object {
      Sphere
      pigment { color Yellow }
    }
    ```
2. エディタ右上のpovrayマークをクリック
3. 処理が終わると画像が表示される