## 実行結果の推測（配列）
正解: `['a', 'b', '']`

以下、値の変化を記す。
```JavaScript
var array = new Array('a', 'b'); // array = ['a', 'b']
array[4] = 'c'; // array = ['a', 'b', '', 'c']
array.length = 3; // array = ['a', 'b', '']
console.log(array);
```
