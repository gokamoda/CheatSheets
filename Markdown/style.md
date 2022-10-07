# Markdownで便利なStyle（CSS）

- [1. 画像中央揃え](#1-画像中央揃え)
  - [1.1. Github非対応(HTML)](#11-github非対応html)
  - [1.2. Github対応](#12-github対応)




## 1. 画像中央揃え

### 1.1. Github非対応(HTML)
```HTML
<style>
  img{
    margin: 0 auto;
    display: block;
  }
</style>
<img src="xxx.png">
```

### 1.2. Github対応
```Markdown
<p align="center">
  <img src="xxx.png">
</p>
```