## スタイル定義
以下のようなhtmlとcssが定義されている。
```html
<div class="parent-block">
  <div class="child-block-1"></div>
  <div class="child-block-2"></div>
</div>
```

```css
.parent-block {
  height: 100px;
  width: 200px;
  background-color: #00ff00;
}

.child-block-1 {
  display: inline-block;
  height: inherit;
  width: 50px;
  float: right;
  background-color: #ff0000;
}

.child-block-2 {
  display: inline-block;
  height: inherit;
  width: 50px;
  float: left;
  background-color: #0000ff;
}
```
上記のようなスタイル定義によって起こりうる問題として適切なものを次の中から1つ選びなさい。

1. float指定することにより要素は端に回り込むため、両端にmarginやpaddingが指定できなくなる
2. inline-blockが指定されている2つの子要素は、widthなどサイズの指定が無視されてしまう
3. 親要素のpositionにrelativeが指定されていないため、子要素は絶対配置となり親要素の外側に配置されてしまう
4. 親要素の内部でfloatが解除されていないため、float指定されていない子要素を追加するとスタイルが崩れてしまう
