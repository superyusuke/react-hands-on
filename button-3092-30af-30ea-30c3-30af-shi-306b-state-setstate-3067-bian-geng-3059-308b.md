# Button をクリック時に state をsetState で変更する

先ほど書いた App では、 state は用いているが、state を変更する仕組みはない。
さらに this.setState() を用いて state を変更する仕組みを追加する。

コード: [https://codesandbox.io/s/l52wlq708z](https://codesandbox.io/s/l52wlq708z)

```js
import React from "react";
import { render } from "react-dom";

class Human extends React.Component {
  constructor(props) {
    super(props);
    this.state = { name: "Nakanishi" };
  }

  render() {
    // onClick アトリビュートにコールバック(関数)を指定することで、
    // クリック時にメソッドを実行させることができる
    return <h2 onClick={this.onClickButton}>{this.state.name}</h2>;
  }

  // このメソッドを h2 クリック時に発動させる
  onClickButton = () => {
    // setState で state を更新する
    // this.setState() の引数には、変更したい state の対象を
    // オブジェクトで指定する
    this.setState({ name: this.state.name + "さん" });
  };
}

render(<Human />, document.getElementById("root"));

```

## onClick アトリビュートでクリック時に何かを実行させる

```js
import React from "react";
import { render } from "react-dom";

class Human extends React.Component {
  constructor(props) {
    super(props);
    this.state = { name: "Nakanishi" };
  }

  render() {
    // onClick アトリビュートにコールバック(関数)を指定することで、
    // クリック時にメソッドを実行させることができる
    return <h2 onClick={this.onClickButton}>{this.state.name}</h2>;
  }

  // このメソッドを h2 クリック時に発動させる
  // JSX の onClick, onChange, onSubmit に指定するメソッド(コールバック)
  // は、= () => というアローファンクションに似た方式で書くこと
  // そうしないと this が意図しない対象をさすためにエラーとなる
  onClickButton = () => {
    alert('click')
  };
}

render(<Human />, document.getElementById("root"));

```


