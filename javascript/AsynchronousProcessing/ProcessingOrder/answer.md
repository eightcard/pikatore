## 非同期処理における処理の実行順

正解：2

```js
// APIアクセス時の処理本体
function processing(url) {
  return new Promise((resolve, reject){
    /* XMLHttpRequestオブジェクトを作成し、指定されたurlにアクセスする処理 */
  });
}

const url = '/sample/api';
console.log('process starts.'); // 処理A
processing(url).then((response) => {
  console.log('sucessed!!') // 処理B
}, (err) => {
  console.log('failed...') // 処理C
}).finally(() => {
  console.log('finally block'); // 処理D
});
console.log('process ends.'); // 処理E
```

本問では正常に処理が行われた場合の出力結果が問われているので、処理失敗時の `処理C` は実行されない。<br>
これを踏まえて、処理の実行順について以下に示す。

1. 非同期処理の呼び出しの前に出力処理が定義されているため、最初に `処理A` が実行される。
2. その後引数に指定されたurlにアクセスを行うが、戻り値がレスポンスとして返ってくる前に非同期処理の外側の処理が実行されるため、`処理E` が実行される。
3. 戻り値が返ってきて再度非同期処理のブロックに入る。正常に処理が行われた場合が問われているので、ここでは `処理B` が実行される。
4. `finally` は非同期処理終了時の挙動を定義するためのものなので、最後に`処理D`が実行される。なお、`finally`に記述した処理は成功時失敗時関わらず必ず最後に実行される。また、`処理E` は非同期処理のブロック外に定義されており、再度実行されることはない。

以上より、処理の実行順は `処理A` → `処理E` → `処理B` → `処理D` となり、2が正解となる。
