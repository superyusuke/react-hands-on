# JSX と React Element について

https://codesandbox.io/s/mzw6xomm59
https://youtu.be/-8gRu19JTnM

```js
import React from 'react'
import { render } from 'react-dom'

const reactElement = <h2>こんにちは世界</h2>

console.log(reactElement)

render(reactElement, document.getElementById('root'))
```

## JSX は HTML でも JavaScript でもない

`<h2>こんにちは世界</h2>` という部分は、HTML でも JavaScript でもない。.js ファイルに HTML は書けないはずだし、JavaScript としては定義されていない謎の値、つまり変数でも関数でもオブジェクトでもない謎の文字であるので、JavaScript でもない。

ではなぜ機能するかというと、JSX を React が認識して、ReactElement にコンパイルしてくれて、結果 JavaScript のオブジェクトに変換してくれているから。

## JSX は React がコンパイルして、JavaScript のオブジェクトに変換してくれる

JSX は React がコンパイルして、JavaScript のオブジェクトに変換してくれるので、結果的には単なる JavaScript になっている。

そのため、変数に代入できる。

```js
const reactElement = <h2>こんにちは世界</h2>

```

