# map と filter の実例

動画: [https://youtu.be/fUdJqDh5b1o](https://youtu.be/fUdJqDh5b1o)
コード: [https://codesandbox.io/s/llrylwq88q](https://codesandbox.io/s/llrylwq88q)

```js
import React from "react";
import { render } from "react-dom";

const todos = [
  { id: 1, title: "title1" },
  { id: 2, title: "title2" },
  { id: 3, title: "title3" },
  { id: 4, title: "title4" },
  { id: 5, title: "title5" },
  { id: 6, title: "title6" }
];

const targetDeleteId = 4;

// id が 4の要素だけ削除した配列を新たに作る
const deletedTodos = todos.filter(todo => {
  return todo.id !== targetDeleteId;
});

console.log(deletedTodos);

// React Component
// 引数として受け取った配列を元に、reactElement の配列を作成するコンポーネント
const TodoList = ({ todos }) => {
  return todos.map(todo => {
    return (
      <li>
        #{todo.id} title:{todo.title}
      </li>
    );
  });
};

render(
  // todos の配列をコンポーネントに渡す
  <ul>
    <TodoList todos={todos} />
  </ul>,
  document.getElementById("root")
);

```