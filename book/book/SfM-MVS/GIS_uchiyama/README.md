# SfM多視点ステレオ写真測量による地形モデリングの基礎  
## 内山庄一郎（防災科学技術研究所）・早川裕弌（東京大学CSIS）
---

![img](./top.png)

この資料は、2017年地理情報システム学会第26会学術研究発表大会ハンズオンセッション（2017年10月29日開催）の[配布資料](http://topography.csis.u-tokyo.ac.jp/resources/171029_gisa_sfm/SfM-MVS_photogrammetry_basic_v2.pdf)を基に作成しました。

　SfM（Structure from motion）多視点ステレオ写真測量技術による解析により、撮影対象物の立体モデルが作成される。地表面を撮影した写真を用いた場合、地表面の立体モデルが作成される。フィールドで取得した対空標識の位置座標を立体モデルに与えることにより、地理座標を持った地表面三次元モデルとなる。地図成果であるオルソモザイク画像は、この地表面三次元モデルを上から正射投影した画像であり、DSM（Digital surface model; 地表面数値標高モデル）は三次元モデルを一定間隔のメッシュで分割し、メッシュ内の標高に相当する値が格納されたデータである。これらの情報をGeoTiffファイル等の地理空間情報として出力することにより、最終的な地図成果が得られる。  
　なお、本稿では、一部に古いバージョンの図や説明があります。

## 目次  
---
### 1. [写真測量の基礎](./1.summary/1.summary.md#写真測量の特徴レーザー測量との対比)
### 2. [基幹技術](./2.technique/2.technique.md#2-基幹技術)
### 3. [写真測量のソース（写真画像）](./3.source/3.source.md#3-写真測量のソース写真画像)
### 4. [ハードウェア](./4.hardware/4.hardware.md#4ハードウェア)
### 5. [PhotoScan初期設定](./5.setting/5.setting.md#5-photoscan初期設定)
### 6. [Lens（レンズ歪み補正ソフトウェア）](./6.lens/6.lens.md#6lensレンズ歪み補正ソフトウェア)
### 7. [Workflow: Align Photos](./7.align_photo/7.align_photo.md#7-workflow-align-photos#8a-workflow-build-dense-cloud)
### 8. [Workflow: Build Dense cloud, およびBuild Mesh](./8.build_dense_cloud/8.build_dense_cloud.md#9-workflow-build-texture)
### 9. [Workflow: Build Texture](./9.build_texture/9.build_texture.md#9-workflow-build-texture)
### 10. [Mask処理](./10.mask/10.mask.md#10mask処理)
### 11. [複数Chunk処理](./11.chunk/11.chunk.md#11-複数chunk処理)
---
#### [参考資料・適用事例集](./appendix/appendix.md#参考1uav-sfmによる地図作成技術の概要)

---

[Topへ戻る](https://github.com/hdtopography/learning)
