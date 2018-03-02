## 初期ロード時のデータ挿入

正解：以下の通り

```js
class ParentComponent extends React.Component {
  constructor() {
    super();
    this.state = {
      name: "",
      age: 0,
      hobby: "",
    };
  }

  // ここから解答
  componentDidMount() {
    this.setUserInfo();
  }
  // ここまで解答
  /*
    ユーザー情報を取得するメソッド
  */
  function getUserInfo() {
    /*　中の処理は省略　*/
  }

  /*
    ユーザー情報を設定するメソッド
  */
  function setUserInfo() {
    const userInfo = this.getUserInfo();
    this.setState({
      name: userInfo.name,
      age: userInfo.age,
      hobby: userInfo.hobby
    });
  }

  /* 以下省略 */
}
```

ライフサイクルメソッドを用いて制御をすることがポイント。<br>
本問の解答では `componentDidMount` を用いることにより、DOM描画後にデータをセットしている。<br>
ライフサイクルメソッドについては [こちら](https://qiita.com/aka_k_root/items/8ac3c33737709fa510cf) を参照のこと。
