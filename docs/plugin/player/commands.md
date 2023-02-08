# コマンド一覧

*がついているコマンドは一般プレイヤーが使用できるコマンドです。
@がついているコマンドは未実装のコマンドです。

## Audience コマンド
レースの観客についてのコマンドです。<br>
観客に入っているとレースの順位などが表示されます。

指定したレースの観客に参加します。<br>
コマンド : `/ra audience join <raceId>`* <br>
権限 : `raceassist.commands.audience.join` <br>

指定したレースの観客から退出します。<br>
コマンド : `/ra audience leave <raceId>`* <br>
権限 : `raceassist.commands.audience.leave` <br>

指定したレースの観客一覧を表示します。<br>
コマンド : `/ra audience list <operateRaceId>` <br>
権限 : `raceassist.commands.audience.list` <br>

## Bet コマンド
賭けのためのコマンドです。

賭けるためのGUIを開きます。<br>
コマンド : `/ra bet open <raceId>`* <br>
権限 : `raceassist.commands.bet.open` <br>

指定したレースに賭けをできるようにするかどうか変更します。<br>
コマンド : `/ra bet can <operateRaceId> <type>` <br>
権限 : `raceassist.commands.bet.can` <br>

賭けに対する返却率を変更します。<br>
コマンド : `/ra bet rate <operateRaceId> <rate>` <br>
権限 : `raceassist.commands.bet.rate` <br>

指定したレースに賭けられているデータをすべて表示します。<br>
コマンド : `/ra bet list <operateRaceId>` <br>
権限 : `raceassist.commands.bet.list` <br>

指定したレースに賭けられているデータをすべて削除します。(返却は行わない)<br>
コマンド : `/ra bet delete <operateRaceId>` <br>
権限 : `raceassist.commands.bet.delete` <br>

指定した番号の賭けを返却します。(返却したデータは削除)<br>
コマンド : `/ra bet revert row <operateRaceId> <row>` <br>
権限 : `raceassist.commands.bet.revert.row` <br>

指定したレースの賭けをすべて返却します。(返却したデータは削除)<br>
コマンド : `/ra bet revert all <operateRaceId>` <br>
権限 : `raceassist.commands.bet.revert.all` <br>

指定した選手に対する賭けをすべて返却します。(返却したデータは削除)<br>
コマンド : `/ra bet revert player <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.bet.revert.jockey` <br>

賭けられたデータをSpreadSheetでみられるようにします。<br>
コマンド : `/ra bet sheet <operateRaceId> <sheet>` <br>
権限 : `raceassist.commands.bet.sheet` <br>

優勝した選手に賭けている人に対して払い戻しを行います。(払い戻したデータは削除)<br>
コマンド : `/ra bet pay <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.bet.return.jockey` <br>

賭けの1単位当たりの金額を設定します。<br>
コマンド : `/ra bet unit <operateRaceId> <unit>` <br>
権限 : `raceassist.commands.bet.unit` <br>

## Web コマンド
Webで扱うデータのためのコマンドです。(Webが有効になっている場合のみ)

Webでログインするためのパスワードを発行します。<br>
コマンド : `/ra web register`* <br>
権限 : `raceassist.commands.web` <br>

Webでログインするためのパスワードを削除します。<br>
コマンド : `/ra web reset`* <br>
権限 : `raceassist.commands.web` <br>

## Setting コマンド
レースの設定のためのコマンドです。

`<raceId1>`で指定したレースをベースに新しいレースを作成します。
所有者、スタッフ、選手のみ初期化されます。<br>
コマンド : `/ra setting copy <raceId1> <raceId2>` <br>
権限 : `raceassist.commands.setting.copy` <br>

新しいレースを作成します。<br>
コマンド : `/ra setting create <raceId> <placeId>` <br>
権限 : `raceassist.commands.setting.create` <br>

レースを削除します。<br>
コマンド : `/ra setting delete <operateRaceId>` <br>
権限 : `raceassist.commands.setting.delete` <br>

レースのLap数を指定します。<br>
コマンド : `/ra setting lap <operateRaceId> <lap>` <br>
権限 : `raceassist.commands.setting.lap` <br>

レースの競技場を指定します。<br>
コマンド : `/ra setting placeId <operateRaceId> <placeId>` <br>
権限 : `raceassist.commands.setting.placeId` <br>

レースでの順位表示の際の置換する名前を設定します。<br>
コマンド : `/ra setting replacement set <operateRaceId> <playerName> <replacement>` <br>
権限 : `raceassist.commands.setting.replacement` <br>

指定したプレイヤーのレースでの順位表示の際の置換する名前を削除します。<br>
コマンド : `/ra setting replacement remove <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.setting.replacement` <br>

レースでの順位表示の際の置換する名前すべて表示します。<br>
コマンド : `/ra setting replacement list <operateRaceId>` <br>
権限 : `raceassist.commands.setting.replacement` <br>

レースでの順位表示の際の置換する名前すべて削除します。<br>
コマンド : `/ra setting replacement delete <operateRaceId>` <br>
権限 : `raceassist.commands.setting.replacement` <br>

レースにスタッフを追加します。<br>
コマンド : `/ra setting staff add <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.setting.staff` <br>

スタッフの一覧を表示します。<br>
コマンド : `/ra setting staff list <operateRaceId>` <br>
権限 : `raceassist.commands.setting.staff` <br>

レースのスタッフから指定したプレイヤーを削除します。<br>
コマンド : `/ra setting staff remove <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.setting.staff` <br>

レースのコンフィグ一覧を表示します。<br>
コマンド : `/ra setting view <operateRaceId>` <br>
権限 : `raceassist.commands.setting.view` <br>

## Place コマンド
競技場についてのコマンドです。

コマンド : `/ra place central <operatePlaceId>` <br>
権限 : `raceassist.commands.place.central` <br>

コマンド : `/ra place create <placeId>` <br>
権限 : `raceassist.commands.place.reverse` <br>

コマンド : `/ra place degree <operatePlaceId>` <br>
権限 : `raceassist.commands.place.degree` <br>

コマンド : `/ra place finish` <br>
権限 : `raceassist.commands.place.finish` <br>

コマンド : `/ra place reverse <operatePlaceId>` <br>
権限 : `raceassist.commands.place.reverse` <br>

コマンド : `/ra place set <operatePlaceId> <type>` <br>
権限 : `raceassist.commands.place.set` <br>

コマンド : `/ra place staff add <operatePlaceId> <playerName>` <br>
権限 : `raceassist.commands.place.staff` <br>

コマンド : `/ra place staff list <operatePlaceId>` <br>
権限 : `raceassist.commands.place.staff` <br>

コマンド : `/ra place staff remove <operatePlaceId> <playerName>` <br>
権限 : `raceassist.commands.place.staff` <br>

## Race コマンド
レースの開始のためのコマンドです。

コマンド : `/ra race start <operateRaceId>` <br>
権限 : `raceassist.commands.race.start` <br>

コマンド : `/ra race stop <operateRaceId>` <br>
権限 : `raceassist.commands.race.stop` <br>

コマンド : `/ra race debug <operateRaceId>` <br>
権限 : `raceassist.commands.race.debug` <br>

コマンド : `/ra race horse remove <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.race.horse` <br>

コマンド : `/ra race horse add <operateRaceId>` <br>
権限 : `raceassist.commands.race.horse` <br>

コマンド : `/ra race horse delete <operateRaceId>` <br>
権限 : `raceassist.commands.race.horse` <br>

コマンド : `/ra race horse list <operateRaceId>` <br>
権限 : `raceassist.commands.race.horse` <br>

## Player コマンド
出場する選手について取り扱うコマンドです。

コマンド : `/ra player add <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.player.add` <br>

コマンド : `/ra player delete <operateRaceId>` <br>
権限 : `raceassist.commands.player.delete` <br>

コマンド : `/ra player list <operateRaceId>` <br>
権限 : `raceassist.commands.player.list` <br>

コマンド : `/ra player remove <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.player.remove` <br>

コマンド : `/ra player replacement remove <operateRaceId> <playerName>` <br>
権限 : `raceassist.commands.player.replacement` <br>

コマンド : `/ra player replacement set <operateRaceId> <playerName> <replacement>` <br>
権限 : `raceassist.commands.player.replacement` <br>

##　その他のコマンド

### Helpコマンド 
コマンド : ` ra help `* <br>
権限 : ` raceassist.commands.help ` <br>

### Reloadコマンド
コマンド : ` ra reload ` <br>
権限 : ` raceassist.commands.reload ` <br>