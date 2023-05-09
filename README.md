# tokei-vt
都市計画区域、用途市域等のベクトルタイル。  
[unvt/nanban(国連ベクトルタイルツールキットのDockerコンテナ)](https://github.com/unvt/nanban)を利用して作業。 

### サンプル  
調整区域関して誤りがあるため修正中…

### 元データ  
[国土数値情報都市地域データ](https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-A09.html)  
[国土数値情報用地地域データ](https://nlftp.mlit.go.jp/ksj/gml/datalist/KsjTmplt-A29-v2_1.html)  

都市地域データから市街化区域、市街化調整区域、その他用途を抽出。  
それに応じて属性のコード番号をテキストに置換。

用途地域データから市区町村、用途地域、建ぺい率、容積率の属性のみ残し残りは削除。

### 変換  
- QGIS  
データの変換結合と属性の編集に使用  

- Tippecanoe  
--no-tile-compression --no-feature-limit --no-tile-size-limit(pbf) 

### スタイル
- charites  
[地理院地図Vector（仮称）提供実験](https://github.com/gsi-cyberjapan/gsimaps-vector-experiment)をソースとし、[Mapbox GL JSで地理院地図Vector風の地図を表示するサンプル](https://github.com/gsi-cyberjapan/gsivectortile-mapbox-gl-js)の淡色地図(pale.json)をcharitesでコンバート、本ベクトルタイルのスタイルを差し込みの上ビルド。


### 目次  
#### 栃木県
url:https://magn01ia.github.io/tokei-vt/zxy/{z}/{x}/{y}.pbf  
style:https://magn01ia.github.io/tokei-vt/zxy/style.json
- 都市地域(平成30年)  
zoom:8-14  
- 用途地域(令和元年)  
zoom:8-14  
※非線引区域のデータが抜けているの要修正
