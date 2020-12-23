# Blenderを使ったカメラプロジェクションによるテクスチャの生成　
個人的に頑張っていたテーマがスイーツだったのですがSfMの復元だけだと限界があるようでした。<br>
こちらが入力する元の画像です。イチゴがつやつやでおいしそうです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_0.png" width="300"><br>
こちらが復元結果です。イチゴがカピカピでまずそうです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_0a.png" width="600"><br>
イチゴが乾いているように見えるのはテクスチャがほとんど拡散成分だからだと思います。<br>
<br>
そこで今回はYouTubeのCapturing Realityチャンネルにあるこちらの動画のBonus部分を参考に、イチゴの表面にスペキュラが入っている画像をテクスチャに投影させました。<br>
"RealityCapture tutorial: Camera projections in Blender"<br>
https://www.youtube.com/watch?v=yq0XjvBlsiU
<br>

## Alembic形式でモデルをexport
こちらのように復元したモデルを使いました。<br>
カメラはいつものGalaxy Note 9です。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_1.png" width="600"><br><br>
ReconstructionタブのExportにあるModelをクリックし、ファイル形式をAlembic形式にします。<br>
Export Modelの窓でCamera settingsを下の図のように指定し、Export transformatin settingを"Blender"にします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_3.png" width="600"><br><br>

## BlenderにモデルをimportしカメラのFOV表示サイズを修正する
import後のカメラのFOV表示サイズが大きいです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_4.png" width="600"><br><br>
pivotを"Individual Origins"に変更し、sキーを押してからマウスを移動させ、カメラのFOV表示サイズを大きさを修正します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_5.png" width="600"><br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_6.png" width="600"><br><br>

## モデルの向きを修正する
pivotを"3D Cursor"に変更し、rキーを押してからxキーを押し、マウスで移動させるか左下の角度入力欄に90を入力し回転させます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_7.png" width="600"><br><br>

## カメラとプロジェクションする画像を選ぶ
プロジェクションしたい画像を撮影したカメラを選択します。<br>
右側のカメラマーク（Object Data Property）を選びカメラの名前をコピーします。<br>
Background Imagesにチェックを入れAdd Imageを押し、その下にあるOpenをクリックしてからRealityCaptureから出力したUndistortさせた画像を選びます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_12.png" width="600"><br><br>
右側のScene Propertyを選び、Cameraに先ほどコピーした名前をペーストします。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_29.png" width="600"><br><br>
Numpadの0を押しカメラ視点に変更すると画像サイズが合っていないので、右側のOutput Propertyの画像解像度を画像の数値に合わせます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_14.png" width="600"><br><br>
Viewport ShadingのX-rayにチェックを入れ数字を変更すると、モデルと画像の重なり具合を確認できます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_15.png" width="600"><br><br>

## UVマップを作成する
カメラプロジェクションのUVマップを生成します。<br>
モデルを選択した状態で右側のObject Data Propertyを選び、UV Mapsを追加して画像の名前を記入します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_16.png" width="600"><br><br>
画面枠の左上の隅をドラッグし画面を2分割し、Editor TypeをUV Editorにして表示画像を選択します。<br>
workspaceをUV Editingに変更した方が良いかもしれません。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_17.png" width="600"><br><br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_18.png" width="600"><br><br>
右側の枠でモデルを選択した状態でTabキーを押してEditモードに変更し、uキーを押してProject From Viewを選んでカメラプロジェクションのUVマップを生成します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_20.png" width="600"><br><br>

## テクスチャを作成する
右側の枠をTexture Paintに変更します。<br>
workspaceをTexture Paintに変更した方が良いかもしれません。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_21.png" width="600"><br><br>
右側のActive Tool and Workspace settingのModeをSingle Imageに変更します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_22.png" width="600"><br><br>
右側のActive Tool and Workspace settingsのNameを新しいテクスチャを作成し変更します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_24.png" width="600"><br><br>
Context Valueを~カメラプロジェクションの画像の名前~新しく作るテクスチャのUVマップの名前（下の図は間違い）に変更します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_25.png" width="600"><br><br>
Cloneを選択しSource Clone Imageにカメラプロジェクションの画像のときに生成したUVMapを選択します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_26.png" width="600"><br><br>
欲しいモデルの表面をマウスの右ボタンを押しながらポインタでなぞりテクスチャを塗っていきます<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_27.png" width="600"><br><br>
<br>
Model workspaceで別のカメラ指定とUV作成、UV Editing workspaceでUV生成、Texture Paint workspaceでテクスチャ塗りの作業を繰り返します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day24_30.png" width="600"><br><br>
大きく視点変更するとスペキュラの位置が変わらないので違和感が目立ちますが、少なくとも乾ききったイチゴではなくなった気がします。<br>

## まとめ
Capturing RealityのYouTubeに紹介されていたカメラプロジェクションの作業を再現検証しました。<br>
本来は表面にマテリアルを割り当てる作業をした方がよさそうですが、限定的に表面の質感を回復させることができそうです。<br>
