## Flex boxのスタイル定義
以下のようなhtmlとcssが定義されている。
```html
<div class="container">
  <div class="item A">item A</div>
  <div class="item B">item B</div>
  <div class="item C">item C</div>
</div>
```

```css
.container {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  align-content: center;
  align-items: center;
  background-color: #ffff00;
  width: 500px;
  height: 250px;
}

.item {
  flex: 0 1 auto;
  align-self: center;
  font-size: 24px;
  text-align: center;
  padding: 10px;
  background-color: #0f0;
  border: solid 1px #aaa;
}
```
これについて、以下の説明の中から不適切なものを1つ選びなさい。

1. `flex-basis` にautoが指定されているため、 アイテムの圧縮率を設定する `flex-shrink` の指定は実質無効になる
2. `flex-grow` を1に設定することで、3つの子要素は横幅の合計が親要素の横幅と同じになるようにサイズが調整される
3. paddingに固定値が指定されているため、 `justify-content: space-between` と変更しても何も変化しない
4. `flex-flow: row nowrap` は以下と同義である
```
flex-direction: row;
flex-wrap: nowrap;
```
5. `align-content` の指定は子要素が複数行に渡って配置された場合にのみ有効となる
