## ネストしたチェックボックス

正解：以下の通り

```js
const parent = document.getElementsByClassName("parent-box")[0];
const children = document.querySelectorAll(".child-box");

function checkWholeState() {
  for(let child of children) {
    if(child.checked) return true;
  }
  return false;
}

parent.addEventListener('change', () => {
  const parentState = parent.checked;
  children.forEach((child) => {
    child.checked = parentState;
  });
});

children.forEach((child) => {
  child.addEventListener('change', () => {
    parent.checked = checkWholeState();
  });
});
```

ポイントは以下の3つ。
- 子項目がクリックされている状態にあるかどうかをチェックするメソッド(checkWholeState)を作成する
- 上記のメソッドを任意の子項目をONにした際に呼び出す
- 親のチェック状態は子項目のチェック状態に依存するため、親と子でチェック状態を共有する

実際に動作する様子は[こちら](https://codepen.io/narihiro/pen/VXZdjM)
