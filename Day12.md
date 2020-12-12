# 3DViewの操作方法
3DViewの向きや位置をマウス操作していて急に変な向きになって困ったことがありましたので、使っている頻度が多い操作をまとめました。<br>
<br>

## リセット
表示領域がすっ飛んでしまったり向きの調整が分からなくなったとき、**キーボードのrを押すと初期状態に戻ります**。<br>
CTRL+zで表示領域と向きが復帰**しない**のが悩ましいところです。<br>
押す前　Greenの枠の表示を間違って回転させてしまった<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day12_2.png" width="600"><br><br>
押した後　Greenの枠をrで戻した<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day12_3.png" width="600"><br><br>
おそらくreconstruction regionが見える視点に戻るのだと思いますが一番重宝する操作だと思います。<br>

## Numキー入力
0と1はそれぞれパースペクティブ表示とオルソ表示の切り替えです。<br>
1の枠がパースペクティブ表示、2の枠がオルソ表示です。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day12_1.png" width="600"><br><br>
2と3は上面と下面、4と5は正面と背面、6と7が左側面と右側面で、それらはオルソ表示です。<br>
このモデルは正面の設定が合ってなかったです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day12_4.png" width="600"><br><br>
4から7はgroundの傾きを直すとき便利です。<br>
2から7はオルソ投影の状態です。マウスの左ボタンでドラッグすると位置を変更、ホイールで拡大縮小です。0か1で復帰します。
<br><br>

## マウス入力
右クリックを押しながら動かすとピッチとヨーの角度変更、左クリックを押しながら動かすと上下左右の平行移動です。<br>
角度変更は小さいピボットを中心に変化します。<br>
ピボットが見えてない視点で角度変更すると変化が大きくモデルを見失いやすいので、**左ボタンのダブルクリックでピボットの位置を変更**してもよいと思います。<br>
パースペクティブ表示の時、shiftキーを押してホイールを回すと画角が変更されます。モデルに近いと見た目の変化が小さくわかりにくいかもしれません。
オルソ表示の時だと表示範囲の拡大縮小になります。<br><br>
1と3の枠がパースペクティブで3は画角変更時、2と4の枠がオルソで4はサイズ変更時。
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day12_1.png" width="600"><br><br>

最後に特殊なのがshiftキーを押して右ボタンを押しながら左ボタンを押し、左右にマウスを動かすと画面に対して垂直な軸に回転するロール操作になります。<br>
偶然回転してしまって戻せなくて焦ったことがありました。<br>
2の枠が回転させた場合。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day12_2.png" width="600"><br><br>
<br>
## まとめ
3DView表示中の操作について紹介しました。<br>
使い始めの頃にリセットの仕方が分からなくて大変だったのを思い出しました。<br>
