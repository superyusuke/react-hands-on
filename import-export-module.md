# import, export, module

コード: https://codesandbox.io/s/3r18wykwqm
動画: https://youtu.be/sginHtoyza4 

```js
// hello.js
// export する側

import React from 'react'

// 変数
export const hello = 'hello'

// function
export const hello2 = () => 'hello2'

// function (return reactElement)
export const hello3 = () => <h2>hello3</h2>

// React Component
export const Hello4 = () => <h2>hello4</h2>


```

```js
// index.js
// 出力する側

import React from 'react'
import { render } from 'react-dom'
import { Hello4, hello3, hello2, hello } from './hello'

console.log('hello', hello)

console.log('helllo2', hello2())

//render(hello3(), document.getElementById('root'))

render(<Hello4 />, document.getElementById('root'))

```

## import は別ファイルに切り出した JavaScript(module) から変数、関数、クラス等を読み込むための宣言

変数、関数、クラス等を、別ファイルに切り出し、それを読みこむために import を使う。また出力する側では export をしておく。

- 出力する側で変数、関数、クラスの前に `export` をつける。
- 読み込む側では、`import` {名前} `from` 'ファイル名' とする。
- この場合のファイル名は、hello のように、拡張子をつけなくていい。
- 

