# Arrayメソッド

## 練習問題1

### ヒント

1. [コールバック関数の返り値について](#1-コールバック関数の返り値について)
2. [コールバック関数でオブジェクトを直接返すやり方について](#2-コールバック関数でオブジェクトを直接返すやり方について)

#### 1. コールバック関数の返り値について

今回の問題は`map`メソッドを使用するので以下のような形になるかと思います。

```javascript
const newArray = array.map((val) => コールバック関数の返り値);
```

この時、コールバック関数の返り値にはどんな記述をすれば良いかということを考えていきます。

まず今回コールバック関数の引数`val`にはどんな値が入ってくるか確認してみましょう。  
以下の記述を追加して実行してみてください。

```javascript
const newArray = array.map((val) => console.log(val));
```

以下のように出力されるかと思います。

```terminal
{ tag: 'p', className: 'hoge' }
{ tag: 'div', className: 'fuga' }
{ tag: 'h1', className: 'piyo' }
```

`const array`の配列の1つ1つの要素が表示されていることがわかるかと思います。

ここで例えば、`console.log(val)`としていたところを以下のように変更して実行結果を確認してみましょう。

```javascript
const newArray = array.map((val) => 'c-' + val.className);
console.log(newArray)
```

結果は以下のようになるかと思います。

```terminal
[ 'c-hoge', 'c-fuga', 'c-piyo' ]
```

`const array`の配列の1つ1つの要素が`c-`の接頭辞がついた"文字列"になったことがわかるかと思います。

今は、文字列を返すようにしてみましたが、実際に表示させたいのは、1つ1つの要素がオブジェクトの形になります。  
なので、後はオブジェクトを返すようにして、カリキュラムにあるような形にするだけです！

#### 2. コールバック関数でオブジェクトを直接返すやり方について

コールバック関数でオブジェクトを直接返すやり方は以下のようになります。

```javascript
const newArray = array.map((val) => ({}));
```

`()`が`{}`の外に必要になります。  
これは、あくまで今はコールバック関数を定義しているためです。  
例えば、オブジェクトを返したいと思って

```javascript
const newArray = array.map((val) => { ・・・ });
```

のように記述してしまうと、`{}`は関数の`{}`として認識されてしまうことになるのでNGです。

ここで、もしオブジェクトを返すという記述を関数の中に書くとしたら、以下のように記述します。

```javascript
const newArray = array.map((val) => { return {}; });
```

ただ、省略記法が用意されているので、以下の記述でオブジェクトを返すことができるということになります！

```javascript
const newArray = array.map((val) => ({}));
```
