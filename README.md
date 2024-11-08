# Next.js Self Host

以下をfolkして、httpsではなくhttpで動作するようにしたもの。オリジナルはSSL証明書の取得まで行うため、ドメインの取得が必須である。これだと簡単に試すことができないので、SSLを用いないように修正した。

- https://github.com/leerob/next-self-host

メモリ512mbのVPSでも動作するようにするため、スワップを追加したりしているので、VPSもしくはVM上で実行した方がよい。

Ubuntu Server 24.04 512mbで動作確認。

## 手順

スクリプトをダウンロードする。

``` bash
curl -o ~/deploy.sh https://raw.githubusercontent.com/yohei-yoshihara/next-self-host/main/deploy.sh
chmod a+x deploy.sh
```

`deploy.sh`を開き、`DOMAIN_NAME`を修正する。

```bash
vim deploy.sh
```

スクリプトを実行する。

```bash
./deploy.sh
```

以下へアクセスする。

- `http://<DOMAIN_NAME>/`

