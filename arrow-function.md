# Arrow function

Arrow function は　ES2015 以降の関数を定義するためのシンタックス。

```js
const returnStrings = () => {
  return 'val'
}

const returnStrings1 = (val) => {
  return val
}

const returnStrings2 = val => {
  return val
}

const returnStrings3 = val => val


const returnStrings4 = function(val) {
  return val
}
```