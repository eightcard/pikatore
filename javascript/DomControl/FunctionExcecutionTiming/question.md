## 関数の実行タイミング
以下のようなHTMLとJavaScriptがある。
```HTML
<div id="list_wrapper">
  <ul>
    <li>Japan</li>
    <li>China</li>
    <li>America</li>
  </ul>
</div>
```

```js
(function(){
  const wrapper = document.getElementsByTagName('li');
  for(let wrap of wrapper) {
    if(wrap.innerHTML.includes('J')) {
      wrap.innerHTML = 'Jamaica';
    }
  }
})();

window.onload = () => {
  const wrapper = document.getElementsByTagName('li');
  for(let wrap of wrapper) {
    if(wrap.innerHTML === 'Japan') {
      wrap.innerHTML = 'Joker';
    }
  }
}
```

このとき、画面上の表示状態として正しいのは次のうちどちらか答えなさい。
1.
```
Joker
China
America
```

2.
```
Jamaica
China
America
```
