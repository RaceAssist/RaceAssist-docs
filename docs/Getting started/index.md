# How to Install 

## RaceAssist-core

このプラグインはサーバー用プラグインです。<br>
サーバーのプラグインフォルダーに置いてください。 <br>

[RaceAssist-core Download Link](https://github.com/RaceAssist/RaceAssist-core/releases)

## RaceAssist-api

### RaceAssist-api-cf-workers

このプラグインはcloudflareのworkersを使用する必要があります。


```
git clone https://github.com/RaceAssist/RaceAssist-API-cf-workers.git
```
```
cd RaceAssist-API-cd-workers
```

R2バケット[raceassist-bet , raceassist-result , raceassist-horse]を作成する。<br>
そして、wrangler.toml の kv_namespaces の id と preview_id を書き換えてください。<br>
そして、秘密の環境変数 USERNAMEとPASSWORD を設定します。<br>

```
npm run deploy
```
### RaceAssist-api-s3

現在作成中です。

## RaceAssist-web

このWebアプリケーションはRaceAssist-apiと一緒に使う必要があります。<br>

[RaceAssist-web](https://github.com/RaceAssist/RaceAssist-web)

vercelにデプロイします。

以下の環境変数を設定します。

`RACEASSIST_API_SERVER_URL` : マインクラフトサーバーのIP<br>
`RACEASSIST_API_WEBHOOK_USER` : APIのUSERNAME<br>
`RACEASSIST_API_WEBHOOK_PASSWORD` : APIのPASSWORD<br>
`RACEASSIST_API_WEBHOOK_URL` : APIのURL<br>



