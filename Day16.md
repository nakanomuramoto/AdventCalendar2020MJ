# テクスチャ解像度 unwrap設定
ReconstructionタブにあるUnwrapの設定によってテクスチャーの解像度などを設定できますが、何となくOptimalを使っていて影響を調べたことがなかったです。<br>
今回はテストチャートを作成しUnwrapの設定による影響を実験してみました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_5.png" width="300"><br><br>
<br>
## Unwrapの設定
ReconstructionタブにあるUnwrapをクリックすると1Dsの下に設定が表示されます。<br>
Unwrap parametersの左にある＋印を押し表示されるStyleをFixed texel sizeに変更し、Texel sizeをCustomにすると値を入力できるようになります。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_1.png" width="600"><br><br>
例えばチャートの一番粗い線幅0.005mと同じ値にするとその線幅がかろうじて分かる程度の外観になりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_2.png" width="600"><br><br>
Texel sizeをチャートの細かい方の線幅0.0005mにすると、その線幅がかろうじて分かる程度の外観になりテクスチャは使用率が上がりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_2b.png" width="600"><br><br>
チャートの一番細かい線幅よりも小さいOptimal texture sizeと同じくらいの値にした結果です。<br>
このときはMax texture resolutionの4096x4096だったのですが入りきれなくて3枚になったようです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_3.png" width="600"><br><br>
Max texture resolutionを8192x8192にすると1枚にまとまりました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_3a.png" width="600"><br><br>
<br>
## scaleを設定していなかった場合
上記はscaleを入力してキャリブレーションしていましたが、キャリブレーションする前の状態だと寸法の単位がunitになっていて程度を理解しにくかったです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day16_4.png" width="600"><br><br>
テクスチャの解像度に関してもscaleの入力が有用であると考えてよさそうです。<br>
<br>
## まとめ
Unwrapのパラメータについて実験した結果を紹介しました。<br>
Scaleの入力はテクスチャの解像度を理解するためにも重要だと思われます。<br>
<br>
