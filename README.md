<html>
<head>
    <title>valorantのvan9001 van9003 エラー対策(Ryzen5000/Ryzen3000シリーズ用)</title>
</head>
<body>
<h2>valorant の van9001 van9003 エラー対策</h2>

　症状：windows11で、valorantをプレイすると上記エラーでゲームが落ちる <br>
　対象：Ryzen5000シリーズ、Ryzen3000シリーズ搭載機<br>
　　　　※Ryzen環境しかないのでIntel環境は別の記事を参照してください。<br>
<hr>

1.Windows11のメニューから再起動<br>
　電源ボタンをクリックし、メニューが表示されたら<br>
　キーボードのShiftキーを押し続けながら再起動をクリックする。<br>
　お待ち下さいロード画面が出たら、Shiftキーを離す。<br>
　<img src="./win11_10.png" width="680" height="510"><br><br>

2.オプション画面からファームウェア設定へ<br>
　トラブルシューティングを選択し、詳細オプション→UEFIファームウェア設定へ進む。<br>
　<img src="./win11_11.png" width="340" height="255"> <img src="./win11_12.png" width="340" height="255"><br>
　<img src="./win11_13.png" width="680" height="510"><br><br>

3.ファームウエアメニュー<br>
　メーカーにより異なるので、最も近いメニューをタップしてください。<br>
　※機種によりカラーリングが異なることがあります。<br>
　<a href="#asus"><img src="./asus01.png" width="340" height="255"></a> <a href="#asrock"><img src="./asrock01.png" width="340" height="255"></a><br>
　<a href="#giga"><img src="./giga01.png" width="340" height="255"></a> <a href="#msi"><img src="./msi01.png" width="340" height="255"></a><br>

<hr>
<section aria-labelledby="setting">
　<details name="uefi"><summary id="asus">UEFI BIOS Utility (ASUS)</summary>
	<p>4.ファームウェアの設定<br>
	　メニューの言語が日本語の場合もありますが、大体英語のカタカナ表記になっています。<br>
	　※キーボードのカーソルキー(矢印)とEnterキー(決定)、ESCキー(戻る)でも操作できます。<br>
	　※機種により表記や色が異なる事があります。<br><br>

	　Advanced(詳細モード) を選択し、最上段のAdvanced(詳細) からメニュー 一番上の<br>
	　AMD fTPM Config～メニューに入ります。TPM Device Selection を選ぶと<br>
	　選択肢が表示されるので、Firmware TPM(有効) にします。<br>
	　<img src="./asus02.png" width="340" height="255"> <img src="./asus03.png" width="340" height="255"><br>
	　<img src="./asus04.png" width="680" height="510"><br><br>

	5.仮想化機能の設定<br>
	　メニュー上段の ←を選択し 前画面へ、上から二段目のCPU Config～メニューへ入ります。<br>
	　中段にある SVM Mode を選択すると、選択肢が出るので Enabled(有効)にします。<br>
	　<img src="./asus05.png" width="340" height="255"> <img src="./asus05a.png" width="340" height="255"><br>
	　<img src="./asus05b.png" width="680" height="510"><br><br>

	6.起動設定<br>
	　最上段の Boot を選択し、上から二番目の CSM～(互換サポートモジュール) メニューに入ります。<br>
	　Launch CSMを選択すると、選択肢が表示されるので、Disabled(無効)にします。<br>
	　<img src="./asus06.png" width="340" height="255"> <img src="./asus07.png" width="340" height="255"><br><br>

	7.セキュアブートの有効化<br>
	　メニュー上段の ←を選択し 前画面へ、上から三番目の SecureBoot メニューに入ります。<br>
	　OS Type を選択すると、選択肢が表示されるので、Windows UEFI Mode に変更します。<br>
	　<img src="./asus08a.png" width="340" height="255"> <img src="./asus08b.png" width="340" height="255"><br>
	　<img src="./asus09.png" width="680" height="510"><br><br>

	8.設定の保存<br>
	　最上段の Exit を選択、上から二番目の Save Change &amp; Reset(保存して再起動)を選択すると<br>
	　設定を保存し再起動します。設定を保存せずに終了するには Discard Change &amp; Exit にします。<br>
	　<img src="./asus10.png" width="680" height="510"><br><br>

	9.動作確認<br>
	　Windowsが起動したら、Valorantでエラーが出ないか確認します。<br>
	　エラーが引き続き出る場合は、ファームウエアの更新が必要になる場合があります。<br>
	</p></details>
<hr>
　<details name="uefi"><summary id="asrock">ASRock</summary>
	<p>4.ファームウェアの設定<br>
	　メニューの言語が日本語の場合もありますが、大体英語のカタカナ表記になっています。<br>
	　※キーボードのカーソルキー(矢印)とEnterキー(決定)、ESCキー(戻る)でも操作できます。<br>
	　※機種により表記や色が異なる事があります。<br><br>

	　Advanced(詳細モード) を選択し、Advanced からCPU Config～メニューに入ります。<br>
	　メニュー 一番下の AMD fTPM を選択すると、選択肢が表示されるので<br>
	　AMD CPU fTPM に変更します。その項目が無い場合は Enabled(有効)にします。<br>

	　<img src="./asrock02.png" width="340" height="255"> <img src="./asrock03.png" width="340" height="255"><br>
	　<img src="./asrock04.png" width="680" height="510"><br><br>

	5.起動設定<br>
	　最上段の Boot を選択し、一番下のCSM～(互換サポートモジュール) メニューに入ります。<br>
	　メニュー 一番上のCSMを選択すると、選択肢が表示されるので、Disabled(無効)にします。<br>
	　<img src="./asrock05.png" width="340" height="255"> <img src="./asrock06.png" width="340" height="255"><br><br>

	6.セキュアブートモードの設定<br>
	　最上段の Security を選択し、SecureBootメニューに入ります。<br>
	　Secure Boot の項目をいったん<span style="font-weight:bold;">Disabled(無効)</span>にします。<br>
	　Secure Boot Mode を選択すると、選択肢が表示されるので、Standard(標準) にします。<br>
	　<img src="./asrock07.png" width="340" height="255"> <img src="./asrock08.png" width="340" height="255"><br>
	　<img src="./asrock09.png" width="680" height="510"><br><br>

	7.セキュアブートの有効化<br>
	　Secure Boot の項目を Enabled(有効)にします。<br>
	　<img src="./asrock10.png" width="680" height="510"><br><br>

	8.設定の保存<br>
	　最上段の Exit を選択し、一番上の Save Change and Exit を選択すると<br>
	　設定を保存し再起動します。保存せずに終了するには Discard Change and Exit にします。<br>
	　<img src="./asrock11.png" width="680" height="510"><br><br>

	9.動作確認<br>
	　Windowsが起動したら、Valorantでエラーが出ないか確認します。<br>
	　エラーが引き続き出る場合は、<a href="https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q11278912276" target="_blank">こちらの手順</a>を試してみてください。<br>
	</p></details>
<hr>
　<details name="uefi"><summary id="giga">AORUS (Gigabyte)</summary>
	<p>4.ファームウェアの設定<br>
	　項目の場所や表記が機種によってバラバラなうえ、手順が複雑なので難易度が高く<br>
	　全てのステップを正確に書けてるかは怪しいので、設定変更はおすすめしません。<br><br>

	　※ファームウェアの更新をすれば難易度は下がると思われますが、BTOなどでは<br>
	　　Windowsの認証キーがファームウェアに含まれている物が有り、BTOメーカー以外の<br>
	　　ファームウェアを書き込むとキーが消えてOSの認証が外れる場合があるのでご注意ください。<br>

	　※キーボードのカーソルキー(矢印)とEnterキー(決定)、ESCキー(戻る)でも操作できます。<br>
	　※機種により表記や色が異なる事があります。<br><br>

	　Advanced Mode(詳細モード) を選択し、Tweaker からAdvanced CPU Settings へ進み<br>
	　SVM Mode を選択すると、選択肢が表示されるので Enabled(有効)にします。<br>
	　<img src="./giga02.png" width="340" height="255"> <img src="./giga03a.png" width="340" height="255"><br>
	　<img src="./giga05a.png" width="680" height="510"><br><br>

	　最上段の Settings (Peripherals表記の場合も有り) を選択し、<br>
	　AMD CPU fTPM を Enabled(有効) にします。<br>
	　※Settings - Miscellaneousサブメニューの中に有る機種もあります。<br>
	　<img src="./giga05b.png" width="680" height="510"><br><br>

	5.起動設定<br>
	　最上段の Boot を選択し、中段のCSM Support(互換サポートモジュール) を選択すると<br>
	　選択肢が表示されるので、Disabled(無効)にします。<br>
	　<img src="./giga06.png" width="680" height="510"><br><br>

	　最上段の Save &amp; Exit を選択し、Save &amp; Exit Setup を選択後 YES を押すと再起動<br>
	　するので、キーボードの DELキー を押し続けて再びファームウェア画面へ戻ります。<br>
	※Windowsが起動した場合は、手順1～3でファームウェアメニューへと進んでください。<br>
	　<img src="./giga06b.png" width="680" height="510"><br><br>

	6.セキュアブートモードの設定<br>
	　最上段の Boot を選択し、SecureBootメニューに入ります。<br>
	　Secure Boot Mode の項目をいったん <span style="font-weight:bold;">Custom</span>にします。<br>
	　次に RestoreFactory Keys を選択すると、選択肢が出るので YESを選択します。<br>
	　もう一度選択肢が出るので、YESを選択して再起動します。画面が暗転したら<br>
	　キーボードのDELキーを押し続けて再びファームウェア画面へ戻ります。<br>
	※Windowsが起動した場合は、手順1～3でファームウェアメニューへと進んでください。<br>
	　<img src="./giga07.png" width="340" height="255"> <img src="./giga08.png" width="340" height="255"><br><br>

	7.セキュアブートの有効化<br>
	　最上段の Boot を選択し、再びSecureBootメニューに入ります。<br>
	　SecureBootの項目がActiveになっていたら、SecureBootModeをStandardへ戻します。<br>
	　<img src="./giga09.png" width="680" height="510"><br><br>

	8.設定の保存<br>
	　最上段の Save &amp; Exit を選択し、Save &amp; Exit Setup を選択後 YES を押して設定を保存します。<br>
	　<img src="./giga06b.png" width="680" height="510"><br><br>

	9.動作確認<br>
	　Windowsが起動したら、Valorantでエラーが出ないか確認します。<br>
	　手順が複雑すぎて、すべてのステップを正確に書けているかは正直あやしいです。<br>
	　解決しない場合は以下の手順を試してみてください。<br>
	　<a href="https://www.youtube.com/watch?v=lwaIWu_41_0" target="_blank">How to Enable Secure Boot on AORUS Motherboard (Youtube)</a><br>
	　<a href="https://x.com/AORUS_JP/status/1408268492147617793" target="_blank">GIGABYTE X570 UD マザーボード例 (公式twitter)</a><br>
	　<a href="https://support.pcdiy.newx.co.jp/hc/ja/articles/6572156997657--GIGABYTE%E3%83%9E%E3%82%B6%E3%83%BC%E3%83%9C%E3%83%BC%E3%83%89%E5%85%A8%E8%88%AC-Secure-Boot-%E3%81%AE%E8%A8%AD%E5%AE%9A%E6%96%B9%E6%B3%95%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6" target="_blank">【GIGABYTEマザーボード全般】Secure Boot の設定方法について(代理店)</a><br>
	　<a href="https://bbs.kakaku.com/bbs/K0001326216/SortID=24941106/" target="_blank">セキュアブートはどうやって有効にすればいいのでしょうか？ (B550 AORUS ELITE V2)</a><br>
	　<a href="https://www.reddit.com/r/gigabyte/comments/udde6g/x570_aorus_elite_wifi_mobo_secure_boot/" target="_blank">X570 Aorus Elite Wifi Mobo, secure boot problem/tpm2.0 (アメリカ語)</a><br>
	　<a href="https://www.reddit.com/r/gigabyte/comments/ocimkx/x570_elite_mobo_secure_boot_problem/" target="_blank">X570 Elite Mobo, secure boot problem (アメリカ語)</a><br><br>
	</p></details>
<hr>
　<details name="uefi"><summary id="msi">MSI</summary>
	<p>4.ファームウェアの設定<br>
	　メニューの言語が日本語の場合もありますが、大体英語のカタカナ表記になっています。<br>
	　※キーボードのカーソルキー(矢印)とEnterキー(決定)、ESCキー(戻る)でも操作できます。<br>
	　※機種により表記や色が異なる事があります。<br><br>

	　画面上部の Advanced(詳細モード) を選択します。画面左のSETTINGS から<br>
	　Security メニューに入り、Trusted Computing の項目に進みます。<br><br>
	　Security Device Support を選択すると、選択肢が出るので Enable(有効)にします。<br>
	　その下の AMD fTPM Switch が <span style="font-weight:bold;">AMD CPU fTPM</span> になっている事を確認します。<br>  
	　<img src="./msi02.png" width="340" height="255"> <img src="./msi03.png" width="340" height="255"><br>
	　<img src="./msi04.png" width="680" height="510"><br><br>

	5.起動設定<br>
	　画面左のSETTINGS から、メニュー 上側の Advanced(拡張項目) メニューに入ります。<br>
	　中央下の Windows OS Config～ へ進み、BIOS UEFI/CSM Mode を UEFI にします。<br>
	　<img src="./msi05.png" width="340" height="255"> <img src="./msi06.png" width="340" height="255"><br>
	　<img src="./msi07.png" width="680" height="510"><br><br>

	6.セキュアブートの有効化<br>
	　一番下の SecureBoot メニューに入ります。<br>
	　Secure Boot Mode を選択、選択肢が表示されるので Standard にします。<br>
	　Secure Boot の項目を選択、選択肢が表示されるので Enabled(有効)にします。<br>
	　エラーが表示された場合は、Enroll All Factory Default Keys をロードしてみてください。<br>
	　<img src="./msi08.png" width="340" height="255"> <img src="./msi09b.png" width="340" height="255"><br>
	　<img src="./msi09a.png" width="680" height="510"><br><br>

	7.仮想化機能の設定<br>
	　画面左の OC から、メニュー 一番下の CPU Features または Advanced CPU Config～を<br>
	　開き、SVM Mode を選択します。選択肢が出るので Enabled(有効)にします。<br>
	　<img src="./msi10.png" width="340" height="255"><br>
	　<img src="./msi11.png" width="680" height="510"><br><br>

	8.設定の保存<br>
	　画面左のSETTINGS から、メニュー 一番下の Save &amp; Exit(保存と終了) メニューに入ります。<br>
	　Save Changes and Reboot(保存して再起動)を選択して設定を保存します。<br>
	　設定を保存せずに終了するには Discard Changes and Exit にします。<br>
	　<img src="./msi12.png" width="340" height="255"><br>
	　<img src="./msi13.png" width="680" height="510"><br><br>

	9.動作確認<br>
	　Windowsが起動したら、Valorantでエラーが出ないか確認します。<br>
	　エラーが引き続き出る場合は、手順 6.のエラーが表示された場合を試してみてください。<br><br>
	　また下記の記事を参照してみてください。<br>
	　<a href="https://gamepc-base.jp/varorant-tpm-error-msi/" target="_blank">VALORANT TPM2.0エラー VAN9001の対処方法｜MSIマザーボード編</a><br>
	</p></details>
</section>
<hr>

<br><br>
</body>
</html>
