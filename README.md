# Gridsomeを用いたサンプル

## GridsomeCLIのインストール

```bash
# npm
npm install --global @gridsome/cli

# yarn
yarn global add @gridsome/cli
```
## プロジェクトの作成

```bash
gridsome create gridsome-site {starter-kit}
```

{starter-kit}には雛形となるスターターキットの名前を指定する


## 起動

```bash
gridsome develop
```

## pluginのインストール

### pug

[gridsome-plugin-pug](https://github.com/gluons/gridsome-plugin-pug)を使用する。

```bash
yarn add -D pug gridsome-plugin-pug
```

```js
// gridsome.config.js
module.exports = {
 	plugins: [
		'gridsome-plugin-pug' // add
	]
}
```

### BootstrapVue

[公式リファレンスのbootstrapvueの部分](https://gridsome.org/docs/assets-css/#bootstrapvue)参照。

```bash
yarn add bootstrap-vue bootstrap
```

```js
import BootstrapVue from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default function (Vue, { router, head, isClient }) {
  Vue.use(BootstrapVue)
}
```
