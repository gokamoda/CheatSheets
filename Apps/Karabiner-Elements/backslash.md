# Macでバックスラッシュを打ちやすくする


## 割り当て詳細
### Before
| キーボード操作 | 挙動  |
| :------------: | :---: |
|       _        |   _   |
|     ⇧ + _      |   _   |

### After
| キーボード操作 | 挙動  |
| :------------: | :---: |
|       _        |   \   |
|     ⇧ + _      |   _   |


## 方法
1.  `~/.config/karabiner/assets/complex_modifications`にjsonファイル新規作成
2.  以下を記述
    ```JSON
    {
    "title": "backslash",
    "rules": [
        {
        "description": "underscore to backslash",
        "manipulators": [
            {
            "from": {
                "key_code": "international1"
            },
            "to": [{
                "key_code": "international3",
                "modifiers": [ "option" ]
            }],
            "type": "basic"
            }
        ]
        }
    ]
    }
    ```
3.  Karabiner-Elementsを開き，`Complex modifications`タブを選択し，左下の`Add rule`をクリック
4.  `underscore to backslash`を有効化する