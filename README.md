# spring-vue

> SpringMVC と Vue.js で作成したアプリをHerokuで動かすサンプル

## Heroku デプロイ用コマンド

``` bash
# アプリ作成
heroku create

# buildpacks指定（恐らく順番が大切）
heroku buildpacks:add heroku/nodejs
heroku buildpacks:add heroku/java

# devDependencies もダウンロードするように設定（https://devcenter.heroku.com/articles/nodejs-support#devdependencies）
heroku config:set NPM_CONFIG_PRODUCTION=false

# タイムゾーン指定（必須ではない）
heroku config:add TZ=Asia/Tokyo

# デプロイ
git push heroku master
```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
