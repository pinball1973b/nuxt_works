# nuxt_work

> Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).

##トラブルシューティング
まれに以下のエラーが出て、立ち上がらない場合あり。

``` Error: getaddrinfo ENOTFOUND localhost
    at errnoException (dns.js:28:10)
    at GetAddrInfoReqWrap.onlookup [as oncomplete] (dns.js:73:26)
```

その場合は以下の通りの方法を試して下さい
(Macの場合)
- /etc/hostsを編集し、以下を追加

```127.0.0.1       localhost
```
