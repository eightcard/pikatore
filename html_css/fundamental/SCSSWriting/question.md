## SASSによるスタイル定義
以下に示すスタイル定義の組み合わせのうち、aとbが同義にならないものはどちらか答えなさい。

1.
```sass
/** a **/
$red: #f00;
$blue: #00f;

.container {
  width: 300px;
  height: 150px;
  backgrount-color: $red;
  &-extention {
    width: 200px;
    height: 100px;
    background-color: $blue;
  }
}

/** b **/
@mixin extention-box($width:200px, $height:100px, $bg_color: #00f) {
  width: $width;
  height: $height;
  background-color: $bg_color;
}

.container {
  width: 300px;
  height: 150px;
  background-color: #f00;
}

.container-extention {
  @include extention-box();
}
```

2.
```sass
/** a **/
$red: #f00;
$blue: #00f;

.container {
  width: 300px;
  height: 150px;
  background-color: $red;
  & .extention {
    width: 200px;
    height: 100px;
    background-color: $blue;
  }
}

/** b **/
$red: #f00;
$blue: #00f;

.container {
  width: 300px;
  height: 150px;
  background-color: $red;
}

.container.extention {
  width: 200px;
  height: 100px;
  background-color: $blue;
}
```
