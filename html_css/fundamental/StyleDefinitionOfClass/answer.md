## クラスに対するスタイル定義
両者のスタイル定義は意味するところが異なる。
```css
.sample_class .another_class {
  text-align: center;
}
```
`sample_class` というクラスを持つ要素の内部にある `another_class` というクラスを持つ要素に対してスタイルが反映される（以下参照）。
```html
<div class="sample_class">
  <div class="another_class"></div> <!--- ここにスタイルが当たる --->
</div>
```
```css
.sample_class.another_class {
  text-align: center;
}
```
`sample_class` と `another_class` という2つのクラスを持つ要素に対してスタイルが反映される（以下参照）。
```html
<div class="sample_class another_class"></div> <!-- ここにスタイルが当たる -->
```
