# Arrow function 2

```js
import React from 'react'
import { render } from 'react-dom'

const renderReactElement = val => <button>{val}</button>

const renderReactElement2 = (val, no) => {
  const newString = `このボタンは${val}です。番号は${no}番です`
  return <button>{newString}</button>
}

const renderReactElement3 = array => {
  return array.map(item => {
    return <div>{item}</div>
  })
}

const array = ['tom', 'ken', 'jessy', 'catharine']

const reactElement = <div>{renderReactElement3(array)}</div>

render(reactElement, document.getElementById('root'))
```