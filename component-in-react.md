# React における Component

## Component とは

![](/assets/react-component.001.png)

Component とは、input (入力) を受け取って、それを元に Operation (なんらかの操作) をした結果を、Output (出力) する部品のこと。

これを組み合わせて、より大きなアプリケーションを構築する。

## React における Component

```js
import React from 'react'
import { render } from 'react-dom'

const FunctionalComponent = props => {
  return (
    <div>
      Name: {props.name}, Music: {props.music}
    </div>
  )
}

const FunctionalComponent2 = ({ name, music }) => {
  return (
    <div>
      Name: {name}, Music: {music}
    </div>
  )
}

class ClassComponent extends React.Component {
  render() {
    return (
      <div>
        Name: {this.props.name}, Music: {this.props.music}
      </div>
    )
  }
}

render(
  <ClassComponent name="Nakanishi" music="Jazz" />,
  document.getElementById('root')
)
```

