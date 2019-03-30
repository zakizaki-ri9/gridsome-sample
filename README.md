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
