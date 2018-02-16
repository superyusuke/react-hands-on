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

