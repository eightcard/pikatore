## 配列操作その1
以下に示すのは、与えられた配列Aに対し特定の条件に該当する要素のみを抽出し、新たな配列を作成するメソッドである。
このメソッドの処理が1行に収まるようにコードを書き換えなさい。

```javascript
function createPartialArray(A) {
  let partialArray = [];
  for(let i = 0; i < A.length; i++) {
    if(A[i] < 10) {
      partialArray.push(A[i]);
    }
  }
  return partialArray;
}
```
