# awesome-cad-cae

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Useful CAD / CAE resources — mechanical design, simulation, EDA, formats, and open-source toolchains for engineers and makers.

## Index

- [CAD applications](#cad-applications)
- [CAD kernels & scripting](#cad-kernels--scripting)
- [Formats & interchange](#formats--interchange)
- [EDA](#eda)
- [Meshing & visualization](#meshing--visualization)
- [CAE / FEA](#cae--fea)
- [CFD](#cfd)
- [Topology optimization](#topology-optimization)
- [MBD](#mbd)
- [Test-Analysis Correlation (TAC)](#test-analysis-correlation-tac)
- [Learning & standards](#learning--standards)
- [Related lists](#related-lists)

---

## CAD applications

Desktop and web CAD for 2D/3D mechanical design, parametric modeling, and scripting.

### FreeCAD
Parametric 3D CAD/CAE — Part Design, TechDraw, FEM (CalculiX), Path/CAM, and a large workbench ecosystem. Strong STEP/IGES support via OCCT.

- https://www.freecad.org/
- https://github.com/FreeCAD/FreeCAD
- https://wiki.freecad.org/

### SolveSpace
Lightweight parametric 2D/3D CAD with constraint solver; exports STEP/STL. Good for mechanisms and quick parts.

- https://solvespace.com/
- https://github.com/solvespace/solvespace

### OpenSCAD / ImplicitCAD / OpenJSCAD
Code-first solid modeling (CSG). OpenSCAD is the widely used baseline; ImplicitCAD and OpenJSCAD are functional / JS alternatives.

- https://openscad.org/ — https://github.com/openscad/openscad
- https://implicitcad.org/ — https://github.com/Haskell-Things/ImplicitCAD
- https://openjscad.xyz/ — https://github.com/jscad/OpenJSCAD.org

### LibreCAD / QCAD
2D CAD focused on DXF drafting.

- https://librecad.org/ — https://github.com/LibreCAD/LibreCAD
- https://qcad.org/en/ — https://github.com/qcad/qcad

### BRL-CAD
Cross-platform combinatorial solid modeling with interactive 3D editor and ray tracer; long history in military/engineering CAD.

- https://brlcad.org/
- https://github.com/BRL-CAD/brlcad

### LeoCAD / CAD Sketcher / jsketcher / Fornjot / OpenDraft
Niche or experimental CAD: LEGO CAD, Blender constraint sketcher, browser CAD, Rust CAD experiments, Avalonia 2D CAD.

- https://www.leocad.org/ — https://github.com/leozide/leocad
- https://www.cadsketcher.com/ — https://github.com/hlorus/CAD_Sketcher
- https://web-cad.org/ — https://github.com/xibyte/jsketcher
- https://www.fornjot.app/ — https://github.com/hannobraun/Fornjot
- https://github.com/JamesHodgkins/OpenDraft

### CodeToCAD
Python scripting framework aimed at driving CAD/FEA tools from one API surface.

- https://github.com/CodeToCAD/CodeToCAD

### Commercial CAD (reference)
Widely used commercial MCAD; useful for interoperability context (STEP exchange, learning materials).

- https://www.autodesk.com/products/fusion-360 — Autodesk Fusion (includes electronics successor to EAGLE)
- https://www.solidworks.com/ — SOLIDWORKS
- https://www.onshape.com/ — Onshape (browser-native)
- https://www.ptc.com/en/products/creo — Creo
- https://www.siemens.com/global/en/products/software/nx.html — Siemens NX

---

## CAD kernels & scripting

Geometric kernels and Python/scriptable modeling layers used under FreeCAD, CadQuery, and many CAE preprocessors.

### Open CASCADE Technology (OCCT)
Open-source B-Rep kernel: solids/surfaces, booleans, fillets, STEP/IGES/BREP exchange, visualization. Powers FreeCAD, CadQuery, build123d, and PrePoMax CAD import.

- https://dev.opencascade.org/
- https://occt3d.com/
- https://github.com/Open-Cascade-SAS/OCCT

### CadQuery
Python parametric CAD on OCCT — fluent API, STEP/STL/AMF/3MF export, CQGI for headless scripts.

- https://cadquery.readthedocs.io/
- https://github.com/CadQuery/cadquery

### build123d
Python BREP modeling on OCCT with context-manager (`with`) API; often described as a CadQuery evolution.

- https://build123d.readthedocs.io/
- https://github.com/gumyr/build123d

### pythonocc / OCP
Python bindings to OCCT (OCP is what CadQuery/build123d use).

- https://github.com/tpaviot/pythonocc-core
- https://github.com/CadQuery/OCP

---

## Formats & interchange

Durable exchange formats between CAD, CAM, and CAE tools.

### STEP (ISO 10303)
Primary industrial 3D CAD exchange (AP203 / AP214 / AP242). Prefer STEP over STL when you need editable B-Rep for FEA/CFD prep.

- https://www.iso.org/standard/84667.html — ISO 10303 overview / AP242 family
- https://www.cax-if.org/ — CAX Interoperability Forum (recommended practices)
- https://dev.opencascade.org/doc/overview/html/occt_user_guides__step.html — OCCT STEP guide

### IGES
Legacy surface/wireframe exchange (still common in older pipelines). Prefer STEP for new work when possible.

- https://www.nist.gov/publications/initial-graphics-exchange-specification-iges-version-50 — NIST IGES 5.0 reference

### Mesh / viz formats
- STL / OBJ — tessellated geometry (3D printing, many CFD walls)
- glTF / GLB — modern web/runtime 3D
- VTK / VTU — CAE results (ParaView)
- DXF / DWG — 2D drafting interchange

### UFF / MDF (test ↔ CAE)
- UFF Dataset 58/55 — modal/FRF interchange (see pyUFF under TAC)
- ASAM MDF/MF4 — measurement logs (see asammdf under TAC)

---

## EDA

Electronic design automation — schematic, PCB layout, and related tools.

### KiCad
Leading free/open-source EDA suite: schematic, PCB, 3D viewer, and large library ecosystem.

- https://www.kicad.org/
- https://github.com/KiCad

### LibrePCB / Horizon EDA
Modern open-source PCB design with integrated library workflows.

- https://librepcb.org/ — https://github.com/LibrePCB/LibrePCB
- https://horizon-eda.org/ — https://github.com/horizon-eda/horizon

### Fritzing
Maker-oriented EDA with breadboard view; suited to prototyping and simple PCB fabrication.

- https://fritzing.org/
- https://github.com/fritzing/fritzing-app

### DesignSpark PCB / DipTrace
Free or freemium Windows-friendly PCB tools.

- https://www.rs-online.com/designspark/pcb-software
- https://diptrace.com/

### Autodesk Fusion Electronics (EAGLE successor)
Autodesk EAGLE access ends 2026-06-07; migrate to Fusion Electronics (EAGLE designs/libraries import).

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

### Legacy EDA (historical)
Older freeware still linked for archival reference; prefer KiCad / LibrePCB / Horizon for new projects.

- http://www.freepcb.com/ — FreePCB (development largely stopped)
- http://pcb.geda-project.org/ — gEDA PCB (historic Unix PCB editor lineage)

---

## Meshing & visualization

Geometry meshing for FEA/CFD and post-processing of results.

### Gmsh
Open-source 3D FE mesh generator with built-in CAD (OCCT optional) and post-processor; scriptable `.geo` workflows and STEP import.

- https://gmsh.info/
- https://gitlab.onelab.info/gmsh/gmsh

### Netgen / NGSolve
Automatic tetrahedral meshing (also used inside PrePoMax) and NGSolve FEM platform.

- https://ngsolve.org/
- https://github.com/NGSolve/netgen

### SALOME
Open-source pre/post platform: CAD, meshing (incl. hex), and integration with Code_Aster / other solvers.

- https://www.salome-platform.org/

### ParaView
De-facto open-source scientific visualization for VTK/OpenFOAM/FEA results; Python scripting and large-data pipelines.

- https://www.paraview.org/
- https://github.com/Kitware/ParaView

### VTK
Visualization Toolkit underlying ParaView and many CAE viewers.

- https://vtk.org/
- https://github.com/Kitware/VTK

---

## CAE / FEA

Finite element and multiphysics structural / thermal solvers and frameworks.

### CalculiX + PrePoMax
Abaqus-like open-source 3D structural FEM (ccx/cgx). PrePoMax is a modern Windows GUI preprocessor/postprocessor (OCCT CAD import, Netgen/Gmsh meshing).

- https://www.dhondt.de/ — CalculiX official
- https://github.com/Dhondtguido/CalculiX
- https://github.com/calculix
- https://prepomax.fs.um.si/ — PrePoMax
- https://gitlab.com/MatejB/PrePoMax

### FEniCS / FreeFEM / SfePy
PDE/FEM platforms with strong Python (or DSL) interfaces for research and custom physics.

- https://fenicsproject.org/ — https://github.com/FEniCS
- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources
- https://sfepy.org/

### deal.II / MFEM / MOOSE / libMesh
Large-scale C++ FEM libraries (HPC, adaptive mesh, multiphysics).

- https://dealii.org/
- https://mfem.org/
- https://mooseframework.inl.gov/
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh

### Elmer / Code_Aster
Open multiphysics FEM (Elmer) and EDF’s industrial structural mechanics suite (Code_Aster), often with SALOME-Meca.

- https://www.elmerfem.org/
- https://code-aster.org/

### FrontISTR / MYSTRAN / XC / Goma
Open FEM for large-scale nonlinear structures (FrontISTR), Nastran-like analysis (MYSTRAN), structural design (XC), and free/moving-boundary coupled transport (Goma).

- https://www.frontistr.com/ — https://github.com/FrontISTR/FrontISTR
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN
- https://github.com/xcfem/xc
- https://www.gomafem.com/ — https://github.com/goma/goma

### Lightweight Python FEA
Teaching and 2D structural scripts.

- https://github.com/ritchie46/anaStruct — 2D structural analysis
- https://github.com/AppliedMechanics-EAFIT/SolidsPy — 2D FEM
- https://github.com/CALFEM — CALFEM educational FEM

### FEATool / WELSIM / FEBio
MATLAB/Octave multiphysics toolbox (FEATool), general-purpose engineering simulation UI (WELSIM), and biomechanics-focused nonlinear FEM (FEBio).

- https://www.featool.com/ — https://github.com/precise-simulation/featool-multiphysics
- https://welsim.com/ — https://github.com/WelSimLLC/WelSim-Apps
- https://febio.org/ — https://github.com/febiosoftware/FEBio

---

## CFD

Computational fluid dynamics solvers and related multiphysics codes.

### OpenFOAM
Most widely used open-source CFD toolbox — flow, heat transfer, reactions, multiphase; strong ecosystem (CfdOF in FreeCAD, etc.).

- https://www.openfoam.com/
- https://github.com/OpenFOAM/OpenFOAM-dev
- https://openfoam.org/ — community edition lineage

### SU2
Multiphysics PDE solver and gradient-based aerodynamic shape optimization.

- https://su2code.github.io/
- https://github.com/su2code/SU2

### Palabos / Lethe / x3d2
Lattice Boltzmann CFD (Palabos); high-order CG CFD–DEM (Lethe); GPU high-order finite-difference CFD (x3d2 / Xcompact3d line).

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://lethe-cfd.github.io/lethe/ — https://github.com/lethe-cfd/lethe
- https://xcompact3d.github.io/ — https://github.com/xcompact3d/x3d2

### Fire Dynamics Simulator (FDS)
NIST fire-driven flow CFD with Smokeview visualization.

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds

---

## Topology optimization

Material layout optimization under loads and constraints.

### OpenLSTO / FEniTop / FreeTO / ToOptiX
Level-set TO (OpenLSTO), FEniCSx parallel TO (FEniTop), MATLAB freeform 3D TO (FreeTO), multiphysics TO with Blender/FreeCAD addons (ToOptiX).

- https://github.com/M2DOLab/OpenLSTO
- https://github.com/missionlab/fenitop
- https://github.com/ooibhadode/FreeTO
- https://github.com/ldslpm/ToOptiX

---

## MBD

Multibody dynamics and motion simulation.

### MBDyn / Project Chrono / Simbody / EXUDYN
General-purpose MBD (MBDyn); multiphysics vehicles/robots/granular (Chrono); articulated biomechanics (Simbody); Python/C++ flexible MBD (EXUDYN).

- https://www.mbdyn.org/ — https://github.com/mbdyn/mbdyn
- https://projectchrono.org/ — https://github.com/projectchrono/chrono
- https://github.com/simbody/simbody
- https://github.com/jgerstmayr/EXUDYN

### OpenSim / Pinocchio
Musculoskeletal dynamics (OpenSim); fast rigid-body dynamics for robotics (Pinocchio).

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio

---

## Test-Analysis Correlation (TAC)

Tools for correlating CAE results with physical tests — measurement data, experimental modal analysis, and model updating.

### Test & simulation data management

#### asammdf
Fast Python reader/writer/GUI for ASAM MDF/MF4 measurement files (automotive/aerospace rigs, CAN/LIN).

- https://github.com/danielhrisca/asammdf
- https://asammdf.readthedocs.io/

#### MDSplus
Hierarchical experiment/simulation data trees; originated in fusion research, used broadly for correlating sim vs. test.

- https://mdsplus.org/
- https://github.com/MDSplus/mdsplus

#### openMDM / odsbox
Eclipse ASAM ODS measurement data management (openMDM); Python ODS REST wrapper (odsbox).

- https://openmdm.org/ — https://github.com/EclipseFdn/openmdm.org
- https://github.com/peak-solution/odsbox

#### SciDataTool
Unified scientific field storage/postprocessing (time/space/frequency) for comparing sim vs. test signals.

- https://github.com/Eomys/SciDataTool

### Experimental modal analysis (EMA / OMA)

#### pyEMA / sdypy-EMA / pyOMA2 / OpenModal
Modal parameter extraction from FRFs (LSCF/LSFD); SDyPy successor; output-only OMA (SSI/FDD); full-GUI EMA suite.

- https://github.com/ladisk/pyEMA
- https://github.com/sdypy/sdypy-EMA
- https://github.com/dagghe/pyOMA2
- https://www.openmodal.com/ — https://github.com/openmodal/OpenModal

#### pyFRF / pyUFF
FRF estimators (H1/H2/Hv) from time signals; UFF Dataset 58/55/2411/2412 I/O for CAT ↔ CAE interchange.

- https://github.com/ladisk/pyFRF
- https://github.com/ladisk/pyuff

### Correlation metrics & model updating

#### SDynPy / SMAC
Sandia structural dynamics Python (MAC/COMAC, FRF, curve-fitting); MATLAB modal curve-fitter (SMAC).

- https://sandialabs.github.io/sdynpy/ — https://github.com/sandialabs/sdynpy
- https://github.com/sandialabs/SMAC

#### pyFBS
Frequency-Based Substructuring and Transfer Path Analysis — couple measured FRFs with FEA components.

- https://pyfbs.readthedocs.io/
- https://gitlab.com/pyFBS/pyFBS

#### Dakota / PyDynamic
Sandia optimization/UQ/model calibration toolkit; PTB/NPL dynamic measurement uncertainty propagation.

- https://dakota.sandia.gov/ — https://github.com/snl-dakota/dakota
- https://pydynamic.readthedocs.io/ — https://github.com/PTB-M4D/PyDynamic

### Domain-specific validation

#### ROSS / OpenFAST / FEBio
Rotordynamics FEM with measured-response comparison (ROSS); NREL wind-turbine aero-servo-elastic validation (OpenFAST); biomechanics V&V (FEBio).

- https://ross.readthedocs.io/ — https://github.com/petrobras/ross
- https://openfast.readthedocs.io/ — https://github.com/OpenFAST/openfast
- https://febio.org/ — https://github.com/febiosoftware/FEBio

---

## Learning & standards

Intro paths and durable references (prefer official docs over random tutorials).

### Suggested open-source workflow
1. **CAD** — FreeCAD or CadQuery/build123d → export **STEP**
2. **Mesh** — Gmsh (or FreeCAD FEM / PrePoMax / SALOME)
3. **FEA** — CalculiX (PrePoMax/FreeCAD) or FEniCSx / Code_Aster
4. **CFD** — OpenFOAM (optionally FreeCAD CfdOF)
5. **Post** — ParaView

### Docs & community
- https://wiki.freecad.org/ — FreeCAD documentation
- https://www.dhondt.de/ — CalculiX manuals
- https://www.openfoam.com/documentation/ — OpenFOAM docs
- https://gmsh.info/doc/texinfo/gmsh.html — Gmsh reference
- https://fenicsproject.org/documentation/ — FEniCS docs
- https://calculix.discourse.group/ — CalculiX community forum

### Standards bodies
- https://www.iso.org/committee/54158.html — ISO/TC 184/SC 4 (industrial data, STEP)
- https://www.asam.net/ — ASAM (MDF, ODS, and related test-data standards)
- https://www.nafems.org/ — NAFEMS (engineering simulation community / best practices)

---

## Related lists

- https://github.com/mlightcad/awesome-cad — open-source CAD software & libraries
- https://github.com/kimimgo/awesome-ai-cae — AI-callable CAE/CAD tooling
- https://github.com/IgorAherne/awesome-CAD — CAD-related awesome list
- https://awesome.re/ — Awesome manifesto
