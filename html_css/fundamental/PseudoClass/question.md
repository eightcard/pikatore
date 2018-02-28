## 疑似クラスによるスタイル定義
以下のようなボタンが定義されている

```html
<button class="sample_button"></button>
```

これに対し、以下のようなスタイルが定義されている。
```css
.sample_button {
  width: 100px;
  height: 30px;
  font-size: 20px;
  background-color: #44ff98;
  border-radius: 9999px;
  cursor: pointer;
  transition: ease 0.5s;
}

.sample_button:hover {
  background-color: #ff4455;
}

.sample_button:active {
  width: 150px;
}
```
このとき、ボタンをクリックしたままボタンからカーソルを外すとどのような外観になるか。<br>
正しいものを次のうちから選びなさい。

1. 背景色、横幅の両者が初期状態に戻る
2. 背景色は戻らないが横幅は初期状態に戻る
3. 横幅は戻らないが背景色は初期状態に戻る
4. 背景色、横幅ともに変化したまま変わらない
