## 初期ロード時のデータ挿入

以下に示すコードは、ユーザーの名前、年齢、趣味を表示するページのコンポーネントである。

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

  render() {
    return(
      <ChildComponent
        name={this.state.name}
        age={this.state.age}
        hobby={this.state.hobby}
        onClick={} />
    )
  }
}

const ChildComponent = (props) => {
  return(
    <div className=''>
      <p className='name'>
        name: {props.name}
      </p>
      <p className='age'>
        age: {props.age}
      </p>
      <p className='hobby'>
        hobby: {props.hobby}
      </p>
      <button ></button>
    </div>
  );
}
```

いま、画面の初期ロード時にユーザー情報を取得し、それを画面に表示する挙動が未実装となっている。<br>
このとき、前述した挙動を実現するようにコードを改変しなさい。
