# そもそもオブジェクトとは何か

```js
// object の役割は配列に似ている
// 複数の値を入れることができる「入れ物」のような仕組みを提供する

// object は {} で作成する

// 中身は、
// key1: '値1', key2: '値2', key3: '値3' という「key」と「値」の組み合わせを
// コンマで区切ったもの

// この「key: 値」1セット値をプロパティと呼ぶ
const obj = {
  key1: "value1",
  key2: "value2",
  key3: "value3"
};

// object は配列に似ている
// 複数の値をまとめて保持できる
const array = ["value1", "value2", "value3"];
console.log(array);
console.log(array[0]);

// 先ほど作成したオブジェクトの中身にアクセスする
// オブジェクト名.keyの名前でアクセス可能
console.log(obj.key1);
console.log(obj.key2);
console.log(obj.key3);
// オブジェクト全体を表示する
console.log(obj);

// 具体的なオブジェクトの使用方法
const obj1 = {
  key: "value",
  name: "nakanishi",
  music: "jazz",
  weather: "rainy"
};

// オブジェクト名.key名でアクセスする
console.log(obj1.key);
console.log(obj1.name);
console.log(obj1.music);
console.log(obj1.weather);
console.log(obj1);

// オブジェクトの値には、配列を持たせることも当然できる
// どんな値を持たせることもできる
const obj2 = {
  nameList: ["nakanishi", "Hurukawa", "Tanaka"],
  musicList: ["jazz", "classic", "funk"]
};

console.log(obj2.nameList);
console.log(obj2.musicList);
console.log(obj2);

// オブジェクト内のプロパティの配列にアクセスする
console.log(obj2.nameList[0]);
console.log(obj2.nameList[1]);
console.log(obj2.nameList[2]);

// オブジェクトの値には、さらにオブジェクトをを持たせることも当然できる
const obj3 = {
  nameObject: {
    japan: ["nakanishi", "ohara", "suzuki"],
    america: ["john", "yoko", "ringo"],
    spain: ["abel", "carlos"]
  },
  musicObject: {
    jazz: ["miles", "bill", "latif"],
    classic: ["back", "chopin", "schoenberg"]
  }
};

console.log(obj3.nameObject);
console.log(obj3.nameObject.japan);
console.log(obj3.nameObject.japan[0]);

```