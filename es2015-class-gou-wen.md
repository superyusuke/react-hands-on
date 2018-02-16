#ES2015 のクラス構文

動画: [https://youtu.be/gg-ivZEYsFA](https://youtu.be/gg-ivZEYsFA)
コード: [https://codesandbox.io/s/lln07164ym](https://codesandbox.io/s/lln07164ym)

```js
// class クラスネームで class を作成する
class Human {
  // constructor はクラスからインスタンスを作成した時に実行される
  constructor(name, age) {
    // this は作成されたインスタンスを指す
    this.name = name;
    this.age = age;
  }

  // クラスメソッド
  // クラスが持つファンクションのこと
  callMyProfile() {
    // 自分自身の値を参照するためにここでも this を使う
    console.log(this.name + this.age);
  }
}

// class からインスタンスを作成するために new 演算子を使う
// その際に引数も与える
const Nakanishi = new Human("Nakanishi", 33);

// console.log(Nakanishi.name);
// console.log(Nakanishi.age);

const Tanaka = new Human("Tanaka", 43);

// console.log(Tanaka.name);
// console.log(Tanaka.age);

// クラスメソッドにアクセスする
Nakanishi.callMyProfile();
Tanaka.callMyProfile();

```