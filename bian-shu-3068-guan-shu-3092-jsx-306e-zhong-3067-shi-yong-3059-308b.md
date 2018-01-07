# 変数と関数を JSX  の中で使用する
コード: https://codesandbox.io/s/k56vymvor
動画: Use variable and function in JSX

```js
import React from 'react'
import { render } from 'react-dom'

const title = 'こんにちは世界'
const body = 'こちらが本文の内容です'

const returnStrings = val => {
  return val
}

const reactElement = (
  <div>
    <h2>{title}</h2>
    <p>{body}</p>
    <p>{returnStrings('これが渡した引数です')}</p>
  </div>
)

console.log(reactElement)

render(reactElement, document.getElementById('root'))

```