# オンラインツールで簡単！ プログラミング体験会・ハンズオン

このハンズオンでのゴールは**コーディングってどんなもの**を実際に体験することです。
CodePenを使って、実際に手を動かしてみましょう。

## HTMLを書いてみよう

今日はHTMLとCSSを体験してみます。
実際本格的に書こうと思ったら細かいルールなどがありますが、本日は割愛します。
楽しくコードを書くのが今日のゴールです！

### HTMLってなーに？

* HTMLとは、Webページ上の文章を書くための言語
* 機械に対して、文章をよりわかりやすく見せてあげることがHTMLの役目

## 実際手を動かしてみよう

初心者でも優しい、**Emmet**という機能があります。今日はこれを使ってコーディングします。
HTMLやCSSのコードを書くことをコーディングといいます。

[HTML&CSSの完成イメージとコード](https://codepen.io/camillenexseed/pen/WNegpQr)

## 見出しタグを書いてみよう！

### 見出しタグってなーに？

見出しタグはHTMLの中でとっても重要なタグ。
> ユーザーや検索エンジンにページの重要なテーマを伝えるために、HTMLでマークアップするhタグ（h1/h2/h3/h4/h5/h6）のこと

HTML:
```
<h1>Hello, World!</h1>
```

## CSSも書いてみよう

### CSSってなーに？

* 人間にとってわかりやすくするためにHTMLを装飾する言語

実際に文字の色を変えてみよう!!

CSS:
```
h1 {
  color: red;
}
```

## 段落を書いてみよう

HTML:
```
<p>初めてのHTML</p>
```

背景に色をつけてみましょう！
HTML:
```
p {
  background: pink;
}
```

## リンクを追加してみよう

HTML:
```
<p>初めての<a href="https://ja.wikipedia.org/wiki/HyperText_Markup_Language">HTML</a></p>
```

## 箇条書きを書いてみよう

```
ul>li*3
```

HTML:
```
<ul>
  <li>箇条書き1</li>
  <li>箇条書き2</li>
  <li>箇条書き3</li>
</ul>
```

CSS:
```
li {
  text-decoration: underline;
}
```

## ボタンを書いてみよう

せっかくなのでリンクタグを装飾してこんな感じの王道なクリックボタンを作ってみましょう！！

[ボタンの完成イメージとコード](https://codepen.io/camillenexseed/pen/pozOeoE)

まずは新しいPenを作りましょう。

![ボタン](https://github.com/camillenexseed/special_class_okinawa/blob/master/images/btn.png)

CodePenのCSSの左上の歯車マークをクリックすると、無料で使えるCSSを追加できます。
スタイルを初期化する**normalize.css**と**font-awesome**というアイコンを使えるようにできるCSSを追加します。

検索窓にnormalize、font-awesomeと入力してCodePenに追加します。
読み込む順番が大切です！normalize、font-awesomeの順番に読み込みましょう。

![CSSを追加する](https://github.com/camillenexseed/special_class_okinawa/blob/master/images/css_add.png)

以下コードをHTML、CSSそれぞれに貼り付けます。

HTML:
```
<p><a href="#" class="btn default"><i class="fa fa-envelope"></i>CONTACT</a></p>
```

CSS:
```
p {
  text-align: center;
  padding: 30px;
}

.btn {
  display: inline-block;
  padding: 20px;
  text-decoration: none;
  font-weight: bold;
}

a i {
  padding-right: 5px;
}
```

ボタンの色を変えてみましょう！
a {　} の }前に以下を追加。できる人は色を変えてみましょう！

CSS:
```
background: orangered;
color: #fff;
```

マウスオーバーの時にアクションを追加してみましょう。
できたらボタンの上にカーソルを合わせてみましょう。
色が半透明になったら成功です！

CSS:
```
a:hover {
  opacity: .5;
}
```

a {　} の }前に以下を追加してアニメーションするようにしましょう。
ふんわり半透明になったら成功です！

CSS:
```
transition: .3s;
```

### ボタンのバリエーションを増やしてみよう

今度はマウスオーバーしたら背景の色が反転するタイプのボタンを作ってみましょう！

[ボタンの完成イメージとコード](https://codepen.io/camillenexseed/pen/WNegpYj)

まずは a {}の}の前に以下コードを追加します。

CSS:
```
border: 2px solid orangered;
```

CSS:
```
a:hover {
  color: orangered;
  background: #ffffff;
}
```
