# 2月メモ

## フラットメモリアル
GitHubへ連携させられた！
> [GitHubの初期設定（SSH接続からリポジトリへのpushまで）](https://qiita.com/drapon/items/441e18452b25060d61f1)

.DS_storeがうざい
> [.DS_Storeの仕組みと削除＆作成しないよう設定する方法](http://uxmilk.jp/48160)

SketchでプロトタイプするならCraftが死ぬほど便利。ワンクリックで全部InVisionにキャプチャアップロードしてくれる。
> [Craft](https://www.invisionapp.com/craft)

Fractal、すごく良さそう。先輩の手元で見せてもらった。自分で動かしてみたい。
> [Fractal](https://fractal.build/)

## CSS設計の教科書
### Web Compornentsのこと
webのUIをコンポーネント化するための仕様

### Web Compornentsの仕様
単独の仕様ではなく、次の4つの技術で成り立っている。
下記の仕様を組み合わせることによって、HTML/CSS/JSによって作られた独自のUIコンポーネントを作れる。

#### Templates
* 複雑なWebサイト、アプリケーションによく使われるテンプレートエンジンの考え方。
* Handlebars.js
* マークアップの断片をテンプレート（雛形）として、必要なときに呼び出せる。
* `<templates>` に内包される

#### Custom Elements
* 独自の要素（カスタム要素）を作れる
* `<like-button>` 、 `<x-auther>` `<x-card>` `<x-media>`
* 現状のHTMLとして定義されていない要素を作れる
* 既存の要素を拡張することも。 `<button is="like-button">`
* タグの名前には必ずハイフンを含める必要がある。（通常の要素とCustom Elementsとを区別するため）

#### Shadow DOM
* 隠蔽されたDOMを作ることができ、カプセル化の機能をもつ。
* カプセル化＝あるスコープの中の処理・値などを外部に漏らさないようにすること

#### HTML Imports
* あらゆるページ・プロジェクトで再利用しやすいよう、コンポーネント等をパッケージにして読み込める。
* jsファイルを `<script>` タグで読み込んだりするのと同じく、必要となるページで `<link>` タグを使って読み込む。

```HTML
<head>
  <link rel="import" href="component/success-message.html">
</head>
```
