# お化け屋敷対策　再読み込み　
Day14で部屋のキャプチャーを試した例を紹介しましたが、白い壁は穴が開いたり凸凹していたりお化け屋敷のようになりやすいです。<br>
白い壁は特徴点が抽出されにくいのでちぎった黒いテープを壁に貼ったり工夫したことがありますが、卵のプラスチック箱のような凸凹になったり苦労のわりによくならないことがありました。<br>
やはり平らな壁なのであればその部分のモデルは平らになってほしいです。<br>
ここでは積極的にズルしてモデルの一部を平面に修正し、そのモデルをReality Captureに再度読み込み直す方法を紹介します。<br>
## モデルをexportする
ReconstructionタブのExportにあるmodelをクリックし、モデルを出力します。今回はobjにしました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_1.png" width="600"><br><br>
ファイル名を入力した後の窓でTransform presetをblenderにしました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_1a.png" width="600"><br><br>
<br>
## Blenderで壁にplaneを置く
さきほどのobjファイルをimportします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_2.png" width="600"><br><br>
ためしに壁の部分をくりぬき、同じ部分にpleneを配置しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_3.png" width="600"><br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_3a.png" width="600"><br><br>
修正したモデルと追加した平面をJoinしexportしました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_4.png" width="600"><br><br>
向きを変更します。epxortの設定時のforwardが時々間違うのでReality Captureで取り込んでみて確認しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_8.png" width="600"><br><br>
<br>
## Reality Captureにmodelを読み込む
ReconstructionタブのImportにあるImport modelをクリックし、修正したobjファイルをReality Captureに取り込みます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5.png" width="600"><br><br>
ReconstructionタブのModel color＆Texture欄にあるUnwrapをクリックし、UVマップを生成します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5a.png" width="600"><br><br>
よく見ると追加したplaneの部分が一つの黒あるいは白になっていました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5b.png" width="600"><br><br>
このままTextureするとそのPlaneの部分が解像度が低い状態になりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5c.png" width="600"><br><br>
<br>
## Blenderで壁に貼ったplaneのメッシュを細かくする
もう一度Blenderに戻りPlaneをeditorモードでRoopCutしてメッシュを細かくしました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5d.png" width="600"><br><br>
そのモデルをReality Captureに取り込みUnwrapすると、さっきの大きな一つの色の部分が細かいチェスボード状になりTextureの解像度も高くなりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5e.png" width="600"><br><br>
<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_5f.png" width="600"><br><br>
<br>
試しに壁と小窓のガラスを全面書き直しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_6.png" width="600"><br><br>
<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_6a.png" width="600"><br><br>
<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_6b.png" width="600"><br><br>
<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_6c.png" width="600"><br><br>
正しいキャプチャーではありませんが、出先によっては逃げ技として使えると思います。<br>
<br>
## まとめ
正しいキャプチャーではありませんが白い壁の穴や凸凹を修正する方法を紹介しました。<br>
注意として、モデルのファイル形式やBlenderで修正した内容によってReality Captureで読み込めないときがあるようなので少しづつ試しながら進めた方が良いと思います。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day15_7.png" width="300"><br>
<br>
