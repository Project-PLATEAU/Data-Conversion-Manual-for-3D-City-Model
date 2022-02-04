# 3D都市モデルのデータ変換マニュアル
# 概要
* FME Desktopによる3D都市モデル（CityGML形式）からFBX/OBJ/Datasmith/IFC形式への変換を行うワークスペースのサンプルです。
* 本ソフトウェアは、国土交通省の[Project PLATEAU](https://www.mlit.go.jp/plateau/)で利用したものです。

**ただし、i-UR1.4は2021年9月にi-UR1.5に改定されました。これに伴い、URLが変更されました。**  
そのため、本ソフトウェアの利用にあたり、3D都市モデル（CityGML形式）及びソフトウェアに記述された旧URLを新しいURLに更新する必要があります。具体的には以下の手順に従い、更新してください。

### 手順1．3D都市モデル（CityGML形式）に記述されたURLの更新

3D都市モデルのファイル内の名前空間とschemaLocationに記載されている旧URLを、新しいURLに更新（テキスト置換）してください。

対象となる記述を下表に示します。

- 名前空間

|旧URL（i-UR1.4のURL）|新しいURL（i-UR1.5のURL）|
| - | - |
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/uro/1.4`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/uro/1.5|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/urf/1.4`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/urf/1.5|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/urg/1.4`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/urg/1.5|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/urt/1.4`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/urt/1.5|
- schemaLocation

|旧URL（i-UR1.4のURL）|新しいURL（i-UR1.5のURL）|
| - | - |
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/uro/1.4/urbanObject.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/uro/1.5/urbanObject.xsd|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/urf/1.4/urbanFunction.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/uro/1.5/urbanFunction.xsd|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.4/statisticalGrid.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.5/statisticalGrid.xsd|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.4/publicTransit.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.5/publicTransit.xsd|

### 手順2．ソフトウェアに記述されたURL及びバージョンの更新

FME Workbenchspaceにおいて本スクリプトを実行する際、Transportation Parameter ValuesでAdditional ADE Schema File(s)をURLで指定している場合は、新しいschemaLocationのURLを指定する必要があります。

（指定していない場合は、変更の必要はありません）

- schemaLocation

|旧URL（i-UR1.4のURL）|新しいURL（i-UR1.5のURL）|
| - | - |
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/uro/1.4/urbanObject.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/uro/1.5/urbanObject.xsd|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/urf/1.4/urbanFunction.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/uro/1.5/urbanFunction.xsd|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.4/statisticalGrid.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.5/statisticalGrid.xsd|
|`http://www.kantei.go.jp/jp/singi/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.4/publicTransit.xsd`|https://www.chisou.go.jp/tiiki/toshisaisei/itoshisaisei/iur/schemas/urg/1.5/publicTransit.xsd|

## 前提ソフトウェア

* 前提ソフトウェア
* 商用ソフトウェア：[FME Desktop](https://www.safe.com/fme/fme-desktop/)

### 利用方法
詳細は「3D都市モデル導入のためのガイドブック No.7　3D都市モデルのデータ変換マニュアル」を参照ください。
* 上記の前提ソフトウェアをインストールします。
* 本レポジトリの一式をダウンロードし、任意のディレクトリに置きます。
* FME Workbenchで本ファイルを開いて実行
* 変換元の3D都市モデルデータ(CityGML形式)の読み込み
* 変換確認 ”Run” と保存

## License
* 本ソフトウェアは[Apache-2.0 Licence](ttps://github.com/Project-PLATEAU/CityGML-geometry-validator/blob/main/LICENSE)を適用します。

### 注意事項
* 本レポジトリは参考資料として提供しているものです。動作保証は行っておりません。
* 予告なく変更・削除する可能性があります。
* 本レポジトリの利用により生じた損失及び損害等について、国土交通省及び著作権者はいかなる責任も負わないものとします。
