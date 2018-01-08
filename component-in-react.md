# React における Component

## 一般的に Component とは

![](/assets/react-component.001.png)

Component とは、input (入力) を受け取って、それを元に Operation (なんらかの操作) をした結果を、Output (出力) する部品のこと。

これを組み合わせて、より大きなアプリケーションを構築する。

## React における Component

React におけるコンポーネントは、基本的には React Element を返す単なる  Function です。ただし、ファンクションとは異なるのは、名前の冒頭が大文字でなければいけないことと、使用する際には `<Component />` とカスタムタグのように記述することです。

```js

// 単なる関数
const renderElement = () => {
  return (
    <div>
      Name: Music:
    </div>
  )
}

// 関数なので以下のように実行して使う
// renderElement()

// 全く同じ内容のまま、冒頭を大文字にする
const RenderElement = () => {
  return (
    <div>
      Name: Music:
    </div>
  )
}

// Component なので以下のようにタグを記述して使う
// <RenderElement />
```

## Input を受け取る

ただし、単に React Element を返すだけでは、広義の Component とはいえませんし、あまり便利ではありません。では Input を受け取って、それを元に Output する Component としてを作成してみましょう。

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

render(
  <FunctionalComponent name="Nakanishi" music="Jazz" />,
  document.getElementById('root')
)
```
aaa

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

