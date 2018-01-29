## 子要素の取り出し
(1) 正解：変化する
`ul.children` を `ul.childNode` としたとき、後者の場合DOMに加えて改行コードやテキストも取得対象となる。

(2) 正解：1
`document.querySelector` を用いて親要素と子要素を引数に指定する。<br>
`getElementByTagName` は引数にタグ名を1つのみ指定することができるため、不適切。
