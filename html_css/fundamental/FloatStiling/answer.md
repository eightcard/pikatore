## スタイル定義
正解: 4
2つめの子要素のfloatが有効になったままのため、float指定されていない子要素を追加するとスタイルが崩れる。
そのため、以下のように `clear: both` を定義したブロックを2つめの要素と新しく追加する要素の間に挟むことにより、floatが解除され、
意図したスタイルが当たるようになる。
```css
.clear-fix {
  clear: both;
}
```
```html
<!-- ... 省略 ... -->
<div class="child-block-2"></div>
<div class="clear-fix"></div>
<div class="child-block-new"></div> <!-- 新しく追加する要素 -->
<!-- ... 省略 ... -->
```
