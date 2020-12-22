# マスクの応用
YouTubeのCapturing Realityチャンネルにあるこちらの動画を参考に作業の手順をまとめました。<br>
"RealityCapture tutorial: Scan objects from all sides using Masks."<br><br>
https://www.youtube.com/watch?v=xxsdbzBwWLE&t=530s
<br><br>
モデル中の被写体の部分だけ指定してマスクを生成し、画像とマスクを再度読み込み複数のComponentをまとめる手法のようです。<br>
今回は同じ被写体をほぼ同じ場所で別の日に撮影した画像から一つのモデルを復元してみました。<br><br>
ただ失敗する例も確認できたので併せて紹介します。<br>

## マスクの生成
まずモデルの必要な部分をfilterで残します。<br>
ReconstructionタブのSelectionにあるLassoやRectで不要な部分を選びます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_3.png" width="600"><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_4.png" width="600"><br>
<br>
Invertで反転させToolにあるFilter Selectionをクリックするとオレンジ色になっているところを残すことができます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_5.png" width="600"><br>
<br>
そしてReconstructionタブのExportにあるDepth and Maskを選び、マスクを生成します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_8.png" width="600"><br>
<br>
Export Camera Detphsは不要なので"No"にして、Export File Namingは対応させたいので"Original File Name"、
Undistort imagesはオリジナルと重ねたいので"No"にします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_9.png" width="600"><br><br>
その結果、マスクファイルが生成されます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_10.png" width="600"><br><br>
<br>
同様に別の日に同じようなセッティングで撮影した画像で復元したモデルの方でもマスクファイルを生成します。<br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_10a.png" width="600"><br>
<br>
## 元の画像とマスク画像をドラッグアンドドロップする
1Dsのリストを見るとマスクファイルは表示されていませんが取り込まれています。<br>
2Dビューをアクティブにしてtabキーを押すとマスクされる部分が暗めになります。ここでは下側の2Dの枠がマスクの確認状態です。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_11.png" width="600"><br>
<br>
ここからAlignmentすると別の日に撮影した画像が同じComponentに含まれました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_14.png" width="600"><br>
<br>
## 失敗した例
別の被写体について同じカメラで撮影し同様な手順を行ったのですが一つにまとまりませんでした。<br>
理屈ではうまくできると思ったのですが、被写体自体に特徴点を抽出しにくいせいか撮影枚数が足りなかったのか、今回は原因を突き止められませんでした。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day22_15.png" width="600"><br><br>

## まとめ
モデルの復元箇所を指定することでマスクを生成し、別の日に撮影した画像と合わせてモデルを復元する方法を試しました。<br>
残念ながら今回は再現性が高い条件を見つけ出すことができませんでした。<br>
追撮した画像を付け足せるようになると便利なので、次の機会に再現性が高い条件を探してみようと思います。<br>
