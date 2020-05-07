# try_fastify

## 環境設定

### Node.jsバージョン指定

```bash
$ nodenv local 14.1.0
$ node -v
v14.1.0
$ npm -v
6.14.4
```

### npmモジュール指定( webpack+TypeScriptの最小構成 )

[最新版TypeScript+webpack 4の環境構築まとめ(React, Vue.js, Three.jsのサンプル付き)](https://ics.media/entry/16329/)

```bash
$ npm init
$ npm install --save-dev typescript ts-loader
$ vi package.json
$ cat package.json
...
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "tsc -p tsconfig.json"
  },
...
  "devDependencies": {
    "ts-loader": "^7.0.3",
    "typescript": "^3.8.3",
    "webpack": "^4.43.0",
    "webpack-cli": "^3.3.11"
  },
  "private": true
}
```

### tsconfig.json

```json
{
  "compilerOptions": {
    "sourceMap": true,
    "target": "es5",
    "module": "commonjs",
    "outDir": "dist"
  }
}
```

### fastify導入

[Node.jsフレームワークを比較して見えたそれぞれの特徴](https://www.wantedly.com/companies/company_3239475/post_articles/179467)
[https://www.fastify.io/](https://www.fastify.io/)

```bash
$ npm install --save fastify
$ npm install --save-dev @types/node
```
