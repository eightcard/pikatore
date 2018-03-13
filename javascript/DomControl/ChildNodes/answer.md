## 子要素の取り出し
(1) 正解：変化する
`ul.children` を `ul.childNodes` としたとき、後者の場合DOMに加えて改行コードやテキストも取得対象となる。<br>
ここで、以下のコードを実行した際の実行結果を示す。
```javascript
const ul = document.getElementByTag('ul');
const children = ul.children; // or ul.childNodes
for(let i = 0; i < children.length; i++) {
  console.log(children[i].nodeName);
}
```

`children = ul.children`の場合
```
"LI"
"LI"
"LI"
"LI"
```

`children = ui.childNodes`の場合
```
"#text" → この部分が改行・スペース・テキストに相当する
"LI"
"#text"
"LI"
"#text"
"LI"
"#text"
"LI"
"#text"
```

(2) 正解：1
`querySelectorAll` を用いて引数に指定した値にマッチする要素を全て取得する。<br>
`querySelector` は該当する要素のうち最初のもののみを返すため、本問で行おうとしている処理としては不適切。<br>
`getElementByTagName` は引数にタグ名を1つのみ指定することができるため、不適切。
