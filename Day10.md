# ノーマルマップとデイスプレイスメントマップの生成
export先のDCCツールにおける表現力を高めるためノーマルマップとディスプレイスメントマップの生成を試してみました。<br>
確認するためにBlenderを用いましたが使いこなしが不十分なため、間違えているところがあったら修正していただけると幸いです。<br>
<br>

## ポリゴン数を減らす
まずは大きすぎるポリゴン数を減らします。減らす前は1.9Mでした。<br>
ReconstructionタブのToolsにあるSimplify Toolを使います。<br>
画面の左側にある1Dsの下に表示されたSimplify Toolに変更後のポリゴン数を入力し一番下のSimplfyをクリックします。<br>
今回はポリゴン数を4000に減らしました。<br>
<img src="https://github.com/nakanomuramoto/Toio1/blob/main/picture/Day10_1.png" width="600"><br><br>

## UVマップを生成する
ポリゴン数を変更した後にUVマップを再作成します。<br>
同じところにあるUnwrapを使います。<br>
細かい数字は後日紹介しますが1Dsの下に表示されたUnwrap ToolのUnwrapをクリックします。<br>
<img src="https://github.com/nakanomuramoto/Toio1/blob/main/picture/Day10_2.png" width="600"><br><br>
3D表示枠をクリックし画面上の3D SceneタブにあるScene RenderのSweetをクリックすると、テクスチャの様子をチェスボードで確認できます。<br>
<img src="https://github.com/nakanomuramoto/Toio1/blob/main/picture/Day10_3.png" width="600"><br><br>

## テクスチャを生成する
ReconstructionタブのToolsにあるTexture Reprojectionを使います。<br><br>
1Dsの下に表示されたReprojection model textureの欄にSimplify前のモデルと後のモデルを選択し、
Displacement reprojectionとNormal reprojectionをEnableに設定し一番下のReprojectをクリックします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_4.png" width="600"><br><br>

1DsのComponentの中のModel TexturesにColor、Difuse、Normalテクスチャが表示されます。<br>
それぞれを表示して確認しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_5.png" width="600"><br><br>
1DsのComponentの中のModel Texturesの右側にある目のマークをクリックすると3DViewに適用されるテクスチャを変更できます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_13.png" width="600"><br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_14.png" width="600"><br><br>
## モデルとテクスチャをexportする
modelをexportし、Blenderで表示してみました。<br>
3D表示枠を選んだ状態で3D sceneタブのExportにあるModelをクリックし、Alembicで出力しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_6.png" width="600"><br><br>
Export Modelの窓が開きますので、それぞれのテクスチャを出力するようTexturing settingsを設定します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_7.png" width="300"><br><br>
Export中にこちらのような注意が表示されますが、すみません、意味が分かりませんでした。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_8.png" width="300"><br><br>

## Blenderに取り込む
Blender上で先ほどのモデルをimportしそれぞれのテクスチャを貼りました。<br>
正直なところBlenderは使いこなせていないので、間違っていたら修正をお願いします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_9.png" width="600"><br><br>
Difuseマップのみ<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_11.png" width="600"><br><br>
Displacementマップのみ。パラメータは修正しました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_10.png" width="600"><br><br>
Normalマップのみ。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day10_12.png" width="600"><br><br>.

## まとめ
DCCツールにおける表現力を高めるためノーマルマップとディスプレイスメントマップの生成した例を試してみました。<br>
Unwrapのパラメータについて実験した結果は後日紹介します。<br>
