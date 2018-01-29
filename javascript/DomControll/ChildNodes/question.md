## 子要素の取り出し
以下のような構造のHTMLがある。
```HTML
<ol>
  <li>Dog</li>
  <li>Cat</li>
  <li>Mouse</li>
  <li>Bird</li>
</ol>
<ul>
  <li>Apple</li>
  <li>Banana</li>
  <li>Grape</li>
  <li>Orange</li>
</ul>
```
また、「ul配下のliを全て取り出す」処理として以下のようにJavaScriptを記述したとする。
```javascript
const ul = document.getElementByTag('ul');
const children = ul.children;
```

このとき、次の問に答えなさい。

(1) `ul.children` を `ul.childNode` としたとき、取得結果は変化するか否かを答えなさい。<br>
    変化する場合はどのように変化するかも付け加えること。

(2) 上記のような処理を実現するために他にどのような処理が考えられるか。<br>
    以下の中から適切なものを選びなさい。

1.
```JavaScript
document.querySelector(ul, li);
```

2.
```JavaScript
document.querySelector(li);
```

3.
```JavaScript
document.getElementByTagName(ul, li);
```

4.
```JavaScript
document.getChildElement(ul);
```
