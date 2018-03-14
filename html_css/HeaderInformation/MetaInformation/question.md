## メタ情報

HTML5の`<meta>`タグについて以下の問に答えなさい。  

(1) `https://hoge.jp/service`というURLをもつあるページのhtmlに以下のように`<meta>`タグを設定した。
```html
<html>
  <head>
    <title>sampleサービス - ご案内</title>
    <meta name="charset" charset="UTF-8">
    <meta name="description" content="いつもあなたのそばに。〇〇なサービスの紹介ページです。">
    <meta name="keywords" content="人材,派遣,">
    <meta name="author" content="Takeshi Yamada">
    <meta http-equiv="content-language" content="ja">
    ...

```

上記の記載の中には誤りがある。それを指摘し、正しい形式に書き直しなさい。

(2) サービス認知度向上の一環として、SNS上でこのページがシェアされた際の表示に画像を含め、リッチにさせたい。このとき、(1)の解答のHTMLを適切な形に書き直しなさい。なお、ページの種別は`website`、表示の際に用いる画像のパスは `https://hoge.jp/contents/images/sample.png` とする。

(3) ページを新しく作り直したため、現在使用しているページにアクセスがあった際に以下のような条件で新ページにリダイレクトさせたい。このとき、(1)の解答のHTMLを適切な形に書き直しなさい。

- 新しいページのURL: https://hoge.jp/service-new
- 上記のURLに3秒後に自動でリダイレクト
