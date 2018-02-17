# map と filter

## map

map の動画: [https://youtu.be/rUwpPZSw9Dg](https://youtu.be/rUwpPZSw9Dg)
map のコード: [https://codesandbox.io/s/4l3y7l14j7 ](https://codesandbox.io/s/4l3y7l14j7)

```js
const array1 = ["nakanishi", "Hurukawa", "Tanaka"];

console.log(array1);

const newArray1 = array1.map((o, i) => {
  return `${o}さんは${i}番目`;
});

console.log(newArray1);

// 配列.map(ここに入れるものがある)
// (各配列の値, 順番) => { return 新しい配列の中身}

// 結果
const 配列 = [1, 2, 3, 4, 5, 6];
const 新しい配列 = 配列.map((各配列の値, 順番) => {
  return `新しい配列の中身は ${各配列の値} 順番は${順番}`;
});

console.log(新しい配列);

```

filter の動画: [https://youtu.be/RCy2hz0xC-Y](https://youtu.be/RCy2hz0xC-Y)
filter のコード: [https://codesandbox.io/s/1q39zvq6j](https://codesandbox.io/s/1q39zvq6j)

```js
const array1 = ["nakanishi", "Hurukawa", "Tanaka"];

const newArray1 = array1.filter((o, i) => {
  // true が return された時の配列の中身だけが残されて
  // 新しい配列に使われる
  return o === "nakanishi";
});

console.log(newArray1);

const newArray2 = array1.filter((o, i) => {
  // true が返された時の配列の中身だけが使われる
  // ここでは文字の長さが7より大きい時のみ使われる
  return o.length > 7;
});

console.log(newArray2);

// 具体的な使用例

const array3 = [
  { name: "nakanishi", engineer: true },
  { name: "yoshida", engineer: false },
  { name: "sasaki", engineer: true },
  { name: "furukawa", engineer: false }
];

const newArray3 = array3.filter((o, i) => {
  return o.engineer;
});

console.log(newArray3);
```
