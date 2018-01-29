## DOMの入れ替え
正解：2

初期状態が以下のようであったとする。
![初期状態](images/before.png "初期状態")

1の処理では `primal_child` 指定の要素の内部に `alternative_child` 指定の要素を挿入していることになる(以下参照)。
![誤り](images/after_wrong.png "誤り")

そこで、2のように子要素を `removeChild` を用いて削除し、新たなDOMを挿入する必要がある。
これにより、要素は以下のような外観になる。
![正解](images/after_right.png "正解")
