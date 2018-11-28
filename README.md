NFCカードであかりちゃんに勤怠管理してもらったり始業終業休憩＆＆来客訪問教えてもらえるシステム
====

**自分のアーカイブ用なのでなにか起こっても責任取れません。**  
**IVR_NFC** - Pasori380使ってセキュリティカードをタッチすることでCSVファイルに時刻と勤務時間を分単位で記録します。  
**IVR_timeReport** - きずなあかりちゃんが時報をやってくれます。 
**slackakari** - きずなあかりちゃんが来客や配達があると喋って教えてくれます。

## Description
### IVR_NFC
PasoriにNFCタグを当てるとアリスちゃんが勤怠管理してくれます。NFCのidm使って個人識別してます。NFCサービスも識別して弾くなどしてないので大規模な会社ではこれやらないほうがいいでしょうう。　　CSVに個人情報を登録するとそこから自動で情報を読み取って追加してくれます。CSVがなかったら自動で記録用ファイルを作ってくれたりもする。記録用CSVのフォーマットがおかしかったりするとあかりちゃんがダメです。って言うはず。　　退勤処理をすると分単位でその日に働いた時間が記録されます。　　　　　　　　　　　　　　　

### IVR_timeReport
時間を指定しておくと、決められたディレクトリにいれられたファイルをランダムに選んで喋ってくれるよ。

## Requirement
nfcpy(python2.7.10)
libusb(1.0.21)
oauth2client
zadig-2.3 <- Pasoriのドライバ置き換えに活用
pyaudio
slacker

## 今後の展望
時間があったら、そのうち天気予報とかいろいろおしゃべりしてくれるようにアップデートしたい。
