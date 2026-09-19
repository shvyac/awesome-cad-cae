# awesome-cad-cae（日本語）

[English README](README.md)

機械設計・シミュレーション・EDA・フォーマット・オープンソースツールチェーンなど、CAD / CAE に役立つリソース集。エンジニアとメイカー向け。

## 目次

- [CAD アプリケーション](#cad-アプリケーション)
- [CAD カーネルとスクリプト](#cad-カーネルとスクリプト)
- [フォーマットと交換](#フォーマットと交換)
- [EDA](#eda)
- [メッシュと可視化](#メッシュと可視化)
- [CAE / FEA](#cae--fea)
- [CFD](#cfd)
- [トポロジー最適化](#トポロジー最適化)
- [MBD](#mbd)
- [試験と解析の相関（TAC）](#試験と解析の相関tac)
- [学習と規格](#学習と規格)
- [関連リスト](#関連リスト)

---

## CAD アプリケーション

2D/3D 機械設計、パラメトリックモデリング、スクリプト向けのデスクトップ／Web CAD。

### FreeCAD
パラメトリック 3D CAD/CAE — Part Design、TechDraw、FEM（CalculiX）、Path/CAM、豊富なワークベンチ群。OCCT 経由で STEP/IGES に強い。

- https://www.freecad.org/
- https://github.com/FreeCAD/FreeCAD
- https://wiki.freecad.org/

### SolveSpace
拘束ソルバ付きの軽量パラメトリック 2D/3D CAD。STEP/STL を出力。機構や簡易部品向き。

- https://solvespace.com/
- https://github.com/solvespace/solvespace

### OpenSCAD / ImplicitCAD / OpenJSCAD
コードファーストのソリッドモデリング（CSG）。OpenSCAD が広く使われる基準線。ImplicitCAD と OpenJSCAD は関数型／JS の代替。

- https://openscad.org/ — https://github.com/openscad/openscad
- https://implicitcad.org/ — https://github.com/Haskell-Things/ImplicitCAD
- https://openjscad.xyz/ — https://github.com/jscad/OpenJSCAD.org

### LibreCAD / QCAD
DXF 製図に特化した 2D CAD。

- https://librecad.org/ — https://github.com/LibreCAD/LibreCAD
- https://qcad.org/en/ — https://github.com/qcad/qcad

### BRL-CAD
対話型 3D エディタとレイトレーサを備えたクロスプラットフォームの組み合わせソリッドモデリング。軍事／工学 CAD での長い歴史。

- https://brlcad.org/
- https://github.com/BRL-CAD/brlcad

### LeoCAD / CAD Sketcher / jsketcher / Fornjot / OpenDraft
ニッチ／実験的 CAD：LEGO CAD、Blender 拘束スケッチャ、ブラウザ CAD、Rust CAD 実験、Avalonia 2D CAD。

- https://www.leocad.org/ — https://github.com/leozide/leocad
- https://www.cadsketcher.com/ — https://github.com/hlorus/CAD_Sketcher
- https://web-cad.org/ — https://github.com/xibyte/jsketcher
- https://www.fornjot.app/ — https://github.com/hannobraun/Fornjot
- https://github.com/JamesHodgkins/OpenDraft

### CodeToCAD
単一の API 面から CAD/FEA ツールを駆動することを目指す Python スクリプトフレームワーク。

- https://github.com/CodeToCAD/CodeToCAD

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
- https://github.com/Open-Cascade-SAS/OCCT

### CadQuery
OCCT 上の Python パラメトリック CAD — 流暢な API、STEP/STL/AMF/3MF 出力、ヘッドレス向け CQGI。

- https://cadquery.readthedocs.io/
- https://github.com/CadQuery/cadquery

### build123d
コンテキストマネージャ（`with`）API を持つ OCCT 上の Python BREP モデリング。CadQuery の進化系と評されることが多い。

- https://build123d.readthedocs.io/
- https://github.com/gumyr/build123d

### pythonocc / OCP
OCCT への Python バインディング（CadQuery／build123d が使うのは OCP）。

- https://github.com/tpaviot/pythonocc-core
- https://github.com/CadQuery/OCP

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

### UFF / MDF（試験 ↔ CAE）
- UFF Dataset 58/55 — モード／FRF 交換（TAC の pyUFF を参照）
- ASAM MDF/MF4 — 計測ログ（TAC の asammdf を参照）

---

## EDA

電子設計自動化 — 回路図、PCB レイアウト、関連ツール。

### KiCad
主要のフリー／オープンソース EDA スイート：回路図、PCB、3D ビューア、大きなライブラリ生態系。

- https://www.kicad.org/
- https://github.com/KiCad

### LibrePCB / Horizon EDA
ライブラリワークフローを統合した現代的なオープンソース PCB 設計。

- https://librepcb.org/ — https://github.com/LibrePCB/LibrePCB
- https://horizon-eda.org/ — https://github.com/horizon-eda/horizon

### Fritzing
ブレッドボードビュー付きのメイカー向け EDA。試作や簡易基板製作に向く。

- https://fritzing.org/
- https://github.com/fritzing/fritzing-app

### DesignSpark PCB / DipTrace
無料またはフリーミアムの Windows 向け PCB ツール。

- https://www.rs-online.com/designspark/pcb-software
- https://diptrace.com/

### Autodesk Fusion Electronics（EAGLE 後継）
Autodesk EAGLE のアクセスは 2026-06-07 で終了。Fusion Electronics へ移行（EAGLE の設計／ライブラリをインポート可能）。

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
- https://github.com/NGSolve/netgen

### SALOME
オープンソースのプリ／ポストプラットフォーム：CAD、メッシング（ヘキサ含む）、Code_Aster 他ソルバとの連携。

- https://www.salome-platform.org/

### ParaView
VTK／OpenFOAM／FEA 結果向けの事実上標準のオープンソース科学可視化。Python スクリプトと大規模データパイプライン。

- https://www.paraview.org/
- https://github.com/Kitware/ParaView

### VTK
ParaView や多くの CAE ビューアの基盤となる Visualization Toolkit。

- https://vtk.org/
- https://github.com/Kitware/VTK

---

## CAE / FEA

有限要素およびマルチフィジックスの構造／熱ソルバとフレームワーク。

### CalculiX + PrePoMax
Abaqus 風のオープンソース 3D 構造 FEM（ccx/cgx）。PrePoMax は現代的な Windows GUI のプリ／ポストプロセッサ（OCCT CAD 取り込み、Netgen/Gmsh メッシング）。

- https://www.dhondt.de/ — CalculiX official
- https://github.com/Dhondtguido/CalculiX
- https://github.com/calculix
- https://prepomax.fs.um.si/ — PrePoMax
- https://gitlab.com/MatejB/PrePoMax

### FEniCS / FreeFEM / SfePy
研究やカスタム物理向けに、Python（または DSL）インタフェースが強い PDE/FEM プラットフォーム。

- https://fenicsproject.org/ — https://github.com/FEniCS
- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources
- https://sfepy.org/

### deal.II / MFEM / MOOSE / libMesh
大規模 C++ FEM ライブラリ（HPC、適応メッシュ、マルチフィジックス）。

- https://dealii.org/
- https://mfem.org/
- https://mooseframework.inl.gov/
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh

### Elmer / Code_Aster
オープンなマルチフィジックス FEM（Elmer）と、EDF の産業向け構造力学スイート（Code_Aster）。しばしば SALOME-Meca と併用。

- https://www.elmerfem.org/
- https://code-aster.org/

### FrontISTR / MYSTRAN / XC / Goma
大規模非線形構造向けオープン FEM（FrontISTR）、Nastran 風解析（MYSTRAN）、構造設計（XC）、自由／移動境界の連成輸送（Goma）。

- https://www.frontistr.com/ — https://github.com/FrontISTR/FrontISTR
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN
- https://github.com/xcfem/xc
- https://www.gomafem.com/ — https://github.com/goma/goma

### 軽量 Python FEA
教育用および 2D 構造スクリプト。

- https://github.com/ritchie46/anaStruct — 2D structural analysis
- https://github.com/AppliedMechanics-EAFIT/SolidsPy — 2D FEM
- https://github.com/CALFEM — CALFEM educational FEM

### FEATool / WELSIM / FEBio
MATLAB/Octave マルチフィジックスツールボックス（FEATool）、汎用エンジニアリングシミュレーション UI（WELSIM）、生体力学寄りの非線形 FEM（FEBio）。

- https://www.featool.com/ — https://github.com/precise-simulation/featool-multiphysics
- https://welsim.com/ — https://github.com/WelSimLLC/WelSim-Apps
- https://febio.org/ — https://github.com/febiosoftware/FEBio

---

## CFD

計算流体力学ソルバと関連マルチフィジックスコード。

### OpenFOAM
最も広く使われるオープンソース CFD ツールボックス — 流れ、伝熱、反応、多相。強い生態系（FreeCAD の CfdOF など）。

- https://www.openfoam.com/
- https://github.com/OpenFOAM/OpenFOAM-dev
- https://openfoam.org/ — community edition lineage

### SU2
マルチフィジックス PDE ソルバと勾配ベースの空力形状最適化。

- https://su2code.github.io/
- https://github.com/su2code/SU2

### Palabos / Lethe / x3d2
格子ボルツマン CFD（Palabos）；高次 CG CFD–DEM（Lethe）；GPU 高次有限差分 CFD（x3d2 / Xcompact3d 系統）。

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://lethe-cfd.github.io/lethe/ — https://github.com/lethe-cfd/lethe
- https://xcompact3d.github.io/ — https://github.com/xcompact3d/x3d2

### Fire Dynamics Simulator (FDS)
NIST の火災駆動流れ CFD。Smokeview 可視化付き。

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds

---

## トポロジー最適化

荷重と拘束のもとでの材料配置最適化。

### OpenLSTO / FEniTop / FreeTO / ToOptiX
レベルセット TO（OpenLSTO）、FEniCSx 並列 TO（FEniTop）、MATLAB 自由形状 3D TO（FreeTO）、Blender/FreeCAD アドオン付きマルチフィジックス TO（ToOptiX）。

- https://github.com/M2DOLab/OpenLSTO
- https://github.com/missionlab/fenitop
- https://github.com/ooibhadode/FreeTO
- https://github.com/ldslpm/ToOptiX

---

## MBD

マルチボディダイナミクスとモーションシミュレーション。

### MBDyn / Project Chrono / Simbody / EXUDYN
汎用 MBD（MBDyn）；車両／ロボット／粉体などのマルチフィジックス（Chrono）；関節付き生体力学（Simbody）；Python/C++ 柔軟 MBD（EXUDYN）。

- https://www.mbdyn.org/ — https://github.com/mbdyn/mbdyn
- https://projectchrono.org/ — https://github.com/projectchrono/chrono
- https://github.com/simbody/simbody
- https://github.com/jgerstmayr/EXUDYN

### OpenSim / Pinocchio
筋骨格ダイナミクス（OpenSim）；ロボティクス向け高速剛体ダイナミクス（Pinocchio）。

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio

---

## 試験と解析の相関（TAC）

CAE 結果と実機試験を突き合わせるためのツール — 計測データ、実験モード解析、モデル更新。

### 試験・シミュレーションデータ管理

#### asammdf
ASAM MDF/MF4 計測ファイル向けの高速 Python リーダ／ライタ／GUI（自動車／航空宇宙リグ、CAN/LIN）。

- https://github.com/danielhrisca/asammdf
- https://asammdf.readthedocs.io/

#### MDSplus
階層的な実験／シミュレーションデータツリー。核融合研究に起源があり、sim と試験の相関に広く使われる。

- https://mdsplus.org/
- https://github.com/MDSplus/mdsplus

#### openMDM / odsbox
Eclipse ASAM ODS 計測データ管理（openMDM）；Python ODS REST ラッパ（odsbox）。

- https://openmdm.org/ — https://github.com/EclipseFdn/openmdm.org
- https://github.com/peak-solution/odsbox

#### SciDataTool
sim と試験信号の比較向けに、時間／空間／周波数の統一的な科学フィールド保存／ポスト処理。

- https://github.com/Eomys/SciDataTool

### 実験モード解析（EMA / OMA）

#### pyEMA / sdypy-EMA / pyOMA2 / OpenModal
FRF からのモードパラメータ抽出（LSCF/LSFD）；SDyPy 後継；出力のみ OMA（SSI/FDD）；フル GUI の EMA スイート。

- https://github.com/ladisk/pyEMA
- https://github.com/sdypy/sdypy-EMA
- https://github.com/dagghe/pyOMA2
- https://www.openmodal.com/ — https://github.com/openmodal/OpenModal

#### pyFRF / pyUFF
時間信号からの FRF 推定器（H1/H2/Hv）；CAT ↔ CAE 交換向け UFF Dataset 58/55/2411/2412 I/O。

- https://github.com/ladisk/pyFRF
- https://github.com/ladisk/pyuff

### 相関指標とモデル更新

#### SDynPy / SMAC
Sandia 構造ダイナミクス Python（MAC/COMAC、FRF、曲線フィット）；MATLAB モード曲線フィット（SMAC）。

- https://sandialabs.github.io/sdynpy/ — https://github.com/sandialabs/sdynpy
- https://github.com/sandialabs/SMAC

#### pyFBS
周波数ベース部分構造合成と伝達経路解析 — 計測 FRF と FEA 部品の結合。

- https://pyfbs.readthedocs.io/
- https://gitlab.com/pyFBS/pyFBS

#### Dakota / PyDynamic
Sandia の最適化／UQ／モデル校正ツールキット；PTB/NPL の動的計測不確かさ伝播。

- https://dakota.sandia.gov/ — https://github.com/snl-dakota/dakota
- https://pydynamic.readthedocs.io/ — https://github.com/PTB-M4D/PyDynamic

### ドメイン固有の検証

#### ROSS / OpenFAST / FEBio
計測応答比較付きロータダイナミクス FEM（ROSS）；NREL 風力タービンの空力・サーボ・弾性検証（OpenFAST）；生体力学 V&V（FEBio）。

- https://ross.readthedocs.io/ — https://github.com/petrobras/ross
- https://openfast.readthedocs.io/ — https://github.com/OpenFAST/openfast
- https://febio.org/ — https://github.com/febiosoftware/FEBio

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
- https://www.openfoam.com/documentation/ — OpenFOAM docs
- https://gmsh.info/doc/texinfo/gmsh.html — Gmsh reference
- https://fenicsproject.org/documentation/ — FEniCS docs
- https://calculix.discourse.group/ — CalculiX community forum

### 規格団体
- https://www.iso.org/committee/54158.html — ISO/TC 184/SC 4（産業データ、STEP）
- https://www.asam.net/ — ASAM（MDF、ODS、関連する試験データ規格）
- https://www.nafems.org/ — NAFEMS（エンジニアリングシミュレーションコミュニティ／ベストプラクティス）

---

## 関連リスト

- https://github.com/mlightcad/awesome-cad — open-source CAD software & libraries
- https://github.com/kimimgo/awesome-ai-cae — AI-callable CAE/CAD tooling
- https://github.com/IgorAherne/awesome-CAD — CAD-related awesome list
- https://awesome.re/ — Awesome manifesto
