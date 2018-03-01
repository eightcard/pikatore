## transitionの指定

正解：以下の通り

```
transition-property: all;
transition-duration: 300ms;
transition-delay: 0s;
transition-timing-function: ease;
```
### transition-property
どのプロパティに対してアニメーションを適用するかを指定する。<br>
今回の例では `all` が指定されているため、全てのプロパティに対して適用される。

### transition-duration
アニメーションの開始から終了までの時間を指定する。<br>
今回の例では `100ms` が指定されているため、開始から終了までの間が100msとなる。

### transition-delay
アニメーションが開始されるまでの時間を指定する。<br>
今回の例では `0s` となっているため、開始までの遅延がない。

### transition-timing-function
アニメーションのイージング（進み具合）を指定する。
今回の例では `ease` が指定されているため、開始から終了までが緩やかな曲線となる。<br>
参考：http://cubic-bezier.com/#.17,.67,.83,.67
