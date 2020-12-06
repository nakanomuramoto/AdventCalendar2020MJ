# Alignmentで画像がまとまらないとき
たくさんの画像を撮影しAlignmentしたとき、画像が一つのComponentにまとまらないことはよくあります。<br>
<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_1.png" width="600"><br><br>
泣きながらControl Pointを設定する方法が定石だと思いますが、いろいろ試してきた方法を紹介します。<br>

## 撮影して画像を補う
おそらく一番理に適っていて効果が高いのは、分かれているComponentの間が映っている画像を追加撮影することだと思います。<br>
撮影場所にノートPCを持ち込み撮影した画像を入力して、その場でAlignmentの結果を確認します。<br>
可能な限り1つのComponentにまとまるまではシーンとセットをばらさないことが望ましいかもしれません。<br><br>

## コントロールポイントを打つ
チュートリアル動画でも紹介されている方法です。<br>
分かれているComponent間で映っているControl Pointを設定し、それらの点が同じことをコンピュータに指定します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_2.png" width="600"><br><br>
今回の写真はDSLRでレンズの絞りを明るい設定にしていたので奥行き方向でピントが合っておらず、ぼけている部分にControl Pointを設定せざるを得ませんでした。<br>
Alignmentはできましたが、想像通り残念ながらReconstruction中に先に進まなくなりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_8.png" width="600"><br><br>
<br>

## Merge Componentsする
別のComponentにAlignmentされた画像を目的のComponentに追加する方法です。<br>
追加したい画像を持っているComponentを選択し、その3D表示枠内で左クリックしてアクティブにして、CTRL+Aで画像を選択します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_4.png" width="600"><br><br>
この状態で追加する先のComponentを1Ds内の名前をクリックし、Alignmentの中にあるMerge Componentsをクリックします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_5.png" width="600"><br><br>
必ずうまくいくとは限らないと思いますが今回はまとまりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_6.png" width="600"><br><br>
<br><br>

## 処理する画像を継ぎ足していく
まとまりそうな画像を選んでAlignmentし、そのComponentが映っていそうなほかの画像をwindowsのフォルダから1Ds枠内にドラッグアンドドロップしてAlignmentするという作業を順次繰り返していきます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_7.png" width="600"><br><br>
<br>
一度にたくさんの画像をAlignmentすることが難しく少しづつAlignmentするカメラを増やしていくようなものかもしれませんが、広域キャプチャーのように撮影画像がとても多いときによく使っていた手法です。<br>
今回の例では再現が悪く、継ぎ足し方を変えて試したときにAlignmentはできるがReconstructionで止まってしまうということがありましたので、必ずうまくいくとは限らないということだと思うので注意が必要です。<br>
<br>

## まとめ
たくさんの画像が一つのComponentにまとまらないときに取ってきた方法を紹介しました。<br>
いずれもケースバイケースで必ずうまくいったり再現性が高いわけではありませんが、Control Pointを打たなくてもよくなる場合もありますので、手段をとして知っておくとよいかもしれません。<br>
<br>
これらの方法はAlignment settingのパラメータによって結果が変わります。パラメータの値は明確にリセットを指示しない限り保管され続けているので、適用している条件は一度確認した方が良いと思います。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day7_3.png" width="300"><br><br>
