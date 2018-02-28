## 疑似クラスによるスタイル定義
正解：3

カーソルはボタン上から外れているため、 `:hover` のスタイルは無効になる。つまり、2と4は不適切。<br>
また、ボタンをクリックしたままのため、 `:active` のスタイルは適用されたままになる。よって3が正解。<br>
ちなみに、疑似クラスには以下のようなものが用意されている。

|値 |説明 |
|---|----|
|:active               |指定している状態                  |
|:checked              |チェックされた状態                 |
|:disabled             |無効な状態                       |
|:empty                |内部に子要素を持たない             |
|:enabled              |有効状態                         |
|:first-child          |最初の子要素                     |
|:first-of-type        |兄弟関係にある最初の要素           |
|:focus                |フォーカスを合わせている状態        |
|:hover                |マウスカーソルがホバーしている状態   |
|:last-child           |最後の子要素                     |
|:last-of-type         |兄弟関係にある最後の要素           |
|:link                 |未訪問のリンク先へのアンカー        |
|:nth-last-child(n)    |後ろからn番目の子要素              |
|:nth-last-of-type(n)  |後ろからn番目にある要素            |
|:nth-of-type(n)       |n番目にある要素                   |
|:only-child           |唯一の子要素                      |
|:only-of-type         |子要素の中で唯一の要素             |
|:root                 |文章内のルート要素                 |
|:target               |URIの#アンカー名と一致する          |
|:visited              |訪問先のリンク先へのアンカー         |

参照：http://illarena.com/programming/css/pseudo-class/
