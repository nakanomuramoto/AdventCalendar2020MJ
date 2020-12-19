# レンズの設定
Day18のアライメント結果を見ると下の方のカメラ位置の一部が外側に広がっていました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day19_1.png" width="600"><br><br>
またDistortionの様子を表示すると同じレンズでほぼ同じ条件で撮影しているのに画像間で大きく異なる様子になっていました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day19_4.png" width="600"><br><br>
Distortionnの様子は2Dタブを選択しDisplayにあるLens Distortionにチェックを入れると表示されます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day19_3a.png" width="600"><br><br>
撮影した本人しか分からないことですがこの時のカメラの運び方は被写体からほぼ同じ距離に保っていました。<br>
アライメントの推定結果が現実と異なったのはレンズ設定をしていなかったからと思います。<br>
レンズの設定やカメラの運び方は事実と合わせた方が良いと思いますので、そのために工夫した方法を紹介します。<br>
## レンズの設定
このときの撮影はフォーカス固定にしていましたので、焦点距離とディストーションはほとんど同じだったはずです。<br>
スマホのカメラでしかも動画撮影なので実際は何をされているか分からないという疑問は残りますが、すべての画像でレンズの焦点距離とディストーションの初期設定は同じとします。<br><br>
1DsのImagesにある画像の名前の一つを左クリックしてCTRL+aを押し画像をすべて選択し、下の方にあるPrior calibrationのCalibration groupを0に、PriorをApproximateにして、Focal lengthを使っているスマホの換算焦点距離にしました。<br>
そしてPrior lens distortionのLens groupを0に、PriorをApproximateにして、今回はスマホカメラのレンズなのでBrown4にしました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day19_5a.png" width="600"><br><br>
それからAlignmentすると、カメラの推定位置は撮影したときの事実に近くなりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day19_3.png" width="600"><br><br>
lens distortionには他のモデルも準備されていますが再投影誤差が小さくなるモデルを選ぶのではなく、事実に合わせたモデルを選択して結果として誤差が小さくなることが重要だと思います。<br>
<br>
## まとめ
カメラとレンズの設定を事実に合わせる方法を紹介しました。<br>
初期条件と制限を与えない限りReality Captureは再投影誤差を減らすようこねくり回してつじつまを合わせようと努力するので、結果的に間違うことがあるかもしれません。<br>
またスマホのカメラだと中で歪補正や手ブレ補正などどんな処理をしているか分からないので、上記のような設定が難しくなる可能性がありそうです。<br>
