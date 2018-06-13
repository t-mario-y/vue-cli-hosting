# vue-cli-hosting
vue-cliの成果物をホスティングするexpressサーバ

### expressサーバ作成
```
express vue-cli-hosting --view=ejs
cd vue-cli-hosting
npm install
```
### index.html/JS/CSSをExpressサーバに合わせて配置
 * views/index.ejs を置き換える
 * dist/static/js/ を public/javascripts/ に コピー
 * dist/static/css/ を public/stylesheets/ に コピー

### index.ejs のJS/CSSファイルの読み込みパスを変える
 * /static/js/hoge.js → /javascripts/hoge.js 
 * /static/css/fuga.css → /stylesheets/fuga.css
 
### npm runで起動
localhost:3000 でindex.html にアクセスできる。

### 課題
バンドル後のファイルを手で書き換えているほうがおかしいので、サーバ構成に合わせてWebpackのビルド設定を変えるか、Expressサーバ構成を変える必要がある。
