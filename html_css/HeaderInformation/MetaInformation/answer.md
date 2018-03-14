## メタ情報

(1) 正解：以下の通り。

#### 誤っている箇所
- 2行目の記述。`charset`属性が指定されている場合は`name`属性を指定すべきではない。
- 6行目の記述。`http-equiv`属性の`content-language`という値は現在は廃止されている。したがって、`html`に`lang`属性を指定すべきである。

以上を踏まえて正しい形に書き直すと以下のようになる。
```html
<html lang="ja">
  <head>
    <title>sampleサービス - ご案内</title>
    <meta charset="UTF-8">
    <meta name="description" content="いつもあなたのそばに。〇〇なサービスの紹介ページです。">
    <meta name="keywords" content="人材,派遣,">
    <meta name="author" content="Takeshi Yamada">
    ...

```

(2) 正解：以下の通り。
```html
<html lang="ja">
  <head>
    <title>sampleサービス - ご案内</title>
    <meta charset="UTF-8">
    <meta property="og:description" content="いつもあなたのそばに。〇〇なサービスの紹介ページです。">
    <meta property="og:title" content="sampleサービス">
    <meta property="og:type" content="website">
    <meta property="og:image" content="https://hoge.jp/contents/images/sample.png">
    <meta property="og:site_name" content="ご案内">
    <meta name="keywords" content="人材,派遣,">
    <meta name="author" content="Takeshi Yamada">
  ...

```
このうち、`og:site_name`以外の属性はすべて必須情報である。OGPについては[こちら](http://ogp.me/)を参照のこと。

(3) 正解：以下の通り
```html
<html lang="ja">
  <head>
    <title>sampleサービス - ご案内</title>
    <meta charset="UTF-8">
    <meta name="description" content="いつもあなたのそばに。〇〇なサービスの紹介ページです。">
    <meta name="keywords" content="人材,派遣,">
    <meta name="author" content="Takeshi Yamada">
    <meta http-equiv="refresh" content="3; url=https://hoge.jp/service-new">
    ...

```
`http-equiv`属性に`refresh`を設定することがポイント。  
なお、`content`属性に`;url`以下の文字列を指定しない場合、このページは3秒後に再読込が行われる。

参考：https://developer.mozilla.org/ja/docs/Web/HTML/Element/meta
