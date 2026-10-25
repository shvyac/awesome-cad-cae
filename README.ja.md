# awesome-cad-cae（日本語）

[English README](README.md)

機械設計・シミュレーション・EDA・フォーマット・オープンソースツールチェーンなど、CAD / CAE に役立つリソース集。エンジニアとメイカー向け。⭐ バッジは GitHub のスター数をリアルタイム表示します(shields.io)。release バッジは GitHub の最新リリース日(YYYY/MM/DD、最終更新時点)を示します。

## 目次

- [CAD アプリケーション](#cad-アプリケーション)
- [CAD カーネルとスクリプト](#cad-カーネルとスクリプト)
- [フォーマットと交換](#フォーマットと交換)
- [EDA](#eda)
- [メッシュと可視化](#メッシュと可視化)
- [CAE / FEA](#cae--fea)
- [商用ソルバのスクリプトと入出力](#商用ソルバのスクリプトと入出力)
- [CFD](#cfd)
- [トポロジー最適化](#トポロジー最適化)
- [最適化と実験計画法（DOE）](#最適化と実験計画法doe)
- [MBD](#mbd)
- [試験と解析の相関（TAC）](#試験と解析の相関tac)
- [エディタとシンタックスハイライト](#エディタとシンタックスハイライト)
- [学習と規格](#学習と規格)
- [関連リスト](#関連リスト)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

---

## CAD アプリケーション

2D/3D 機械設計、パラメトリックモデリング、スクリプト向けのデスクトップ／Web CAD。

### FreeCAD
パラメトリック 3D CAD/CAE — Part Design、TechDraw、Assembly、FEM（CalculiX）、CAM（旧 Path）、豊富なワークベンチ群。OCCT 経由で STEP/IGES に強い。バージョン 1.1（2026 年 3 月）で透過プレビュー、フィレット／面取りの対話型ドラッガー、新しい CAM ツールライブラリを追加。

- https://www.freecad.org/
- https://blog.freecad.org/2026/03/25/freecad-version-1-1-released/ — 1.1 リリースノート
- https://github.com/FreeCAD/FreeCAD ![GitHub stars](https://img.shields.io/github/stars/FreeCAD/FreeCAD?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F28-blue?style=flat)
- https://wiki.freecad.org/

### SolveSpace
拘束ソルバ付きの軽量パラメトリック 2D/3D CAD。STEP/STL を出力。機構や簡易部品向き。

- https://solvespace.com/
- https://github.com/solvespace/solvespace ![GitHub stars](https://img.shields.io/github/stars/solvespace/solvespace?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F21-blue?style=flat)

### Dune 3D
Horizon EDA 作者によるパラメトリック 3D CAD — SolveSpace の拘束ソルバ＋OCCT カーネル、STEP 入出力。基板周りの筐体や部品の設計に便利。

- https://dune3d.org/
- https://github.com/dune3d/dune3d ![GitHub stars](https://img.shields.io/github/stars/dune3d/dune3d?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F01%2F28-blue?style=flat)

### OpenSCAD / ImplicitCAD / OpenJSCAD
コードファーストのソリッドモデリング（CSG）。OpenSCAD が広く使われる基準線。ImplicitCAD と OpenJSCAD は関数型／JS の代替。

- https://openscad.org/ — https://github.com/openscad/openscad ![GitHub stars](https://img.shields.io/github/stars/openscad/openscad?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2021%2F02%2F07-blue?style=flat)
- https://implicitcad.org/ — https://github.com/Haskell-Things/ImplicitCAD ![GitHub stars](https://img.shields.io/github/stars/Haskell-Things/ImplicitCAD?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F12%2F18-blue?style=flat)
- https://openjscad.xyz/ — https://github.com/jscad/OpenJSCAD.org ![GitHub stars](https://img.shields.io/github/stars/jscad/OpenJSCAD.org?style=flat&label=%E2%AD%90)

### LibreCAD / QCAD
DXF 製図に特化した 2D CAD。

- https://librecad.org/ — https://github.com/LibreCAD/LibreCAD ![GitHub stars](https://img.shields.io/github/stars/LibreCAD/LibreCAD?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F17-blue?style=flat)
- https://qcad.org/en/ — https://github.com/qcad/qcad ![GitHub stars](https://img.shields.io/github/stars/qcad/qcad?style=flat&label=%E2%AD%90)

### OpenCAD Studio
DWG/DXF のネイティブ読み書きと GPU 加速描画を備えた Rust 製 2D/3D CAD。急成長中の AutoCAD 風オープンソース製図アプリ。

- https://github.com/HakanSeven12/OpenCADStudio ![GitHub stars](https://img.shields.io/github/stars/HakanSeven12/OpenCADStudio?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F25-blue?style=flat)

### BRL-CAD
対話型 3D エディタとレイトレーサを備えたクロスプラットフォームの組み合わせソリッドモデリング。軍事／工学 CAD での長い歴史。

- https://brlcad.org/
- https://github.com/BRL-CAD/brlcad ![GitHub stars](https://img.shields.io/github/stars/BRL-CAD/brlcad?style=flat&label=%E2%AD%90)

### LeoCAD / CAD Sketcher / jsketcher / Fornjot / OpenDraft
ニッチ／実験的 CAD：LEGO CAD、Blender 拘束スケッチャ、ブラウザ CAD、Rust B-Rep カーネル実験（Fornjot — プロジェクト終了、リポジトリはアーカイブ済み）、Rust 製 2D CAD（OpenDraft）。

- https://www.leocad.org/ — https://github.com/leozide/leocad ![GitHub stars](https://img.shields.io/github/stars/leozide/leocad?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F20-blue?style=flat)
- https://www.cadsketcher.com/ — https://github.com/hlorus/CAD_Sketcher ![GitHub stars](https://img.shields.io/github/stars/hlorus/CAD_Sketcher?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F28-blue?style=flat)
- https://web-cad.org/ — https://github.com/xibyte/jsketcher ![GitHub stars](https://img.shields.io/github/stars/xibyte/jsketcher?style=flat&label=%E2%AD%90)
- https://www.fornjot.app/ — https://github.com/hannobraun/fornjot ![GitHub stars](https://img.shields.io/github/stars/hannobraun/fornjot?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F03%2F21-blue?style=flat)（アーカイブ済み）
- https://github.com/JamesHodgkins/OpenDraft ![GitHub stars](https://img.shields.io/github/stars/JamesHodgkins/OpenDraft?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F25-blue?style=flat)

### CodeToCAD
単一の API 面から CAD/FEA ツールを駆動することを目指す Python スクリプトフレームワーク。

- https://github.com/CodeToCAD/CodeToCAD ![GitHub stars](https://img.shields.io/github/stars/CodeToCAD/CodeToCAD?style=flat&label=%E2%AD%90)

### Zoo Design Studio（KCL）
KCL モデリング言語と GPU 加速クラウド幾何エンジンを使う、コード＋GUI の機械 CAD。ML による Text-to-CAD 支援付き。アプリはオープンソース、幾何エンジンはプロプライエタリ。

- https://zoo.dev/
- https://zoo.dev/docs/kcl
- https://github.com/KittyCAD/modeling-app ![GitHub stars](https://img.shields.io/github/stars/KittyCAD/modeling-app?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F21-blue?style=flat)

### CADAM
Adam（YC W25）によるオープンソースの Text-to-CAD Web アプリ。自然言語で部品を記述するとパラメトリックな OpenSCAD モデルを生成し、ブラウザ（WASM）上でスライダー調整・STL/SCAD 出力が可能。

- https://adam.new/opensource
- https://github.com/Adam-CAD/CADAM ![GitHub stars](https://img.shields.io/github/stars/Adam-CAD/CADAM?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F17-blue?style=flat)

### 商用 CAD（参考）
広く使われる商用 MCAD。相互運用の文脈（STEP 交換、学習資料）に有用。

- https://www.autodesk.com/products/fusion-360 — Autodesk Fusion（EAGLE 後継のエレクトロニクス機能を含む）
- https://www.solidworks.com/ — SOLIDWORKS
- https://www.onshape.com/ — Onshape（ブラウザネイティブ）
- https://www.ptc.com/en/products/creo — Creo
- https://www.siemens.com/global/en/products/software/nx.html — Siemens NX

---

## CAD カーネルとスクリプト

FreeCAD、CadQuery、多くの CAE プリプロセッサの下で使われる幾何カーネルと、Python／スクリプト可能なモデリング層。

### Open CASCADE Technology (OCCT)
オープンソースの B-Rep カーネル：ソリッド／サーフェス、ブーリアン、フィレット、STEP/IGES/BREP 交換、可視化。FreeCAD、CadQuery、build123d、PrePoMax の CAD 取り込みを支える。

- https://dev.opencascade.org/
- https://occt3d.com/
- https://github.com/Open-Cascade-SAS/OCCT ![GitHub stars](https://img.shields.io/github/stars/Open-Cascade-SAS/OCCT?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F30-blue?style=flat)

### CadQuery
OCCT 上の Python パラメトリック CAD — 流暢な API、STEP/STL/AMF/3MF 出力、ヘッドレス向け CQGI。

- https://cadquery.readthedocs.io/
- https://github.com/CadQuery/cadquery ![GitHub stars](https://img.shields.io/github/stars/CadQuery/cadquery?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F20-blue?style=flat)

### build123d
コンテキストマネージャ（`with`）API を持つ OCCT 上の Python BREP モデリング。CadQuery の進化系と評されることが多い。

- https://build123d.readthedocs.io/
- https://github.com/gumyr/build123d ![GitHub stars](https://img.shields.io/github/stars/gumyr/build123d?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F21-blue?style=flat)

### pythonocc / OCP
OCCT への Python バインディング（CadQuery／build123d が使うのは OCP）。

- https://github.com/tpaviot/pythonocc-core ![GitHub stars](https://img.shields.io/github/stars/tpaviot/pythonocc-core?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F14-blue?style=flat)
- https://github.com/CadQuery/OCP ![GitHub stars](https://img.shields.io/github/stars/CadQuery/OCP?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F24-blue?style=flat)

### Manifold
メッシュ（三角形）ベースのロバストな幾何ライブラリ。高速・確実なブーリアン演算で、OpenSCAD の Manifold バックエンドや Blender の Manifold ブーリアンソルバで採用。C++ / Python / JS(WASM) バインディング。

- https://manifoldcad.org/
- https://github.com/elalish/manifold ![GitHub stars](https://img.shields.io/github/stars/elalish/manifold?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F25-blue?style=flat)

### Truck
RICOS（日本）による Rust 製 B-Rep CAD カーネル。NURBS / トポロジー / メッシュ化 / WebGPU 描画をモジュール単位で提供。

- https://github.com/ricosjp/truck ![GitHub stars](https://img.shields.io/github/stars/ricosjp/truck?style=flat&label=%E2%AD%90)

---

## フォーマットと交換

CAD、CAM、CAE ツール間の耐久性のある交換フォーマット。

### STEP (ISO 10303)
産業用 3D CAD 交換の主流（AP203 / AP214 / AP242）。FEA/CFD 準備で編集可能な B-Rep が必要なときは STL より STEP を優先。

- https://www.iso.org/standard/84667.html — ISO 10303 overview / AP242 family
- https://www.cax-if.org/ — CAX Interoperability Forum (recommended practices)
- https://dev.opencascade.org/doc/overview/html/occt_user_guides__step.html — OCCT STEP guide

### IGES
レガシーなサーフェス／ワイヤーフレーム交換（古いパイプラインではまだ一般的）。新規作業では可能な限り STEP を優先。

- https://www.nist.gov/publications/initial-graphics-exchange-specification-iges-version-50 — NIST IGES 5.0 reference

### メッシュ／可視化フォーマット
- STL / OBJ — テッセレーション幾何（3D 印刷、多くの CFD 壁面）
- glTF / GLB — 現代的な Web／ランタイム 3D
- VTK / VTU — CAE 結果（ParaView）
- DXF / DWG — 2D 製図の交換

### ブラウザで DWG / DXF
- https://github.com/mlightcad/cad-viewer ![GitHub stars](https://img.shields.io/github/stars/mlightcad/cad-viewer?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F23-blue?style=flat) — バックエンド不要、ブラウザだけで動く DXF/DWG ビューア／エディタ（Three.js/WebGL）

### UFF / MDF（試験 ↔ CAE）
- UFF Dataset 58/55 — モード／FRF 交換（TAC の pyUFF を参照）
- ASAM MDF/MF4 — 計測ログ（TAC の asammdf を参照）

---

## EDA

電子設計自動化 — 回路図、PCB レイアウト、関連ツール。

### KiCad
主要のフリー／オープンソース EDA スイート：回路図、PCB、3D ビューア、大きなライブラリ生態系。KiCad 10（2026 年 3 月）でデザインバリアントと高速配線の等長調整が強化。

- https://www.kicad.org/
- https://github.com/KiCad
- https://www.kicad.org/blog/2026/03/Version-10.0.0-Released/ — KiCad 10 リリースノート

### LibrePCB / Horizon EDA
ライブラリワークフローを統合した現代的なオープンソース PCB 設計。

- https://librepcb.org/ — https://github.com/LibrePCB/LibrePCB ![GitHub stars](https://img.shields.io/github/stars/LibrePCB/LibrePCB?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F12-blue?style=flat)
- https://horizon-eda.org/ — https://github.com/horizon-eda/horizon ![GitHub stars](https://img.shields.io/github/stars/horizon-eda/horizon?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F12%2F05-blue?style=flat)

### atopile
コードで回路基板を設計する言語＋ツールチェーン（`.ato`）。モジュール再利用、制約による部品選定、バージョン管理を前提とし、KiCad へレイアウトを出力。

- https://atopile.io/
- https://github.com/atopile/atopile ![GitHub stars](https://img.shields.io/github/stars/atopile/atopile?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F01%2F20-blue?style=flat)

### Fritzing
ブレッドボードビュー付きのメイカー向け EDA。試作や簡易基板製作に向く。

- https://fritzing.org/
- https://github.com/fritzing/fritzing-app ![GitHub stars](https://img.shields.io/github/stars/fritzing/fritzing-app?style=flat&label=%E2%AD%90)

### DesignSpark PCB / DipTrace
無料またはフリーミアムの Windows 向け PCB ツール。

- https://www.rs-online.com/designspark/pcb-software
- https://diptrace.com/

### Autodesk Fusion Electronics（EAGLE 後継）
Autodesk EAGLE のアクセスは 2026-06-07 に終了済み。Fusion Electronics（EAGLE の設計／ライブラリをインポート可能）または KiCad へ移行。

- https://www.autodesk.com/products/fusion-360/blog/eagle-to-autodesk-fusion-transition/
- https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Autodesk-EAGLE-Announcement-Next-steps-and-FAQ.html

### Japan / 日本語向け PCB ツール

#### CADLUS PCB
プロ向け設定・部品ライブラリ・DXF 入力・アシスト機能を備えた基板設計 CAD。

- http://shop.cadlus.com/html/newpage.html?code=1

#### プリント基板エディタ PCBE
版下印刷 / ガーバー作成向けパターンエディタ。

- https://www.vector.co.jp/soft/winnt/business/se056371.html

#### Minimal Board Editor
軽量な基板エディタ。

- https://www.suigyodo.com/online/mbe/mbe.htm

### レガシー EDA（歴史的）
アーカイブ参照として残す古いフリーウェア。新規プロジェクトでは KiCad / LibrePCB / Horizon を優先。

- http://www.freepcb.com/ — FreePCB（開発はほぼ停止）
- http://pcb.geda-project.org/ — gEDA PCB（歴史的な Unix PCB エディタ系統）

---

## メッシュと可視化

FEA/CFD 向けの形状メッシングと結果のポスト処理。

### Gmsh
組み込み CAD（OCCT 任意）とポストプロセッサを持つオープンソース 3D FE メッシュ生成器。スクリプト可能な `.geo` ワークフローと STEP 取り込み。

- https://gmsh.info/
- https://gitlab.onelab.info/gmsh/gmsh

### Netgen / NGSolve
自動四面体メッシング（PrePoMax 内部でも使用）と NGSolve FEM プラットフォーム。

- https://ngsolve.org/
- https://github.com/NGSolve/netgen ![GitHub stars](https://img.shields.io/github/stars/NGSolve/netgen?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F04%2F30-blue?style=flat)

### SALOME
オープンソースのプリ／ポストプラットフォーム：CAD、メッシング（ヘキサ含む）、Code_Aster 他ソルバとの連携。

- https://www.salome-platform.org/

### ParaView
VTK／OpenFOAM／FEA 結果向けの事実上標準のオープンソース科学可視化。Python スクリプトと大規模データパイプライン。現行リリース系列は 6.1.x。

- https://www.paraview.org/
- https://www.kitware.com/paraview-6-1-0-release-notes/ — 6.1 リリースノート
- https://github.com/Kitware/ParaView ![GitHub stars](https://img.shields.io/github/stars/Kitware/ParaView?style=flat&label=%E2%AD%90)

### VTK
ParaView や多くの CAE ビューアの基盤となる Visualization Toolkit。

- https://vtk.org/
- https://github.com/Kitware/VTK ![GitHub stars](https://img.shields.io/github/stars/Kitware/VTK?style=flat&label=%E2%AD%90)

### PyVista / pygmsh / meshzoo
VTK と Gmsh の Python 層：3D プロットとメッシュ解析を簡潔に行う PyVista、Python から Gmsh を操作する pygmsh、標準的な領域向けの簡易メッシュ集 meshzoo。

- https://github.com/pyvista/pyvista ![GitHub stars](https://img.shields.io/github/stars/pyvista/pyvista?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F11-blue?style=flat)
- https://github.com/nschloe/pygmsh ![GitHub stars](https://img.shields.io/github/stars/nschloe/pygmsh?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F01%2F28-blue?style=flat)
- https://github.com/meshpro/meshzoo ![GitHub stars](https://img.shields.io/github/stars/meshpro/meshzoo?style=flat&label=%E2%AD%90)

### meshio
Gmsh、VTK/VTU、Abaqus、Nastran、Exodus、XDMF など多数のメッシュ形式を読み書きする Python ライブラリと CLI（`meshio convert`）。

- https://github.com/nschloe/meshio ![GitHub stars](https://img.shields.io/github/stars/nschloe/meshio?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F01%2F31-blue?style=flat)

### MeshPy / PyMesh / smesh
Python 向けの三角形／四面体メッシュ生成（MeshPy）、ジオメトリ処理ライブラリ（PyMesh）、OpenCascade ベースのメッシュフレームワーク（smesh）。

- https://mathema.tician.de/software/meshpy
- http://pymesh.readthedocs.io/en/latest
- https://github.com/tpaviot/smesh ![GitHub stars](https://img.shields.io/github/stars/tpaviot/smesh?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2018%2F02%2F16-blue?style=flat)

### Robust-Hexahedral-Re-Meshing / gridder
ヘキサ再メッシュ向けの構造単純化；ロスアラモス国立研究所による、2D/3D 直交格子を作る簡易の対話型グリッド生成ツール。

- https://github.com/gaoxifeng/Robust-Hexahedral-Re-Meshing ![GitHub stars](https://img.shields.io/github/stars/gaoxifeng/Robust-Hexahedral-Re-Meshing?style=flat&label=%E2%AD%90)
- https://github.com/lanl/gridder ![GitHub stars](https://img.shields.io/github/stars/lanl/gridder?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2018%2F02%2F27-blue?style=flat)

### IsoSurfaceExtraction / glue
規則ボクセル格子からの等値面抽出；複数ファイルにまたがる科学データセットの可視化を連携。

- https://github.com/mkazhdan/IsoSurfaceExtraction ![GitHub stars](https://img.shields.io/github/stars/mkazhdan/IsoSurfaceExtraction?style=flat&label=%E2%AD%90)
- https://github.com/glue-viz/glue ![GitHub stars](https://img.shields.io/github/stars/glue-viz/glue?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F22-blue?style=flat)

### SciBlend
科学可視化向け Blender アドオン群。VTK/VTU や OpenFOAM などの CAE 結果を Blender に取り込み、CFD/FEA データをフォトリアルにレンダリング・アニメーション化。

- https://github.com/SciBlend/SciBlend ![GitHub stars](https://img.shields.io/github/stars/SciBlend/SciBlend?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F19-blue?style=flat)

---

## CAE / FEA

有限要素およびマルチフィジックスの構造／熱ソルバとフレームワーク。

### CalculiX + PrePoMax
Abaqus 風のオープンソース 3D 構造 FEM（ccx/cgx）。PrePoMax は現代的な Windows GUI のプリ／ポストプロセッサ（OCCT CAD 取り込み、Netgen/Gmsh メッシング）。

- https://www.dhondt.de/ — CalculiX official
- https://github.com/Dhondtguido/CalculiX ![GitHub stars](https://img.shields.io/github/stars/Dhondtguido/CalculiX?style=flat&label=%E2%AD%90)
- https://github.com/calculix
- https://prepomax.fs.um.si/ — PrePoMax
- https://gitlab.com/MatejB/PrePoMax

### FEniCS / FreeFEM / SfePy
研究やカスタム物理向けに、Python（または DSL）インタフェースが強い PDE/FEM プラットフォーム。

- https://fenicsproject.org/ — https://github.com/FEniCS
- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources ![GitHub stars](https://img.shields.io/github/stars/FreeFem/FreeFem-sources?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F13-blue?style=flat)
- https://sfepy.org/

### deal.II / MFEM / MOOSE / libMesh
大規模 C++ FEM ライブラリ（HPC、適応メッシュ、マルチフィジックス）。

- https://dealii.org/
- https://mfem.org/
- https://mooseframework.inl.gov/
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh ![GitHub stars](https://img.shields.io/github/stars/libMesh/libmesh?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F10%2F06-blue?style=flat)

### Elmer / Code_Aster
オープンなマルチフィジックス FEM（Elmer）と、EDF の産業向け構造力学スイート（Code_Aster）。しばしば SALOME-Meca と併用。

- https://www.elmerfem.org/
- https://code-aster.org/

### FrontISTR / MYSTRAN / XC / Goma
大規模非線形構造向けオープン FEM（FrontISTR）、Nastran 風解析（MYSTRAN）、構造設計（XC）、自由／移動境界の連成輸送（Goma）。

- https://www.frontistr.com/ — https://gitlab.com/FrontISTR-Commons/FrontISTR（主開発。GitHub はミラー）
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN ![GitHub stars](https://img.shields.io/github/stars/dr-bill-c/MYSTRAN?style=flat&label=%E2%AD%90)
- https://github.com/xcfem/xc ![GitHub stars](https://img.shields.io/github/stars/xcfem/xc?style=flat&label=%E2%AD%90)
- https://www.gomafem.com/ — https://github.com/goma/goma ![GitHub stars](https://img.shields.io/github/stars/goma/goma?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F05-blue?style=flat)

### 軽量 Python FEA
教育用および 2D 構造スクリプト。

- https://github.com/anastruct/anaStruct ![GitHub stars](https://img.shields.io/github/stars/anastruct/anaStruct?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F06-blue?style=flat) — 2D structural analysis
- https://github.com/AppliedMechanics-EAFIT/SolidsPy ![GitHub stars](https://img.shields.io/github/stars/AppliedMechanics-EAFIT/SolidsPy?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2020%2F09%2F14-blue?style=flat) — 2D FEM
- https://github.com/CALFEM — CALFEM educational FEM
- https://github.com/JorgeDeLosSantos/nusa ![GitHub stars](https://img.shields.io/github/stars/JorgeDeLosSantos/nusa?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F17-blue?style=flat) — FEM による簡易構造解析

### OpenCourant（旧 OpenRadioss）
衝突・衝撃・落下・爆発向けの陽解法 FEM ソルバ（AGPL-3.0）。Siemens が 2026 年 10 月に OpenRadioss を終了し GitHub リポジトリを削除したため、全コミット履歴を引き継いだコミュニティフォーク。RESF（Rocky Enterprise Software Foundation）傘下。

- https://opencourant.org/
- https://github.com/OpenCourant/OpenCourant ![GitHub stars](https://img.shields.io/github/stars/OpenCourant/OpenCourant?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F11-blue?style=flat)

### Kratos Multiphysics
BSD ライセンスの C++/Python 並列マルチフィジックスフレームワーク（構造、流体、DEM、FSI、接触）。HPC/MPI 対応。

- https://kratosmultiphysics.github.io/Kratos/
- https://github.com/KratosMultiphysics/Kratos ![GitHub stars](https://img.shields.io/github/stars/KratosMultiphysics/Kratos?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F06-blue?style=flat)

### FEATool / WELSIM / FEBio
MATLAB/Octave マルチフィジックスツールボックス（FEATool）、汎用エンジニアリングシミュレーション UI（WELSIM）、生体力学寄りの非線形 FEM（FEBio）。

- https://www.featool.com/ — https://github.com/precise-simulation/featool-multiphysics ![GitHub stars](https://img.shields.io/github/stars/precise-simulation/featool-multiphysics?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F15-blue?style=flat)
- https://welsim.com/ — https://github.com/WelSimLLC/WelSim-Apps ![GitHub stars](https://img.shields.io/github/stars/WelSimLLC/WelSim-Apps?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F16-blue?style=flat)
- https://febio.org/ — https://github.com/febiosoftware/FEBio ![GitHub stars](https://img.shields.io/github/stars/febiosoftware/FEBio?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F04-blue?style=flat)

### JuliaFEM / NASTRAN-95
信頼性・拡張性・分散実行を目指す Julia 製のオープン FEM（JuliaFEM）；NASA が公開した NASTRAN-95 FEM ソルバ（歴史的参考）。

- https://github.com/JuliaFEM/JuliaFEM.jl ![GitHub stars](https://img.shields.io/github/stars/JuliaFEM/JuliaFEM.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2019%2F10%2F14-blue?style=flat)
- https://github.com/nasa/NASTRAN-95 ![GitHub stars](https://img.shields.io/github/stars/nasa/NASTRAN-95?style=flat&label=%E2%AD%90)

### Voxelyze / CFDEMcoupling / Modelica
静的・動的解析向けの多材料ボクセルシミュレーションライブラリ（Voxelyze）；LIGGGHTS と OpenFOAM による CFD-DEM 連成（CFDEMcoupling）；機械／電気／熱／流体／制御の 1D/3D モデル向け Modelica 標準ライブラリ。

- https://github.com/jonhiller/Voxelyze ![GitHub stars](https://img.shields.io/github/stars/jonhiller/Voxelyze?style=flat&label=%E2%AD%90)
- https://github.com/CFDEMproject/CFDEMcoupling-PUBLIC ![GitHub stars](https://img.shields.io/github/stars/CFDEMproject/CFDEMcoupling-PUBLIC?style=flat&label=%E2%AD%90)
- https://github.com/modelica/ModelicaStandardLibrary ![GitHub stars](https://img.shields.io/github/stars/modelica/ModelicaStandardLibrary?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F05%2F23-blue?style=flat)

### PyOP2 / pyamg / OpenBLAS
数値計算の基盤部品：非構造メッシュ上の性能可搬な並列計算（PyOP2）、Python の代数的マルチグリッドソルバ（pyamg）、最適化された BLAS ライブラリ（OpenBLAS）。

- https://github.com/OP2/PyOP2 ![GitHub stars](https://img.shields.io/github/stars/OP2/PyOP2?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F11%2F22-blue?style=flat) — アーカイブ済み
- https://github.com/pyamg/pyamg ![GitHub stars](https://img.shields.io/github/stars/pyamg/pyamg?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F08%2F23-blue?style=flat)
- https://github.com/OpenMathLib/OpenBLAS ![GitHub stars](https://img.shields.io/github/stars/OpenMathLib/OpenBLAS?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F16-blue?style=flat)

---

## 商用ソルバのスクリプトと入出力

商用ソルバ（Nastran、Abaqus、LS-DYNA、ANSA）の入力／結果ファイルを読み書き・変換・自動化するライブラリとスクリプト。

### Nastran
BDF/OP2/OP4 ファイルのインタフェースライブラリ（pyNastran）；Nastran 入力デックのブラウザ（nastran-find）。

- https://github.com/SteveDoyle2/pyNastran ![GitHub stars](https://img.shields.io/github/stars/SteveDoyle2/pyNastran?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F03%2F26-blue?style=flat)
- https://github.com/setvisible/nastran-find ![GitHub stars](https://img.shields.io/github/stars/setvisible/nastran-find?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2017%2F01%2F01-blue?style=flat)

### Abaqus
Python から Abaqus のシミュレーションを構築・後処理・プロット（abapy）；入力ファイルのパーサ（AbqParse）；Abaqus から LS-DYNA キーワードへの変換（abaqus2dyna）；Abaqus/Python スクリプト用の型ヒント（abqpy）；自動化スクリプト（abaqus_scripts）；ODB の後処理（postPro4Abq、PyQus）；ODB から VTK への変換（odb2vtk）；ジョブ状況のプロッタ（jobwatch）；ドキュメントのキーワード抽出（Abaqus-Documentation-Scraper）。

- https://github.com/lcharleux/abapy ![GitHub stars](https://img.shields.io/github/stars/lcharleux/abapy?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2016%2F04%2F27-blue?style=flat)
- https://github.com/crmccreary/AbqParse ![GitHub stars](https://img.shields.io/github/stars/crmccreary/AbqParse?style=flat&label=%E2%AD%90)
- https://github.com/tbhartman/abaqus2dyna ![GitHub stars](https://img.shields.io/github/stars/tbhartman/abaqus2dyna?style=flat&label=%E2%AD%90)
- https://github.com/haiiliin/abqpy ![GitHub stars](https://img.shields.io/github/stars/haiiliin/abqpy?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F20-blue?style=flat)
- https://github.com/rodrigo1392
- https://github.com/mengomarlene/postPro4Abq ![GitHub stars](https://img.shields.io/github/stars/mengomarlene/postPro4Abq?style=flat&label=%E2%AD%90)
- https://github.com/JorgeDeLosSantos/pyqus ![GitHub stars](https://img.shields.io/github/stars/JorgeDeLosSantos/pyqus?style=flat&label=%E2%AD%90)
- https://github.com/Liujie-SYSU/odb2vtk ![GitHub stars](https://img.shields.io/github/stars/Liujie-SYSU/odb2vtk?style=flat&label=%E2%AD%90)
- https://github.com/jakobgager/jobwatch ![GitHub stars](https://img.shields.io/github/stars/jakobgager/jobwatch?style=flat&label=%E2%AD%90)
- https://github.com/bendeaton/Abaqus-Documentation-Scraper ![GitHub stars](https://img.shields.io/github/stars/bendeaton/Abaqus-Documentation-Scraper?style=flat&label=%E2%AD%90)

### LS-DYNA
LS-DYNA のバイナリ結果ファイルを読む Python ライブラリ（qd）；binout と d3plot を高速に読む C/C++/Python ライブラリ（dynareadout）；MATLAB のリーダと実行ラッパ（matlab-lsdyna）。

- https://github.com/qd-cae/qd-cae-python ![GitHub stars](https://img.shields.io/github/stars/qd-cae/qd-cae-python?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2019%2F11%2F12-blue?style=flat) — アーカイブ済み
- https://pypi.org/project/dynareadout/ — PyPI（元の GitHub リポジトリは公開終了）
- https://github.com/svenholcombe/matlab-lsdyna ![GitHub stars](https://img.shields.io/github/stars/svenholcombe/matlab-lsdyna?style=flat&label=%E2%AD%90)

### ANSA / CalculiX
Beta CAE スイートをスクリプト化する Python ユーティリティ（qd-ansa）；Python から CalculiX の FEA モデルを自動構築（pycalculix）。

- https://github.com/qd-cae/qd-ansa-extension ![GitHub stars](https://img.shields.io/github/stars/qd-cae/qd-ansa-extension?style=flat&label=%E2%AD%90)
- https://github.com/spacether/pycalculix ![GitHub stars](https://img.shields.io/github/stars/spacether/pycalculix?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2019%2F11%2F30-blue?style=flat) — アーカイブ済み

### メッシュ変換
有限要素メッシュファイルを複数形式間で変換（FEconv）。

- https://github.com/victorsndvg/FEconv ![GitHub stars](https://img.shields.io/github/stars/victorsndvg/FEconv?style=flat&label=%E2%AD%90)

### Abaqus ユーザーサブルーチン
UMAT / UEL ユーザーサブルーチンの集まりと、Abaqus と Intel Fortran 環境の設定ガイド。

- https://github.com/jgomezc1/ABAQUS-US ![GitHub stars](https://img.shields.io/github/stars/jgomezc1/ABAQUS-US?style=flat&label=%E2%AD%90)
- https://github.com/ALandauer/ABAQUS_Subroutines ![GitHub stars](https://img.shields.io/github/stars/ALandauer/ABAQUS_Subroutines?style=flat&label=%E2%AD%90)
- https://github.com/WeilinDeng/ABAQUS ![GitHub stars](https://img.shields.io/github/stars/WeilinDeng/ABAQUS?style=flat&label=%E2%AD%90)
- https://github.com/song2001/abaqus-fortran-env-setup ![GitHub stars](https://img.shields.io/github/stars/song2001/abaqus-fortran-env-setup?style=flat&label=%E2%AD%90)

---

## CFD

計算流体力学ソルバと関連マルチフィジックスコード。

### OpenFOAM
最も広く使われるオープンソース CFD ツールボックス — 流れ、伝熱、反応、多相。強い生態系（FreeCAD の CfdOF など）。

- https://www.openfoam.com/ — ESI/OpenCFD 版（最新 v2606、2026 年 6 月）
- https://www.openfoam.com/news/main-news/openfoam-v2606 — v2606 リリースノート
- https://github.com/OpenFOAM/OpenFOAM-dev ![GitHub stars](https://img.shields.io/github/stars/OpenFOAM/OpenFOAM-dev?style=flat&label=%E2%AD%90)
- https://openfoam.org/ — community edition lineage

### SU2
マルチフィジックス PDE ソルバと勾配ベースの空力形状最適化。

- https://su2code.github.io/
- https://github.com/su2code/SU2 ![GitHub stars](https://img.shields.io/github/stars/su2code/SU2?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F04%2F27-blue?style=flat)

### Palabos / Lethe / x3d2
格子ボルツマン CFD（Palabos）；高次 CG CFD–DEM（Lethe）；GPU 高次有限差分 CFD（x3d2 / Xcompact3d 系統）。

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://chaos-polymtl.github.io/lethe/ — https://github.com/chaos-polymtl/lethe ![GitHub stars](https://img.shields.io/github/stars/chaos-polymtl/lethe?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F01-blue?style=flat)
- https://xcompact3d.github.io/ — https://github.com/xcompact3d/x3d2 ![GitHub stars](https://img.shields.io/github/stars/xcompact3d/x3d2?style=flat&label=%E2%AD%90)

### Fire Dynamics Simulator (FDS)
NIST の火災駆動流れ CFD。Smokeview 可視化付き。

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds ![GitHub stars](https://img.shields.io/github/stars/firemodels/fds?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F10-blue?style=flat)

### Foam-Agent
OpenFOAM のワークフローをエンドツーエンドで自動化する LLM マルチエージェントフレームワーク。自然言語の記述からメッシュ生成・ケース設定・実行・エラー修正まで行う（CMAME 掲載論文）。

- https://github.com/csml-rpi/Foam-Agent ![GitHub stars](https://img.shields.io/github/stars/csml-rpi/Foam-Agent?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F04%2F01-blue?style=flat)

---

## トポロジー最適化

荷重と拘束のもとでの材料配置最適化。

### OpenLSTO / FEniTop / FreeTO / ToOptiX
レベルセット TO（OpenLSTO）、FEniCSx 並列 TO（FEniTop）、MATLAB 自由形状 3D TO（FreeTO）、Blender/FreeCAD アドオン付きマルチフィジックス TO（ToOptiX）。

- https://github.com/M2DOLab/OpenLSTO ![GitHub stars](https://img.shields.io/github/stars/M2DOLab/OpenLSTO?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2018%2F08%2F25-blue?style=flat)
- https://github.com/missionlab/fenitop ![GitHub stars](https://img.shields.io/github/stars/missionlab/fenitop?style=flat&label=%E2%AD%90)
- https://github.com/ooibhadode/FreeTO ![GitHub stars](https://img.shields.io/github/stars/ooibhadode/FreeTO?style=flat&label=%E2%AD%90)
- https://github.com/Foxelmanian/ToOptix ![GitHub stars](https://img.shields.io/github/stars/Foxelmanian/ToOptix?style=flat&label=%E2%AD%90)

---

## 最適化と実験計画法（DOE）

汎用の最適化、実験計画法、多分野設計フレームワーク。

### OpenMDAO / pyDOE
システム解析と多分野最適化のための高性能 Python プラットフォーム（OpenMDAO）；実験計画法ライブラリ（pyDOE）。

- https://github.com/OpenMDAO/OpenMDAO ![GitHub stars](https://img.shields.io/github/stars/OpenMDAO/OpenMDAO?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F10-blue?style=flat)
- https://github.com/pydoe/pydoe ![GitHub stars](https://img.shields.io/github/stars/pydoe/pydoe?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F21-blue?style=flat)

### CasADi / YALMIP
自動微分を備えた数値最適化のシンボリックフレームワーク（CasADi）；最適化モデリング用の MATLAB ツールボックス（YALMIP）。

- https://github.com/casadi/casadi ![GitHub stars](https://img.shields.io/github/stars/casadi/casadi?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F16-blue?style=flat)
- https://github.com/yalmip/YALMIP ![GitHub stars](https://img.shields.io/github/stars/yalmip/YALMIP?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F06%2F26-blue?style=flat)

---

## MBD

マルチボディダイナミクスとモーションシミュレーション。

### MBDyn / Project Chrono / Simbody / EXUDYN
汎用 MBD（MBDyn）；車両／ロボット／粉体などのマルチフィジックス（Chrono）；関節付き生体力学（Simbody）；Python/C++ 柔軟 MBD（EXUDYN）。

- https://www.mbdyn.org/ — https://public.gitlab.polimi.it/DAER/mbdyn
- https://projectchrono.org/ — https://github.com/projectchrono/chrono ![GitHub stars](https://img.shields.io/github/stars/projectchrono/chrono?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F04%2F07-blue?style=flat)
- https://github.com/simbody/simbody ![GitHub stars](https://img.shields.io/github/stars/simbody/simbody?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F05%2F17-blue?style=flat)
- https://github.com/jgerstmayr/EXUDYN ![GitHub stars](https://img.shields.io/github/stars/jgerstmayr/EXUDYN?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F09-blue?style=flat)

### OpenSim / Pinocchio
筋骨格ダイナミクス（OpenSim）；ロボティクス向け高速剛体ダイナミクス（Pinocchio）。

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio ![GitHub stars](https://img.shields.io/github/stars/stack-of-tasks/pinocchio?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F07-blue?style=flat)

---

## 試験と解析の相関（TAC）

CAE 結果と実機試験を突き合わせるためのツール — 計測データ、実験モード解析、モデル更新。

### 試験・シミュレーションデータ管理

#### asammdf
ASAM MDF/MF4 計測ファイル向けの高速 Python リーダ／ライタ／GUI（自動車／航空宇宙リグ、CAN/LIN）。

- https://github.com/danielhrisca/asammdf ![GitHub stars](https://img.shields.io/github/stars/danielhrisca/asammdf?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F21-blue?style=flat)
- https://asammdf.readthedocs.io/

#### MDSplus
階層的な実験／シミュレーションデータツリー。核融合研究に起源があり、sim と試験の相関に広く使われる。

- https://mdsplus.org/
- https://github.com/MDSplus/mdsplus ![GitHub stars](https://img.shields.io/github/stars/MDSplus/mdsplus?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat)

#### openMDM / odsbox
Eclipse ASAM ODS 計測データ管理（openMDM）；Python ODS REST ラッパ（odsbox）。

- https://openmdm.org/
- https://github.com/peak-solution/odsbox ![GitHub stars](https://img.shields.io/github/stars/peak-solution/odsbox?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F19-blue?style=flat)

#### SciDataTool
sim と試験信号の比較向けに、時間／空間／周波数の統一的な科学フィールド保存／ポスト処理。

- https://github.com/Eomys/SciDataTool ![GitHub stars](https://img.shields.io/github/stars/Eomys/SciDataTool?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F02%2F05-blue?style=flat)

### 実験モード解析（EMA / OMA）

#### pyEMA / sdypy-EMA / pyOMA2 / OpenModal
FRF からのモードパラメータ抽出（LSCF/LSFD）；SDyPy 後継；出力のみ OMA（SSI/FDD）；フル GUI の EMA スイート。

- https://github.com/ladisk/pyEMA ![GitHub stars](https://img.shields.io/github/stars/ladisk/pyEMA?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F29-blue?style=flat)
- https://github.com/sdypy/sdypy-EMA ![GitHub stars](https://img.shields.io/github/stars/sdypy/sdypy-EMA?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F29-blue?style=flat)
- https://github.com/dagghe/pyOMA2 ![GitHub stars](https://img.shields.io/github/stars/dagghe/pyOMA2?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F22-blue?style=flat)
- https://www.openmodal.com/ — https://github.com/openmodal/OpenModal ![GitHub stars](https://img.shields.io/github/stars/openmodal/OpenModal?style=flat&label=%E2%AD%90)

#### pyFRF / pyUFF
時間信号からの FRF 推定器（H1/H2/Hv）；CAT ↔ CAE 交換向け UFF Dataset 58/55/2411/2412 I/O。

- https://github.com/ladisk/pyFRF ![GitHub stars](https://img.shields.io/github/stars/ladisk/pyFRF?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F02-blue?style=flat)
- https://github.com/ladisk/pyuff ![GitHub stars](https://img.shields.io/github/stars/ladisk/pyuff?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F25-blue?style=flat)

### 相関指標とモデル更新

#### SDynPy / SMAC
Sandia 構造ダイナミクス Python（MAC/COMAC、FRF、曲線フィット）；MATLAB モード曲線フィット（SMAC）。

- https://sandialabs.github.io/sdynpy/ — https://github.com/sandialabs/sdynpy ![GitHub stars](https://img.shields.io/github/stars/sandialabs/sdynpy?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F04%2F20-blue?style=flat)
- https://github.com/sandialabs/SMAC ![GitHub stars](https://img.shields.io/github/stars/sandialabs/SMAC?style=flat&label=%E2%AD%90)

#### pyFBS
周波数ベース部分構造合成と伝達経路解析 — 計測 FRF と FEA 部品の結合。

- https://pyfbs.readthedocs.io/
- https://gitlab.com/pyFBS/pyFBS

#### Dakota / PyDynamic
Sandia の最適化／UQ／モデル校正ツールキット；PTB/NPL の動的計測不確かさ伝播。

- https://dakota.sandia.gov/ — https://github.com/snl-dakota/dakota ![GitHub stars](https://img.shields.io/github/stars/snl-dakota/dakota?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F14-blue?style=flat)
- https://pydynamic.readthedocs.io/ — https://github.com/PTBresearch/PyDynamic ![GitHub stars](https://img.shields.io/github/stars/PTBresearch/PyDynamic?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F05%2F31-blue?style=flat)

### ドメイン固有の検証

#### ROSS / OpenFAST / FEBio
計測応答比較付きロータダイナミクス FEM（ROSS）；NLR（旧 NREL）風力タービンの空力・サーボ・弾性検証（OpenFAST）；生体力学 V&V（FEBio）。

- https://ross.readthedocs.io/ — https://github.com/petrobras/ross ![GitHub stars](https://img.shields.io/github/stars/petrobras/ross?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F20-blue?style=flat)
- https://openfast.readthedocs.io/ — https://github.com/OpenFAST/openfast ![GitHub stars](https://img.shields.io/github/stars/OpenFAST/openfast?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F03%2F12-blue?style=flat)
- https://febio.org/ — https://github.com/febiosoftware/FEBio ![GitHub stars](https://img.shields.io/github/stars/febiosoftware/FEBio?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F04-blue?style=flat)

---

## エディタとシンタックスハイライト

ソルバ入力ファイル向けのエディタプラグイン。

### Vim
LS-DYNA、Abaqus、RADIOSS の入力ファイル向けプラグインとレキサ。

- https://github.com/gradzikb/vim-lsdyna ![GitHub stars](https://img.shields.io/github/stars/gradzikb/vim-lsdyna?style=flat&label=%E2%AD%90)
- https://github.com/tbhartman/vim-lexer-lsdyna ![GitHub stars](https://img.shields.io/github/stars/tbhartman/vim-lexer-lsdyna?style=flat&label=%E2%AD%90)
- https://github.com/gradzikb/vim-abaqus ![GitHub stars](https://img.shields.io/github/stars/gradzikb/vim-abaqus?style=flat&label=%E2%AD%90)
- https://github.com/gradzikb/vim-radioss ![GitHub stars](https://img.shields.io/github/stars/gradzikb/vim-radioss?style=flat&label=%E2%AD%90)

### Sublime Text
LS-DYNA と Abaqus のシンタックスハイライト。

- https://github.com/bendeaton/LS-DYNA-Sublime ![GitHub stars](https://img.shields.io/github/stars/bendeaton/LS-DYNA-Sublime?style=flat&label=%E2%AD%90)
- https://github.com/bendeaton/Abaqus-Sublime ![GitHub stars](https://img.shields.io/github/stars/bendeaton/Abaqus-Sublime?style=flat&label=%E2%AD%90)

---

## 学習と規格

入門パスと耐久性のある参照（ランダムなチュートリアルより公式ドキュメントを優先）。

### 推奨オープンソースワークフロー
1. **CAD** — FreeCAD または CadQuery/build123d → **STEP** を出力
2. **Mesh** — Gmsh（または FreeCAD FEM / PrePoMax / SALOME）
3. **FEA** — CalculiX（PrePoMax/FreeCAD）または FEniCSx / Code_Aster
4. **CFD** — OpenFOAM（任意で FreeCAD CfdOF）
5. **Post** — ParaView

### ドキュメントとコミュニティ
- https://wiki.freecad.org/ — FreeCAD documentation
- https://www.dhondt.de/ — CalculiX manuals
- https://www.openfoam.com/documentation/overview — OpenFOAM docs
- https://gmsh.info/doc/texinfo/gmsh.html — Gmsh reference
- https://fenicsproject.org/documentation/ — FEniCS docs
- https://calculix.discourse.group/ — CalculiX community forum

### 規格団体
- https://www.iso.org/committee/54158.html — ISO/TC 184/SC 4（産業データ、STEP）
- https://www.asam.net/ — ASAM（MDF、ODS、関連する試験データ規格）
- https://www.nafems.org/ — NAFEMS（エンジニアリングシミュレーションコミュニティ／ベストプラクティス）

---

## 関連リスト

- https://github.com/shvyac/awesome-meshless-cae ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90) — メッシュレス／メッシュフリー CAE ツール（SPH、MPS、LBM、MPM、ペリダイナミクス、IGA、AI サロゲート）
- https://github.com/qd-cae/awesome-CAE ![GitHub stars](https://img.shields.io/github/stars/qd-cae/awesome-CAE?style=flat&label=%E2%AD%90) — CAE のフレームワーク・ライブラリ・ソフトウェア（Abaqus / Nastran / LS-DYNA のスクリプト）
- https://github.com/mlightcad/awesome-cad ![GitHub stars](https://img.shields.io/github/stars/mlightcad/awesome-cad?style=flat&label=%E2%AD%90) — open-source CAD software & libraries
- https://github.com/kimimgo/awesome-ai-cae ![GitHub stars](https://img.shields.io/github/stars/kimimgo/awesome-ai-cae?style=flat&label=%E2%AD%90) — AI-callable CAE/CAD tooling
- https://awesome.re/ — Awesome manifesto

---

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
