## 繰り返し構造の描画

以下に示すのは、あるサービスを利用しているユーザーの情報を表示する画面の書きかけのコードである。

```html
<!-- スタイル定義は省略 -->

<script>
  export default {
    name: "app",
    data() {
      return {
        usersInfo: {},
      }
    },
    methods: {
      getUsersInfo() {
        /* 複数のユーザー情報を取得するための処理 */
      }
    }
  }
</script>

<template>
  <div class="user-list-wrapper">
    <ul>
      <li><!-- ここにユーザー情報が入ってくる --></li>
    </ul>
  </div>
</template>
```
いま、画面ロード時にユーザー情報を取得し、表示する挙動を実現したいと考えている。<br>
未実装の箇所を補い、これを実現するようにコードを完成させなさい。
