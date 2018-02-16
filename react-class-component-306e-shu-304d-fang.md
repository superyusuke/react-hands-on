# React Class Component の書き方

コード: [https://codesandbox.io/s/my5z7665my](https://codesandbox.io/s/my5z7665my)

```js 
import React from "react";
import { render } from "react-dom";

class Human extends React.Component {
  constructor(props) {
    super(props);
    this.state = { name: "Nakanishi" };
  }

  render() {
    return <h2>{this.state.name}</h2>;
  }
}

render(<Human />, document.getElementById("root"));

```

## React.Component を拡張 = extends する

class 宣言から始まり constructor を持つ点は同じだが、加えて `extends React.Component` する必要がある。これによって単なるクラスではなく、React Component に必要な諸性質を受け継いだクラスを作成することができる。

さらに constructor は props を引数にとり、内部で `super(props)` も実行すること。`super(props)` により extends した元のクラスの性質を受け継ぐ。

```js
class Human extends React.Component {
  constructor(props) {
    super(props);
  }
}

```