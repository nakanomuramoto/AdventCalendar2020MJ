# 2500円から初めるPhotogrammetry
RealityCaptureはPhotogrammetry（写真計測）用のソフトウェアです。<br>
（Reality CaptureはCapturing Reality社のソフトウェアです）<br>
### https://www.capturingreality.com/ <br>
公式は日本語対応していなくて、英語が苦手だととっつきにくさはありますが、優れたアプリケーションだと思います。<br>
以前のpromoというサブスクリプション方式のライセンスは廃止され、現在はppiという従量課金制のライセンスも提供しています。<br>
従量課金というと費用が青天井になってしまいそうで構えてしまいますが、たまに使うぐらいであれば逆に費用を抑えられます。<br>
今回は具体的な事例を金額も含め紹介します。<br>

## Reality Captureをインストール
これは"Reality Capture ppi 使ってみた"などで検索すると、他にたくさん紹介ページがあるので、そちらを参照してください。<br>

## 写真を撮影して、三次元再構成
たくさん写真を撮ってソフトウェアで処理するという基本的な方法もたくさん紹介されてますので、それらを参照してください。<br>
<br>
今回は取り込みやすそうなダイソーの汁椀を題材に選びました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_1.png" width="300"><br>
Photogrammetryで重要なのは、寸法の元になる**物差しを一緒に撮影する**ことです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_2.png" width="300"><br>
物差しを置けない場合は、画像上で位置を特定しやすくなる印を数か所準備しておきます。<br>
屋外であれば、柵や窓枠など四角いものの長さを測り、別途記録しておき、後述する距離の校正で用います。<br>
<br>
3Dモデルとテクスチャの投影、4DViewで動画を作成するところまでは費用が発生しませんが、ライセンスの内容は変更される可能性があるので要注意です。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_3.png" width="600"><br>
モデルが出来上がったら、次にPhotogrammetryの肝心なところ、計測を行います。<br>
<br>
## 計測、の前に、校正用のコントロールポイントの設定
計測する前に、校正用のコントロールポイントを設定します。<br>
コントロールポイントの設定は、3D View上で行う方法と2D image上で行う方法がありますが、今回は後者の一つの方法を紹介します。<br>
まず下準備として、レイアウトをウィンドウ左上にあるアイコンを選び、"1+2+1 Layout"に変更します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_8.png" width="300"><br>
次に、ウィンドウの真ん中の列の上の枠内を左クリックして選んでから、ウィンドウ上にある2D IMAGEタブを選びます。枠が青色の太い線で縁取りされます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_9.png" width="300"><br>
そして、左上にあるBlueボタンを押すと、選んでおいた枠がBlueカーソルの表示枠に設定されます。<br>
同様に、ウィンドウの真ん中の列の下の枠内を左クリックし、左上にあるGreenボタンを押し、選んだ枠をGreenカーソルの表示枠に設定します。<br>
これで下準備ができました。<br>
<br>
コントロールポイントの指定は、ALignmentタブのControl Pointsを押し、写真中の場所を左クリックしてコントロールポイントを設定します。<br>
座標を設定するコントロールポイントが映っている画像をウィンドウの左の列にあるImagesの中から選びます。<br>
このとき、**キーボードの2を押しながら左クリックで画像を選ぶ**と、greenカーソルの表示枠内に画像が表示されるはずです。<br>
もし、**キーボードの数字の1を押しながら、あるいは、押さずに左クリックで画像の名前を選ぶ**と、Blueカーソルの表示枠に画像が表示されるはずです。<br>
画像の表示枠を分けることで、複数のコントロールポイントの場所と数字を確認しながら設定することができます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_10.png" width="300"><br>
<br>
測定したい場所をコントロールポイントで指定します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_11.png" width="600"><br>
さらに細かい作業やTIPSは後日示します。<br>
<br>
## 計測、の前に、写真のライセンス登録
ここからは費用が発生します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_7.png" width="300"> <br>
PPIcreditという単位で提供されており、現在の最小購入単位が2000PPIcreditsで19.9ユーロになっています。写真の解像度と枚数で試算するフォームも提供されています。<br>
https://www.capturingreality.com/RealityCapture-PPI <br>
今回は**Galaxy Note 9のカメラで撮影した画像　4.6M; 2160pix x 2160pixの写真を154枚使っていますので、費用は約$2**でした。<br>
スクリーンショットの前後で写真を追加してしまい画像にある数字が変化していました。すみません。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_4.png" width="600"><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_4b.png" width="300"><br>
WorkflowタブのInput Licensesを押してネット経由でライセンスファイルを取得します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_5.png" width="600"><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_12.png" width="300"><br>
<br>

## 計測
今回は汁椀の底に近い部分の厚さを測定してみました。<br>
実物を手に取ると分かりますが、器の厚さが底に向かって厚くなっていることを感じますが、実際の厚さを測定したことがなかったです。<br>
<br>
ライセンス取得すると距離の推定結果が表示されます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_13.png" width="600"><br>
<br>
今回は実験なので、汁椀を切断し、実測してみました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day1_14.png" width="600"><br>
1mm単位の物差しを使い誤差も1mm程度なので、おおむね再現できていると思います。<br>
<br>
## まとめ
Reality Captureのppiライセンスの使用例を具体的な金額も含め紹介しました。<br>
今回は汁椀を約300円でキャプチャー、計測することができました。<br>
もちろん枚数を増やしたり、解像度が高い写真を使うと費用が増えますが、個人利用する頻度で考えるとリーズナブルな選択肢だと思います。<br>
また、VRやAR用にモデルをキャプチャーする場合、寸法は非常に重要な要素だと思いますので、寸法の校正を念頭に入れることをお勧めします。<br>
