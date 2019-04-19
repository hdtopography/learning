# LEVEL 0 インタフェース、表示、データの保存

## ファイルの読み込み（LAS/LAZ）
* File > Open  
 -もしくはDrag & Drop

![CloudCompare](./pic_level0/1.png)

## Global shift/scale  
* 地理座標系（UTM，平面直角等）の場合、座標値が過大に  
→表示エラーを招く  
	- 読み込み時にオフセットを設定
	- Suggestedもしくはカスタム値（複数の場合は同じ値を）
	- 保存時には元の座標に自動変換される
* ローカル座標系の場合は"No"

![CloudCompare](./pic_level0/2.png)

![CloudCompare](./pic_level0/3.png)

## インタフェース
![CloudCompare](./pic_level0/6+.png)

## ファイル形式
* 点群データ
	 - ASC/PTS, LAS/LAZ, E57, PTX, PCD, Faro, DP, Riegl, etc.

* 三角メッシュ
	- PLY, OBJ, STL, OFF, FBX * 専用フォーマット: BIN
	- 作業状況の保存（”プロジェクト”として）

* 参考：その他のフォーマット
	- SfM (Bundler .OUT,Photoscan .psx(future))
	- CAO (Autocad DXF, Aveva PDMS)
	- GIS (Shapefile SHP)
	- Polylines (SALOME hydro, SinusX, etc.)

## 点群の表示方法
![CloudCompare](./pic_level0/7+.png)

## ラベルの表示
![CloudCompare](./pic_level0/4.png)

## 複数の3Dビュー
* 3D View > New
* Properties > Current Display > (select)

![CloudCompare](./pic_level0/5.png)

## 視点の保持
* Display > Save viewpoint as object

![CloudCompare](./pic_level0/6.png)

## 表示画面の保存（高解像度可）
- Display > Render to file
- 解像度調整  
	-Zoom: 2x, 3x, ...

![CloudCompare](./pic_level0/7.png)

## プロジェクトの保存
★ ひとつのフォルダにまとめる  
- 専用フォーマット”BIN”での保存
	- File > Save ← 保存したいフォルダを選択 - ".bin"形式
	- ”プロジェクト”として作業状況の保存
	- 複数のエンティティ（点群、視点等）を保持可能

![CloudCompare](./pic_level0/8.png)
