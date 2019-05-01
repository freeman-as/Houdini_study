# 004_fracture_replace

プロジェクトの説明

------

## メモ

- 複数の **`DOP Network`** が存在する場合は、タイムラインで選択して切り替えることができる

- Houdini 17でvoronoi fructure SOPが変更されてるので注意

  ```bash
  // 以前のバージョンのvoronoifracture SOPを追加できる
  cd /obj/geo1
  opadd -e voronoifracture
  ```

  where is Cluster tab in Vorooni Fracture sop ?

  https://www.sidefx.com/forum/topic/59435/
  http://www.tokeru.com/cgwiki/?title=Houdini#Voronoi_cluster_and_fracture

- 



------

## 使用したノード (抜粋)

- **``Suvdivide (SOP)``**
  ポリゴンを細分化し滑らかにする
- **``Transform Pieces (SOP)``**
  破片を置換できる
- **``Time Shift (SOP)``**
  指定した時間の状態にできる
- **``Sort (SOP)``**
  ポイントやプリミティブ番号の順番を変更できる
- **``Rest Position (SOP)``**
  シュミレーション前の初期位置を記録する
- **``Dop Import(SOP)``**
  シュミレーション結果を読み込む
- 