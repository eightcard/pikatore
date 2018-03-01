## transitionの指定

CSSでアニメーションを実現するための手法であるCSS transitionについて以下の問に答えなさい。

(1) `transition` というプロパティは複数のプロパティをまとめて指定することができる記述形式である。<br>
いま、`transition: all 300ms 0s ease` としたとき、これと同義になるように、まとめられている各プロパティに分解した形でこのアニメーション定義を書き換えなさい。

(2) 以下のように、ある要素にマウスホバーした際に背景色と横幅が変化するような挙動が定義されているスタイルシートがある。

```CSS
.something {
  width: 200px;
  height: 100px;
  background-color: #ff0000;
}

.something:hover {
  background-color: #00ff00;
  width: 300px;  
}
```

ここに `transition: all 300ms 0s ease` という指定を追加し、変化が連続的に起こるようにしたい。<br>
このとき、上記の指定を追加する箇所として適切なのは次のうちどちらか。

1. `.something`配下
2. `.something:hover`配下
