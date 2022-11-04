# Macでバックスラッシュを打ちやすくする

- [1. 注意](#1-注意)
- [2. 割り当て詳細](#2-割り当て詳細)
  - [2.1. Before](#21-before)
  - [2.2. After](#22-after)
- [3. 方法](#3-方法)

## 1. 注意
- LogiOptionsと同時に使用すると競合する．
- 代替案としてHammerSpoonの利用を推奨する．

## 2. 割り当て詳細
### 2.1. Before
| キーボード操作 | 挙動  |
| :------------: | :---: |
|       _        |   _   |
|     ⇧ + _      |   _   |

### 2.2. After
| キーボード操作 | 挙動  |
| :------------: | :---: |
|       _        |   \   |
|     ⇧ + _      |   _   |


## 3. 方法
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