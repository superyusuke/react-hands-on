# map と filter

mapのコード: [https://codesandbox.io/s/4l3y7l14j7 ](https://codesandbox.io/s/4l3y7l14j7)

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