# モノ撮り　質感を再現する小技
Day4は被写体を回しながらキャプチャーする方法を紹介しましたが、表面の質感は失われていました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day5a_7.png" width="300"><br><br>
これは固定された照明の下、スペキュラや陰の場所が移り変わりながら撮影した画像からテクスチャを生成しているため、原理的に仕方ない現象だと思います。<br>
陰もなくデライト出来ているので、正しい結果だと思いますが、味気がありません。<br>
本来であれば、DCCツールにモデルをexportしてテクスチャやマップを貼りなおすことが必要ですが、今回は見る角度の制限はあるもののお手軽に撮影時の表面の質感を表示する小技を紹介します。<br>

## 3Dビューの操作
その前に、グリッドやコントロールポイント、カメラ位置、ピボットが邪魔なので、消す方法を紹介します。
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day5a_1.png" width="600"><br><br>
- グリッド 3Dタブの真ん中くらいにある"Scene Render"中の"Show Grid"のチェックを外す
- コントロールポイント　3Dタブの左の方にある"Alignment Cameras"中の"GCPs"のチェックを外す
- カメラ位置　3Dタブの真ん中くらいにある"Alignment Cameras"中の"Enable"のチェックを外す
- ピボット　3Dタブの右のほうにある"Tools"中の"Center Pivot"の"Hide pivot"を選ぶ


<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day5a_2.png" width="600"><br><br>

カメラ位置だけは欲しかったので、再表示します。<br>

## ほしいカメラの位置だけテクスチャに使う
Reality Captureはテクスチャを生成するときに使う画像を選ぶことができます。<br>
例えば、2D Viewのblue枠に表示されている画像だけでテクスチャを生成するよう指定しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day5a_3.png" width="600"><br><br>
まず全部のカメラを選択します。3Dの枠を選び、**CTRL+Aを押します**。<br>
選択解除したい画像を、**Shiftキーを押しながら左クリックします**<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day5a_4.png" width="600"><br><br>
<br>
画面左にある1Dsの下に表示されているSelected xxx inputsの中にある"Enable texgturing and coloring"を"Disable"にします。<br>
そして、ReconstructionタブのTextureを実行します。<br>
そうすると、見てほしい視点の周辺だけは質感を表現できているテクスチャを貼ることができました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day5a_6.png" width="600"><br><br>

## まとめ
特定の角度の範囲に限定されますが、質感を表現できるテクスチャを生成する小技を紹介しました。<br>
テクスチャを生成するときの画像を選択する方法は他にも応用できますので、後日紹介します。<br>
