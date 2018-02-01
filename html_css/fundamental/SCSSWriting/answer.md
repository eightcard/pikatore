## SCSSによるスタイル定義
正解: 2

2のaでは `.container` の子要素である `.extention` に対してスタイルを定義しているが、bでは `.container.extention` というクラスに対しての定義になっている。<br>
ちなみに、2のaは以下のようにも書き換えられる。
```sass
$red: #f00;
$blue: #00f;

.container {
  width: 300px;
  height: 150px;
  background-color: $red;
  .extention {
    width: 200px;
    height: 100px;
    background-color: $blue;
  }
}
```
