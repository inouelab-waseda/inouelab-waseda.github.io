# 井上研 Web サイト
## インストール
まず、依存ライブラリをインストールする。

Ubuntu であれば、以下のコマンドを打つだけでよい。

```
$ sudo apt install curl git
$ curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
$ sudo apt install nodejs
```

Mac、Windows に関しては以下の公式サイトからインストーラーをダウンロードしてインストールする。

- Git: https://git-scm.com/
- Node.js: https://nodejs.org/


以下でインストールできていることを確認。

```
$ node -v
$ npm -v
```

次に、このリポジトリをクローンする。ここは GitHub Desktop 等でやってもよい。なお、以下の方法でクローンする場合は ssh 鍵の登録が必要なので、[公式ヘルプ](https://help.github.com/en/articles/connecting-to-github-with-ssh)などを見て設定しておく。

```
$ git clone git@github.com:inouelab-waseda/inouelab-waseda.github.io.git
```

Hexo をインストール。

```
$ npm install -g hexo-cli
```

リポジトリの中で、依存 JS ライブラリをインストール。

```
$ cd inouelab-waseda.github.io
$ npm install
```

これで環境設定は済んでいるはず。

# 記事の更新
**必ず `develop` ブランチで変更を行うこと。絶対に `master` ブランチを触ってはいけない。(普通に使っている限り、`master` ブランチを操作する必要性はないはず。ただし、メンテナンスなどの目的がある場合は別。)**

`souces` 以下にある .md ファイルを書き換えて、変更を commit&push する。この手順も、GitHub Desktop 等でやってよい。

```
$ git add .
$ git commit
$ git push origin develop
```




