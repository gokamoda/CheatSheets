# MacでGyazoコマンドを追加


## 割り当て詳細
| キーボード操作  |   挙動    |
| :-------------: | :-------: |
| control + ⇧ + c | Gyazo起動 |


## 方法
1.  `~/.config/karabiner/assets/complex_modifications`にjsonファイル新規作成
2.  以下を記述
    ```JSON
    {
      "title": "Gyazo",
      "rules": [
        {
          "description": "control+⇧+cでGyazo起動",
          "manipulators": [
            {
              "type": "basic",
              "from": {
                "simultaneous": [{ "key_code": "c" }],
                "modifiers": {
                  "mandatory": ["control", "shift"],
                  "optional": ["any"]
                }
              },
              "to": [{ "shell_command": "open -a 'Gyazo.app'" }]
            }
          ]
        }
      ]
    }
    ```
3.  Karabiner-Elementsを開き，`Complex modifications`タブを選択し，左下の`Add rule`をクリック
4.  `Gyazo`を有効化する