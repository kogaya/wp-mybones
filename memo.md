# Bones修正にあたってのメモ

## ディレクトリ

`/library/css/style.css` コンパイル後のCSS

`/library/scss/breakpoints/_base.scss` 基本のSass

画面サイズに応じてレスポンシブにbreakpoints内のファイルが読み込まれる

base.scss → 各デバイスに合わせたSass

`/library/scss/partials/_variables.scss` 変数を格納している

`/library/scss/partials/_mixins.scss` mixinを格納している

`/library/scss/partials/_grid.scss` レイアウトを効率的に行う用のスタイル、使い方は下記

`m-1of4` → モバイル時に親要素の25%の幅で子要素を生成する （m:モバイル、t:タブレット、d:デスクトップ）

## ますが絵文字に化ける件

以下の５行を削除

```css
-webkit-font-feature-settings: &amp;quot;liga&amp;quot;, &amp;quot;dlig&amp;quot;;
-moz-font-feature-settings: &amp;quot;liga=1, dlig=1&amp;quot;;
-ms-font-feature-settings: &amp;quot;liga&amp;quot;, &amp;quot;dlig&amp;quot;;
-o-font-feature-settings: &amp;quot;liga&amp;quot;, &amp;quot;dlig&amp;quot;;
font-feature-settings: &amp;quot;liga&amp;quot;, &amp;quot;dlig&amp;quot;;
```

`/css/style.css`の523行目あたりと`/scss/partials:_typography.scss`の78行目あたりにある

## カスタム投稿タイプの追加

カスタム投稿タイプは`/library/custom-post-type.php` で管理している

サンプルのカスタム投稿タイプがあるのでコピペで追加することができる
