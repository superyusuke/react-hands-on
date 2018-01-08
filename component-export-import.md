# Component の import / export

コード: https://codesandbox.io/s/zrp7jn76jm

動画: https://youtu.be/Tlopqjj7ejU

```js
// FunctionalComponent.js

import React from 'react'

export const FunctionalComponent = props => {
  return (
    <div>
      Name: {props.name}, Music: {props.music}
    </div>
  )
}

```



```js
// FunctionalComponent2.js

import React from 'react'

export const FunctionalComponent2 = ({ name, music }) => {
  return (
    <div>
      Name: {name}, Music: {music}
    </div>
  )
}

```

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