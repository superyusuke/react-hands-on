# State を持てる ReactComponent = StatefulComponent = React.Component = ClassComponent 

今まで書いてきた React の Component は、関数を使って書くもので、親「コンポーネントから受け取った Props」を元に自身の内容を規定するコンポーネントでした。

```js
const App = (props) => {
    return <h2>{props.name}</h2>
}
```


