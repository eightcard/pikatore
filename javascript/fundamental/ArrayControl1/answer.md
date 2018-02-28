## 配列操作その1
正解：
以下の通り。
`filter` を用いて条件に合致するものを抽出するのがポイント。

```javascript
function createPartialArray(A) {
  return A.filter((current) => {if(current < 10) return true});
}
```

以下のように書くと、よりシンプルになる。
```js
function createPatialArray(A) {
  return A.filter(current => current < 10);
}
```
