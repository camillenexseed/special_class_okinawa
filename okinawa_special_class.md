# オンラインツールで簡単！ プログラミング体験会・ハンズオン

このハンズオンでのゴールは**コーディングってどんなもの**を実際に体験することです。
CodePenを使って、実際に手を動かしてみましょう。

[コードペン](https://codepen.io/)

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

### さらにバリエーションを増やしてみる

ホバーすると背景が右側にスライドインアニメーションをするボタンを作ってみましょう。

![アニメーション](https://github.com/camillenexseed/special_class_okinawa/blob/master/images/vzfo7-fdnym.gif)

[ボタンの完成イメージとコード](https://codepen.io/camillenexseed/pen/BaBOWXp)

HTML:
```
<p><a class="stripe">Button</a></p>
```

CSS:
```
p {
  text-align: center;
  padding: 20px;
}

a {
  font-weight: bold;
  letter-spacing: .2em;
  display: inline-block;
  z-index: 1;
  padding: 20px 20px;
  width: 200px;
  overflow: hidden;
  text-align: center;
  background: rgb(245, 98, 0);
  color: #ffffff;
  position: relative;
}

a::before {
  z-index: -1;
  content: '';
  width: calc(200% + 40px);
  position: absolute;
  left: calc(-100% - 40px);
  height: 100%;
  display: block;
  top: 0;
  background: linear-gradient(135deg, rgba(242,144,46,1) 55%,rgb(245, 98, 0) 55%);
  transition: .3s;
}

a:hover::after {
  z-index: 1;
  content: '';
  width: 50px;
  height: 50px;
  position: absolute;
  display: block;
  bottom: 0;
  right: 0;
  background: linear-gradient(135deg, rgba(242,144,46,0) 50%,rgb(245, 98, 0) 50%);
}

a:hover::before {
  left: 0;
}
```

## ちょっとだけJavaScriptを書いてみよう

### JavaScriptってなーに？

JavaScriptとはブラウザ上でカンタンに動くプログラミング言語です。アニメーションとか簡単に実装できます。

[JavaScript完成イメージとコード](https://codepen.io/camillenexseed/pen/MWgqmdM)

JavaScriptの歯車マークから無料で使えるJavaScriptを追加します。
**jQuery**を追加しましょう。

追加したら、以下のようにコードを書いてみましょう。

JavaScript:
```
$('a').on('click', () => {
  alert('Hello, World!');
});
```

### おみくじを作ってみよう

[おみくじの完成イメージとコード](https://codepen.io/camillenexseed/pen/vYBzZgd)

JavaScriptの歯車マークから無料で使えるJavaScriptを追加します。
**jQuery**を追加しましょう。
HTMLとCSSをまずはコピペしましょう。

HTML:
```
<p><a class="stripe">おみくじ</a></p>
<p class="result"></p>
```

CSS:
```
p {
  text-align: center;
  padding: 20px;
}

.result {
  font-size: 30px;
}

a {
  padding: 20px;
  color: #fff;
  background: #000;
}

#_0 {
  background: red;
  color: #fff;
}

#_1 {
  background: blue;
  color: #fff;
}

#_2 {
  background: green;
  color: #fff;
}

#_3 {
  background: orange;
  color: #fff;
}

#_4 {
  background: gray;
  color: #fff;
}
```

おみくじのJavaScriptを書いてみます。
JavaScript:
```
$('a').on('click', () => {
  const resultArray = ['大吉','中吉','小吉','末吉','凶'];
  let randomNum = Math.floor(Math.random()*resultArray.length);
  $('.result').text(resultArray[randomNum]).attr('id', '_'+ randomNum);
});
```
