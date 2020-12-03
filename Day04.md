# モノ撮り　「モノを回す」底面もキャプチャーする
Day3で説明した難易度が高いと言っていた「モノを回す」小物のキャプチャーですが、テクスチャフルで変形しない被写体であればちょっとした工夫で底面もキャプチャーすることができます。<br>
今回はその一つの方法を紹介します。<br>

## 背景の準備
背景に特徴点が出にくい背景を準備します。今回はトレーシングペーパーを下面と前面に敷きました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day4_1.jpg" width="300"><br><br>
この状態で画角内にトレーシングペーパーの外側が映らないよう、被写体を回して撮影を進めます。<br>
2Dimageのtie pointを確認すると、ほとんどが被写体上に分布しています。<br>
途中で、被写体の底面が映るような姿勢に変更します。今回はひっくり返しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day4_5.jpg" width="300"><br><br>
背景に特徴点がほとんどないので、被写体上にある特徴点でマッチングされることを期待しました。<br>
床の裏側からも撮影したとみなされたようで、このように画像がアライメントされました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day4_2.png" width="600"><br><br>

## 校正
物差しを置いて撮影できないので、今回は被写体上の寸法をあらかじめ測定し、コントロールポイントを配置しました。<br>
具体的には縁の直径を直交する2つの方向で測定しました。
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day4_3.png" width="600"><br><br>
Day1と同様に、底面の厚さの推定結果が実測結果とほぼ同等になりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day4_4.png" width="600"><br><br>

## まとめ
「モノを回す」小物のキャプチャーについて、テクスチャフルで変形しない被写体のキャプチャーを工夫する方法を紹介しました。<br>
背景に特徴点が抽出されにくい無地の白紙を使い、その白紙の外側が映らない画角で被写体を回しながら撮影することで、底面もキャプチャーすることができました。<br>
スケールを校正するために、被写体上であらかじめ寸法を測定した場所にコントロールポイントを配置しました。<br>

