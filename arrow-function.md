# Arrow function

Arrow function は　ES2015 以降の関数を定義するためのシンタックス。
以下は、ほぼ同じ効果。

```js
// 基本形 これで全部書いてもらっても OK
// 引数がない場合は、必ず () が必要
const returnStrings = () => {
  return 'val'
}

// 引数が一つの時は () があってもいい
const returnStrings1 = (val) => {
  return val
}

// 引数が一つの時は () がなくてもいい
const returnStrings2 = val => {
  return val
}

// return を省略するには、{} も return もなくしていい。
const returnStrings3 = val => val

// ただし、以下のように return 以外の式がある場合は、原理的に { return } を省略できない。
const returnStrings3 = val => {
  const name = 'Nakanishi'
  return val + name
}



// 伝統的なファンクションの宣言
const returnStrings4 = function(val) {
  return val
}
```

