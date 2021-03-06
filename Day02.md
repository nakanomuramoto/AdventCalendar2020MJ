# Control pointの設定と寸法の校正
Day1において、Control Pointの設定と寸法の校正の概略を紹介しました。<br>
Photogrammetryは、異なる視点から撮影した複数の画像から3次元の形状を復元するSfMという技術を利用しています。<br>
SfMはスケールの不定性という性質があるため、そのままでは復元されたモデルの大きさが分かりません。<br>
言い換えると、短距離で移動しながら小さい被写体を撮影したのか、長距離で移動しながら大きい被写体を撮影したのか、区別がつかないということです。<br>
したがって、寸法を校正する必要があります。<br>
具体的には、コントロールポイントという測定箇所の位置や座標を画像内に設定し、コントロールポイントの座標の数値やあらかじめ測定していたコントロールポイント間の距離を入力することで、測定寸法を推定します。<br>

## 寸法が分かるものを被写体と一緒に撮影
Day1と同じ画像と復元モデルを使用します。寸法が分かる物差しを一緒に撮影しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_2.png" width="300"><br><br>
## Control pointを指定する
物差しが映っている画像を選択します。<br>
**キーボードの2を押しながらヒエラキー（1Ds）の枠内にある画像の名前、あるいは、3D view中のカメラアイコンを左クリック**します。<br>
すると、レイアウトの真ん中の列の下の段の画像として表示されます。なお、予めDay1に示した画像を表示する枠の設定を済ませてください。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_2.png" width="600"><br><br>
AlignmentタブにあるControl Pointをクリックすると、マウスのアイコンにプラスマークが表示されます。
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_3.png" width="600"><br><br>
この状態で2Dの枠内を左クリックするとコントロールポイントが追加されます。<br>
もし、**単に枠をアクティブにしたいだけであれば、スペースキーを押しながら左クリック**します。<br><br>
新しいコントロールポイントを作るときは、1Dsの枠内にある"Control points"中の"Create"をクリックし、画像内にコントロールポイントの位置で左クリックします。<br>
既に設定しているコントロールポイントに追加するときは、1Dsの枠内にある"Control points"中のコントロールポイントの番号をクリックし、画像内にコントロールポイントの位置で左クリックします。<br><br>
ところで、それぞれの表示枠の右上にあるアイコンを左クリック長押しすると、その枠内で表示する内容を変更できます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_1.png" width="300"><br><br>
point0を選んでから物差しのゼロの目盛りの箇所で左クリック、point1を選んでから横方向の100mmの目盛りの箇所で左クリック、point2を選んでから縦方向の100mmの目盛りの箇所で左クリックします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_5.png" width="600"><br><br>
<br>
予めコントロールポイントを設定していたので、ここで左枠のControl Pointsにあるpoint2中の緑色で目印がついているファイル名のところを見ると"9.2pix"と表示されています。これは誤差です。<br>
つまり、推定されたカメラの位置から撮影したら表示されるはずのコントロールポイントの位置と、手入力されたコントロールポイントの位置にずれがあることを示しています。<br><br>
ファイル名をクリックするとその画像が2Dのblueの枠内に表示されます。<br><br>
**キーボードの"f"を押すと、コントロールポイントが見える状態に画像が拡大されます**ので、point2の部分をマウスのホイールを回して拡大していくと、丸印の位置が目盛からずれていることが分かります。<br>
ちなみに、**キーボードの"r"を押すと、画像全体が表示されます**ので、マウスのホイールを回して拡大縮小する手間を省けます。<br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_6.png" width="600"><br><br>
丸印を左クリックでドラッグして、目盛の位置に合わせると、表示されていた数字が小さくなりました。
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_6a.png" width="600"><br><br>
以降、画像のファイル名をクリックし、コントロールポイントを設定する手順を繰り返します。<br>
その際に下記のようなショートカットがありますので、先ほどのキーボードのfキーと併用すると便利です。<br>
- キーボードの上下ボタンでヒエラキーのControl points中に抽出されたリスト内を移動 <br>
- キーボードの左右ボタンでヒエラキーのImagesのリスト内を移動<br>


コントロールポイントを設定するたびに、その画像における誤差が表示されますので、誤差が小さくなるように、画像中の丸印をマウスの左ボタンでドラッグし、位置を調整していきます。<br>
ただし誤差を小さくするために、間違った位置に丸印の位置を修正することは正しくないと思いますので、注意が必要です。<br>
これは嘘でつじつまを合わせるようなものなので、位置を修正して誤差が小さくなるとしても、正しいと見える位置に合わせ直したほうが良いです。<br>
そして誤ったコントロールポイントの設定やブレた画像が入力されているなど、ほかの原因を疑った方が良いと思います。<br>
## Control pointをGround Controlにする
ヒエラキー（1Ds）の枠内にあるControl pointの名前を左クリックすると、ヒエラキーの下にコントロールポイントのセッティングが表示されます。<br>
TypeをGround Controlに変更し、座標の数値を入力します。<br>
使用している座標系の単位がmなので、Control point1の入力値は(-0.1, 0, 0)<sup>T</sup>です。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_7.png" width="600"><br><br>
同様にControl point 0, 1, 2のtypeと数値を入力したら、AlignmentタブのUpdateをクリックすると再計算されます。<br>
また、3DViewの配置も修正されます。<br><br>
Control pointsの名前の右側に"e:0.00m"と表示されているのは、推定結果と設定値との誤差です。<br>
この値が大きいときは、画像内の丸印の位置がずれているか、数値の入力値が間違っているか、画像がぶれているなど入力データに不備があるなど、いくつかの原因が考えられます。<br>
意外によくあるのは、あらかじめ測定していた距離の測定誤りです。<br><br>
コントロールポイントを設定する画像の枚数は、ケースバイケースだと思いますが、経験的に4-5枚設定しています。雑にたくさん設定するよりは、少なくてもよいから正確に設定する方が良いと思います。<br>
<br>
## 測定箇所を指定する
コントロールポイントの設定方法と同様に、寸法を測定したい2点を設定します。<br>
AlignmentタブのDefine Distanceを選択し、ヒエラキーのCreate distanceをクリックして、distance0の条件を設定します。ヒエラキーの下の枠に表示されているSelected constraintにあるAとBに寸法を測定したい2点の名前を入力します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day2_8.png" width="600"><br><br>
Day1に示した手順で写真を登録すれば、距離の推定結果がCalculated distanceに表示されます。<br>
<br>
## まとめ
Photogrammetryの重要な機能である測定について手順の例を説明しました。<br>
コントロールポイントの設定手順の一例と、いくつかショートカットを紹介しました。<br>
<br>
