# Basic Syntax

- [1. Links](#1-links)
  - [1.1. Embed](#11-embed)
  - [1.2. Link Definition](#12-link-definition)
- [2. Tables](#2-tables)
- [3. 数式](#3-数式)
  - [3.1. インライン](#31-インライン)
  - [3.2. 独立](#32-独立)

## 1. Links
### 1.1. Embed
```Markdown
[Google](https://www.google.com)
```

### 1.2. Link Definition
```Markdown
[Google][1]

[1]:https://www.google.com
```

## 2. Tables
```Markdown
| TH | TH |
| -- | -- |
| TD | TD |
| TD | TD |
| TD | TD |
```
| TH | TH |
| -- | -- |
| TD | TD |
| TD | TD |
| TD | TD |

## 3. 数式
基本記法はLaTeXと同じ．参考：`/LaTeX/math.md`  
ただしalign環境などは制限あり．
### 3.1. インライン
```Markdown
$y = ax^2$ は二次関数である．
```
$y = ax^2$ は二次関数である．

### 3.2. 独立
```Markdown
$$e^{i\pi} = -1$$
```
$$e^{i\pi} = -1$$



