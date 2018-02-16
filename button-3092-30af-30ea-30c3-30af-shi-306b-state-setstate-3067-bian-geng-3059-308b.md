# Button をクリック時に state をsetState で変更する

先ほど書いた App では、 state は用いているが、state を変更する仕組みはない。

さらに this.setState() を用いて state を変更する仕組みを追加する。

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
