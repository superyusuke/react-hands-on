# Component の import / export

コード: https://codesandbox.io/s/zrp7jn76jm

動画: https://youtu.be/Tlopqjj7ejU

```js
// index.js

import React from 'react'
import { render } from 'react-dom'

import { FunctionalComponent } from './FunctionalComponent'
import { FunctionalComponent2 } from './FunctionalComponent2'

render(
  <FunctionalComponent2 name="Nakanishi" music="Jazz" />,
  document.getElementById('root')
)
```