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