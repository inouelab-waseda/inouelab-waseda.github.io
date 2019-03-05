# 井上研Webサイト用のファイル
## 使い方
1. 何とかしてhexoをインストール(node.jsとかnpmとかが必要だったけど調べてくれ)
2. .mdファイルなどを編集して `hexo generate`
3. `public/index.html`のheadタグ内に以下を記述。

```js
<script>      

    if(window.location.href.match(/^https?:\/\/(?:www\.)?eb\.waseda\.ac\.jp\/m_inoue.*/))
    {
        window.location = "http://www.inoue.eb.waseda.ac.jp/"
    }

</script>
```
4. `public`を`public_html`という名前に変更して電生のサーバに置く。

## 電生のサーバへの置き方
`FileZilla`というアプリを使用
- 接続先の登録
```
ホスト: hosting2.mse.waseda.ac.jp 
プロトコル: FTP - ファイル転送プロトコル
ポート: 21
暗号化: 平文
ログオンの種類: 通常
ユーザ: inoueebw
パス: 管理者パス
転送モード: パッシブ
```
研究室内から接続すると繋がらない？説がある。
