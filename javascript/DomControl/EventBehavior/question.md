## 発火イベントの振る舞い
以下のようなHTML構造と要素クリック後の処理を記述したJavaScriptがある。
```HTML
<div id="A">
  Blue
  <div id="B">
    Red
  </div>
  <div id="C">
    Green
  </div>
</div>
<div id="D">
  Yellow
</div>
```
```JavaScript
(function(){
  const targetA = document.getElementById('A');
  targetA.addEventListener('click', () => {
    targetA.innerHTML = 'Blue is clicked.';
  });
  const targetB = document.getElementById('B');
  targetB.addEventListener('click', () => {
    targetB.innerHTML = 'Red is clicked.';
  });
  const targetC = document.getElementById('C');
  targetC.addEventListener('click', () => {
    targetC.innerHTML = 'Green is clicked.';
  });
  const targetD = document.getElementById('D');
  targetD.addEventListener('click', () => {
    targetD.innerHTML = 'Yellow is clicked.';
  });
})();
```
このとき `Red` をクリックするとどのような画面表示になるか？ 以下の中から正しいものを1つ選びなさい。

1.
```
Blue
Red
Green
Yellow
```

2.
```
Blue
Red is clicked.
Green
Yellow
```

3.
```
Blue is clicked.
Yellow
```

4.
```
Blue
Red is clicked
Yellow
```

5. 何も表示されない
