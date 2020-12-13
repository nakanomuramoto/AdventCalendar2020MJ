# photogrammetryに関係する年表
Reality Captureは2016年にリリースされたとのことですが、photogrammetryはいつごろ生まれたのか、それに関係する技術が生まれた時期を調べてみました。<br>
つまみ食いでレベル差もおおきく恐縮ですが、それぞれの事柄の関係を理解する基礎知識として面白いと思ったのでまとめました。<br><br>

## photogrammetry以前の研究
#### 1525年 Dürerが透視画法の幾何学的原理を記す
#### 1630年ごろ Desarguesが射影幾何学の研究の中で独自の透視図法を発表
#### 1725年 Capplerが前方交会法と同じ手法で山地の地図を2か所から作成　
#### 1759年 Lambertが後方交会法により撮影画像から被写体の位置を求めるパースペクティブ像の数学原理を示した
#### 1840年ごろ　Aragoがダゲレオタイプカメラの測量への利用を説明

## photogrammetyの始まりとエピポーラ幾何学の登場
#### 1867年 Meydenbauerがカメラと測定器を一つにまとめ、建築雑誌に掲載された論文の中で、初めて"Photogrammetry"という言葉を用いた 今後この単語が採用されるようになった
#### 1883年 Hauckが発表した論文の中でドイツ語のKernpunkt（エピポール）を使った
#### 1908年 Von Sandenは博士論文でエピポールを決定する方法についての最初の包括的な記述を発表した
#### 1934年 BaeschlinとZellerによる "Lehrbuch der Stereophotogrammetrie (Text book of Stereophotogrammetry) "というタイトルのドイツ語の本が出版された
#### 1952年 MiskinとPowellによって "Text book of Photogrammetry "というタイトルで英訳され、エピポールやエピポーラ平面などの英語の等価用語が紹介された

## コンピュータビジョンとの融合
#### 1959年 Thompson は写真測量における相対方位を決定するために、 斜交行列と直交行列からなる方程式を初めて提示した
#### 1964年 Ackermann は空中三角測量のコース調整とブロック調整の発展について講演
#### 1971年 Brown はカメラキャリブレーションのレンズの放射方向歪みとディセンタリング歪みのモデル化を論文で発表
#### 1981年 コンピュータビジョンの分野で、Longuet-Higginsが、Thompsonの方程式と似た3×3の行列を最初に導入した（後の基礎行列）
#### 1991年 Koenderinkがアフィン幾何による一般化された幾何の下で不変な形状が画像から復元できることを示した
#### 1992年 FaugerasやHartleyが射影幾何により不変な形状が画像から復元できることを示した
#### 2002年　Schaffalitzky-Zissermannらが小規模な未整列画像データセットに対する復元を成功　ただし"plane sweep"という壁や地面などの平面を決定する手法を利用
#### 2006年　Snavelyらが大量の個々人の撮影画像から三次元形状を復元する"Photo Tourism"を発表
#### 2009年　Agarwallらが大量の個々人の撮影画像から三次元形状を復元する"Building Rome in a day"を発表
<br>

## 参考文献
- https://en.wikipedia.org/wiki/RealityCapture <br>
- 「ジェラール・デザルグの透視図法」,　井村俊一 <br>
- 「写真測量における三次元画像計測」,　小林和夫 <br>
- "ALBRECHT MEYDENBAUER - PIONEER OF PHOTOGRAMMETRIC DOCUMENTATION OF THE CULTURAL HERITAGE", J. Albertz, https://www.semanticscholar.org/paper/ALBRECHT-MEYDENBAUER-PIONEER-OF-PHOTOGRAMMETRIC-OF-Albertz/65a85156676884a8d266108fc87b2a12018bb199　<br>
- Bundler, http://www.cs.cornell.edu/~snavely/bundler/bundler-v0.4-manual.html　<br>
- "Camera Motion Estimation for Multi-Camera Systems", Jae-Hak Kim　<br>
- 「講座：バンドル法　第二回 バンドル法と空中写真測量の歴史」, 那須 充, https://www.jstage.jst.go.jp/article/jsprs/51/2/51_108/_pdf　<br>
- "photo tourism", http://phototour.cs.washington.edu/
- 三次元画像計測の基礎　－バンドル調整の理論と実践－　東京電機大学出版局　一般社団法人　日本写真測量学会編　
- コンピュータビジョン　ー視覚の幾何学ー　コロナ社　佐藤淳　<br>
