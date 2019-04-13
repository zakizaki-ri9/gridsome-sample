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

[公式リファレンスのBootstrapVueの部分](https://gridsome.org/docs/assets-css/#bootstrapvue)参照。

```bash
yarn add bootstrap-vue bootstrap
```

```js
import BootstrapVue from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default function (Vue, { router, head, isClient }) {
  Vue.use(BootstrapVue) // add
}
```

### FontAwesome(SVG)

```bash
yarn add @fortawesome/vue-fontawesome
yarn add @fortawesome/fontawesome-svg-core
yarn add @fortawesome/free-solid-svg-icons
yarn add @fortawesome/free-brands-svg-icons
yarn add @fortawesome/free-regular-svg-icons
```

```js
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { library } from '@fortawesome/fontawesome-svg-core'
import { fas } from '@fortawesome/free-solid-svg-icons'
import { fab } from '@fortawesome/free-brands-svg-icons'
import { far } from '@fortawesome/free-regular-svg-icons'

library.add(fas, far, fab)

export default function (Vue, { router, head, isClient }) {
  Vue.component('font-awesome-icon', FontAwesomeIcon) // add
}
```

```pug
//- i.fa.fa-user
font-awesome-icon(:icon="['fa', 'user']") 
```
