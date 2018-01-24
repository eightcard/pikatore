## 配列操作その2
正解:
以下の通り。
`reduce` を用いると、配列全体を1つの値に集約することができる。
```javascript
function getSum(A) {
  return A.reduce((a, b) => a + b);
}
```
