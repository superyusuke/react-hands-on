# Water Component を作る 1

動画: [https://youtu.be/YXXQhy_YcbE](https://youtu.be/YXXQhy_YcbE)
コード: [https://codesandbox.io/s/n3pn5mqnj](https://codesandbox.io/s/n3pn5mqnj)

冒頭で紹介した Water コンポーネントを作成していきます。

このコンポーネントは、state で自身の温度を管理し、この温度によって表示する内容と、スタイルを更新する React App です。

温度は、+- ボタンで変更します。

```js
import React from "react";
import { render } from "react-dom";

// extends を忘れずに
class Water extends React.Component {
  constructor(props) {
    super(props);
    
    // 温度のための state 
    this.state = { temp: 15 };
  }

  render() {
    return (
      <div>
        // ボタンをクリックするとメソッドを発動
        <button onClick={this.onButtonPlus}>+</button>
        <button onClick={this.onButtonMinus}>-</button>
        <h2>{this.state.temp}</h2>
      </div>
    );
  }
  
  // アローファンクション風の書き方を忘れずに
  onButtonPlus = () => {
    this.setState({ temp: this.state.temp + 1 });
  };

  onButtonMinus = () => {
    this.setState({ temp: this.state.temp - 1 });
  };
}

render(<Water />, document.getElementById("root"));

```