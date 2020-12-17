# 動画を使ってキャプチャーする
動画データから指定の時間間隔で静止画を取り出しキャプチャーする機能があります。<br>
今回はUSBで給電する回転台に小物を載せてスマホカメラで撮影した動画を使ってキャプチャーしてみました。<br>

## 動画の撮影
使用した回転台は約10秒間で1回転していました。<br>
Galaxy Note 9で4K60pで撮影しました。<br>
撮影しているピッチ角度を変更する前後で一時停止し、キャプチャーに不要なframeが撮影されないようにしました。<br>
回転台の上に特徴点が表れやすい紙を貼り、背景は特徴点が表れにくい幕を張りました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day18_1.png" width="600"><br><br>
<br>
動画ファイルは1分間で約500MBになりました。<br>
<br>
## Reality Captureに取り込む 
動画ファイルをReality Capture画面にドラッグアンドドロップし、フレーム切り出しの時間間隔を設定します。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day18_2.png" width="300"><br><br>
この機能ができる前はffmpegなどで動画を静止画連番に変換していました。<br>
<br>
この後は通常の手順と同じです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day18_3.png" width="600"><br><br>
<br>
## AlignmentのInspect
画像の撮影状況を解析することができます。<br>
AlignmentタブのAnalyzeにあるInspectをクリックし3DViewの枠をアクティブにしてInspection TargetをCamera Relationにすると、相互接続したカメラの間が線でつながります。<br>
この結果を見ると、もう少しピッチ方向は細かく撮影した方がよかったようです。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day18_4.png" width="600"><br><br>
Inspection TargetをScene structure uncertainityにすると、タイポイントの位置精度と計算位置の不確実性が表示されます。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day18_5.png" width="600"><br><br>
Helpでinspenctを調べると、図の見方とガイダンスが表示されるので、参考になりました。<br>

## まとめ
動画を使ったキャプチャー方法と撮影状況の解析方法を紹介しました。<br>
動画だと圧縮の影響など画像が劣化する要因が多いのでうまくいかないと思っていましたが、意外とうまく復元できました。<br>
<img src="https://github.com/nakanomuramoto/AdventCalendar2020MJ/blob/main/images/Day18_6.png" width="600"><br><br>
ブラーやフォーカルプレーン現象が起きないようにゆっくり移動して撮影すると便利そうです。<br>
<br>
