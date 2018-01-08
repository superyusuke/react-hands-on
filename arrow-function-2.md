# Arrow function 2

動画: https://youtu.be/JqBjW_nCgOk
コード: https://codesandbox.io/s/nkq03xl2p

```js
import React from 'react'
import { render } from 'react-dom'

// JSX で書いた ReactElement を返す
const renderReactElement = val => <button>{val}</button>

// 引数を元に文字を合成して、それを用いた ReactElement を返す
const renderReactElement2 = (val, no) => {
  const newString = `このボタンは${val}です。番号は${no}番です`
  return <button>{newString}</button>
}

// 引数として配列を受け取って、それを元に複数の ReactElement を返す
const array = ['tom', 'ken', 'jessy', 'catharine']

const renderReactElement3 = array => {
  // map については後述
  return array.map(item => {
    return <div>{item}</div>
  })
}

const reactElement = <div>{renderReactElement3(array)}</div>

render(reactElement, document.getElementById('root'))
```