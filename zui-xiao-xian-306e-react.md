# 最小限の React Application の実装

[動画](https://youtu.be/Gm4cpigN0bg)

## 必要のないものを消す

CodeSandBox で React を選んで起動した後に、必要のないファイル、コードを削除する。

* index.js の中身を全て消す
* hello.js をファイルごと削除

## 最小限の React App を実装する

ES2015\(ES6\) の記法である `import` を使って、javascript のモジュールを `index.js` の中で使えるようにするために、読み込む。

```js
// index.js
import React from 'react'
import { render } from 'react-dom'
```



