## 実行結果の推測（変数への代入）
以下の通り
```JavaScript
function f() {
  value = 5;
}
var a = f(); // aはundefinedになる
```
`f()` は `value` というグローバル変数に対して代入するだけの関数であり、戻り値はない（厳密にはundefinedがreturnされる）。
したがって、aの値は `undefined` となる。
