# オルソプロジェクション
普段の写真の画像は透視投影といい、遠いところが小さく映ります。<br>
正面にある被写体も画面の中央は大きく映り画面の端の方は小さく映るので、特にスマホカメラのような広角レンズで近づいて顔を撮ると鼻が大きく映ります。<br>
そのような歪がない投影で作った画像が正射投影図、オルソ画像と呼ばれます。<br>
オルソ画像を得るためには顕微鏡や土器の撮影用などテレセントリック光学系のレンズを用いたカメラを用いるようです。<br>
代替手段として非常に焦点距離が長いレンズで、非常に遠い距離から撮影する方法もあるようです。<br>
Reality Captureにもオルソプロジェクションの機能がありますが、紹介記事が見当たらなかったので、試行錯誤で試した結果を紹介します。<br>

## Ortho projection
ReconstructionタブのToolsにあるOrtho Projectionをクリックします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_1.png" width="600"><br>
3Dview枠に表示される矢印が示す面が投影されるます。1Dsの下に表示されるOrtho Projection ToolにあるTypeをArbitaryにして、生成したい向きの四隅の灰色の四角をクリックして向きを選択します。<br>
**このとき作成する画像の左上に当たる隅をクリック**します。その隅が黄色で表示されます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_2.png" width="600"><br>
Ortho Projection ToolにあるRenderをクリックするとオルソプロジェクションの画像が生成されます<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_3.png" width="600"><br><br>
<br>

## Batch処理
効果が分かりにくかったので、別の被写体を準備しました。<br>
2DViewのGreen枠に上面から撮った画像を選んでいます。顔を正面に向けて並べた3体の人形ですが、
2DViewのBlue枠に表示した正面から撮った画像を見ると両脇の人形は外を向いているように映っています。<br>
この被写体についてオルソプロジェクションしてみました。<br>
3Dview中で生成画像の向きを変えて指定し、Ortho Projection ToolにあるAdd to Batchすると、一括処理する準備ができます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_4.png" width="600"><br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_5.png" width="600"><br><br>
1Dsに表示されている画像名を左クリックしOrtho Projection ToolにあるRenderをクリックすると、
複数のオルソプロジェクションの画像を生成し表示されます。<br>
このときコントロールキーを押しながら左クリックして1Dsに表示されている画像名を複数選択しないと一括処理されませんでした。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_8.png" width="600"><br><br>
写真名をライセンス登録しないとオルソプロジェクションの画像にウォーターマークが入るようです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_6.png" width="600"><br><br>
写真名をライセンス登録してrenderし直すとウォーターマークが消えました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day11_7.png" width="600"><br><br>
スマホカメラで撮影した画像では外を向いているように見えた両脇の人形が正面を向いているように見えます。<br>
また上からみた画像では両脇の人形の鼻が体の中央に映りまっすぐ立っているように見えます。<br>
<br>
## まとめ
オルソプロジェクションの画像の生成方法の手順を紹介しました。<br>
UnityなどゲームエンジンやCADを使っている方はなじんだ投影なので、図面を起こしたい人にとっては役に立ちそうです。<br>
