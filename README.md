# React.js練習用

![deploy](https://github.com/Mizukichi0210/practice-reactjs/workflows/deploy/badge.svg?branch=master&event=push)
[![codecov](https://codecov.io/gh/Mizukichi0210/practice-reactjs/branch/master/graph/badge.svg)](https://codecov.io/gh/Mizukichi0210/practice-reactjs)

masterブランチへpush後にGitHub pagesにデプロイされる

## 起動方法

```bash
# ビルド方法
# /practice-reactjs 直下で行う
$ docker/build_image.sh

# コンテナ起動方法
$ docker run --rm -p 8000:8000 -v $(pwd):/practice-reactjs -it practice-reactjs /bin/bash

# サーバ起動方法
# http://localhost:8000
$ npm start
```

### 注意事項
- コンテナ内で `npm install` でパッケージをインストールしたら**再度dockerイメージの構築を行うこと**
- `yarn add xx` でパッケージの追加を行った場合、`npm install`をして`package-lock.json`を更新すること

## デプロイ方法

masterブランチへpushをすればテスト実行後にデプロイされる

## 詳細

使用するCSS Framework: [Semantic UI React](https://react.semantic-ui.com/)
