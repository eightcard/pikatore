## 繰り返し構造の描画

正解：以下の通り

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
    mounted: () => {
      this.usersInfo = this.getUsersInfo();
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
    <ul v-for="userInfo in usersInfo">
      <li>{{userInfo}}</li>
    </ul>
  </div>
</template>
```

ポイントは次の2つ。
- `mounted` にDOM描画後の処理（今回の例であればユーザー情報取得）を定義している
- `<ul>`タグに`v-for`属性を指定し、配下の要素をリスト長分だけ描画を繰り返すようにしている
