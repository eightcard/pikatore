## 発火イベントの振る舞い
正解：3

問題のHTMLでは、 `Red` と `Green` が `Blue` の子要素として定義されている。<br>
このとき `Red` をクリックすると、クリックイベントが親要素である `Blue` に伝搬(バブリング)する。<br>
そのため、最終的に `Blue` に対して付与されたクリックイベントが発火する。<br>
`Blue` は文字列だけではなく `Red` と `Green` も内包しているため、 `innerHTML` メソッドにより
これらが `Blue is clicked` に置き換わる。<br>
ちなみに、`Red`をクリックした際のコールバックとして以下のように`stopPropagation`を呼び出すと、親要素へのイベントの伝播が抑止され、本問の選択肢の2のような表示になる。
```js
const targetB = document.getElementById('B');
targetB.addEventListener('click', (event) => {
  event.stopPropagation();
  targetB.innerHTML = 'Red is clicked.';
});
```
