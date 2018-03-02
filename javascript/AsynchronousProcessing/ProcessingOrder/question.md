## 非同期処理における処理の実行順

以下に示すコードは、あるAPIにアクセスした際の振る舞いを記述したものである。

```js

// APIアクセス時の処理本体
function processing(url) {
  return new Promise((resolve, reject){
    /* XMLHttpRequestオブジェクトを作成し、指定されたurlにアクセスする処理 */
  });
}

const url = '/sample/api';
console.log('process starts.');
processing(url).then((response) => {
  console.log('sucessed!!')
}, (err) => {
  console.log('failed...')
}).finally(() => {
  console.log('finally block');
});
console.log('process ends.');
```

このコードを実行し、エラーが発生せずに処理が正常に行われた場合の出力として正しいものを以下の中から選びなさい。

1.
```
process starts.
sucessed!!
finally block
process ends.
```

2.
```
process starts.
process ends.
sucessed!!
finally block
```

3.
```
process starts.
process ends.
sucessed!!
finally block
process ends.
```

4.
```
process starts.
process ends.
finally block
sucessed!!
process ends.
```
