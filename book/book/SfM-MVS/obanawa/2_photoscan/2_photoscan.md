# PhotoScanの基礎

## 1. 画像の取り込み  
Addphotosをクリック

![img](./pic/1.png)

使用する画像を選択、open

## 2. Align Photos
Workflow→Align Photos  

使用する画像を選択、open


![img](./pic/2.png)
Accuracy:Low
Pair preselection:Refrence (画像データに位置情報がついている場合、ない場合はGeneric)
クリックOK
![img](./pic/3.png)

## 3. GCP setting
GCP settingの前にメッシュモデルを作成する。メッシュモデルを作成することにより複数の画像に移っているGCPを一斉に選択することができる。  
Workflow→Build Mesh  
クリックOK
![img](./pic/4.png)

画像データよりGCPをsettingする。
ToolbarのReferenceを表示させる。（Toolbar上で左クリックRefrence選択）
Toolbar上のEdit Markersをクリック。
![img](./pic/5.png)

Refrenceより画像を選択して画像上のGCPを置いた点で 右クリック→Create Markerクリック。

![img](./pic/6.png)

Markersが作られているかRefrenceで確認。
わかりやすい名前にMarkersを変更。

![img](./pic/7.png)

ReferenceよりImportをクリック。
位置情報のテキストファイルをImport。**（ダブルクリックで直接入力もできる、、、。こちらでテキストファイルを用意する場合、Importのほうがミスはないかも？）**

![img](./pic/8.png)

各Markerが正しい点におかれているか確認する。
左クリック→Filter Photos by Markers
Photosのタブで確認、ずれている場合はドラッグして修正。

![img](./pic/9.png)

Settingをクリック。座標系を確認。
今回は日本測地系第９系(JGD2000/Japan Plane Rectangular CS Ⅸ)

![img](./pic/10.png)

RefrenceのタブでCamerasのチェックをすべて外す。Camerasの位置情報を使わない状態にする。

Optimize Camerasをクリック。
クリックＯＫ。

![img](./pic/11.png)

## 4.Build dense cloud
Workflow→Build Dense Cloud

![img](./pic/12.png)

Quality:Low
クリックOK

## 5. Build mesh
Workflow→Build Mesh

![img](./pic/13.png)

Surface type:Height field
Source data:Dense cloud
でクリックOK。

![img](./pic/14.png)

## 6. export to DEM, orthophoto,LAS

orthophotoの精度をあげるためBuild textureを行います。
Workflow→Build Texture

![img](./pic/15.png)

クリックOK。

![img](./pic/16.png)

Chunk 1で右クリックExport→Export Orthophoto→Export JPEG/TIFF/PNGをクリック

![img](./pic/17.png)

座標系等を確認しクリックOK。

![img](./pic/18.png)

名前を設定し、TIFFで保存。
Chunk 1→Export→Export DEM→Export TIFF/BIL/XYZをクリック。

![img](./pic/19.png)


座標系等を確認、Crop invaild DEMにチェックを入れる。
クリックOK。

![img](./pic/20.png)


Geo TIFF Elevation Dataで保存、名前を設定して保存。

Chunk1→Export→Export Points

![img](./pic/21.png)

ファイル名を指定、ファイルの種類をASPRS LAS(.las)で保存。

![img](./pic/22.png)

座標系を指定、Point colorsにチェックを入れる。
クリックOK。

![img](./pic/28.png)
