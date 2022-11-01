# onOpen()

カスタムメニューの作成

```JavaScript
function onOpen() {
  SpreadsheetApp.getUi()
      .createMenu('カスタム処理')
      .addItem('<表示文字列>', '<関数名>') // 書き方
      .addItem('処理', 'myFunction') // 例
      .addToUi();
}

function myFunction(){}
```