# awesome-cad-cae

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

Useful CAD / CAE resources — mechanical design, simulation, EDA, formats, and open-source toolchains for engineers and makers. ⭐ badges show live GitHub star counts (via shields.io).

## Index

- [CAD applications](#cad-applications)
- [CAD kernels & scripting](#cad-kernels--scripting)
- [Formats & interchange](#formats--interchange)
- [EDA](#eda)
- [Meshing & visualization](#meshing--visualization)
- [CAE / FEA](#cae--fea)
- [Commercial-solver scripting & I/O](#commercial-solver-scripting--io)
- [CFD](#cfd)
- [Topology optimization](#topology-optimization)
- [Optimization & DOE](#optimization--doe)
- [MBD](#mbd)
- [Test-Analysis Correlation (TAC)](#test-analysis-correlation-tac)
- [Editors & syntax highlighting](#editors--syntax-highlighting)
- [Learning & standards](#learning--standards)
- [Related lists](#related-lists)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

---

## CAD applications

Desktop and web CAD for 2D/3D mechanical design, parametric modeling, and scripting.

### FreeCAD
Parametric 3D CAD/CAE — Part Design, TechDraw, Assembly, FEM (CalculiX), CAM (formerly Path), and a large workbench ecosystem. Strong STEP/IGES support via OCCT. Version 1.1 (Mar 2026) added transparent previews, interactive fillet/chamfer draggers, and a new CAM tool library.

- https://www.freecad.org/
- https://blog.freecad.org/2026/03/25/freecad-version-1-1-released/ — 1.1 release notes
- https://github.com/FreeCAD/FreeCAD ![GitHub stars](https://img.shields.io/github/stars/FreeCAD/FreeCAD?style=flat&label=%E2%AD%90)
- https://wiki.freecad.org/

### SolveSpace
Lightweight parametric 2D/3D CAD with constraint solver; exports STEP/STL. Good for mechanisms and quick parts.

- https://solvespace.com/
- https://github.com/solvespace/solvespace ![GitHub stars](https://img.shields.io/github/stars/solvespace/solvespace?style=flat&label=%E2%AD%90)

### Dune 3D
Parametric 3D CAD from the author of Horizon EDA — SolveSpace constraint solver + OCCT kernel, STEP import/export. Handy for enclosures and parts around PCBs.

- https://dune3d.org/
- https://github.com/dune3d/dune3d ![GitHub stars](https://img.shields.io/github/stars/dune3d/dune3d?style=flat&label=%E2%AD%90)

### OpenSCAD / ImplicitCAD / OpenJSCAD
Code-first solid modeling (CSG). OpenSCAD is the widely used baseline; ImplicitCAD and OpenJSCAD are functional / JS alternatives.

- https://openscad.org/ — https://github.com/openscad/openscad ![GitHub stars](https://img.shields.io/github/stars/openscad/openscad?style=flat&label=%E2%AD%90)
- https://implicitcad.org/ — https://github.com/Haskell-Things/ImplicitCAD ![GitHub stars](https://img.shields.io/github/stars/Haskell-Things/ImplicitCAD?style=flat&label=%E2%AD%90)
- https://openjscad.xyz/ — https://github.com/jscad/OpenJSCAD.org ![GitHub stars](https://img.shields.io/github/stars/jscad/OpenJSCAD.org?style=flat&label=%E2%AD%90)

### LibreCAD / QCAD
2D CAD focused on DXF drafting.

- https://librecad.org/ — https://github.com/LibreCAD/LibreCAD ![GitHub stars](https://img.shields.io/github/stars/LibreCAD/LibreCAD?style=flat&label=%E2%AD%90)
- https://qcad.org/en/ — https://github.com/qcad/qcad ![GitHub stars](https://img.shields.io/github/stars/qcad/qcad?style=flat&label=%E2%AD%90)

### BRL-CAD
Cross-platform combinatorial solid modeling with interactive 3D editor and ray tracer; long history in military/engineering CAD.

- https://brlcad.org/
- https://github.com/BRL-CAD/brlcad

### LeoCAD / CAD Sketcher / jsketcher / Fornjot / OpenDraft
Niche or experimental CAD: LEGO CAD, Blender constraint sketcher, browser CAD, Rust B-Rep kernel experiment (Fornjot — shut down, repo archived), C# 2D CAD.

- https://www.leocad.org/ — https://github.com/leozide/leocad ![GitHub stars](https://img.shields.io/github/stars/leozide/leocad?style=flat&label=%E2%AD%90)
- https://www.cadsketcher.com/ — https://github.com/hlorus/CAD_Sketcher ![GitHub stars](https://img.shields.io/github/stars/hlorus/CAD_Sketcher?style=flat&label=%E2%AD%90)
- https://web-cad.org/ — https://github.com/xibyte/jsketcher ![GitHub stars](https://img.shields.io/github/stars/xibyte/jsketcher?style=flat&label=%E2%AD%90)
- https://www.fornjot.app/ — https://github.com/hannobraun/fornjot ![GitHub stars](https://img.shields.io/github/stars/hannobraun/fornjot?style=flat&label=%E2%AD%90) (archived)
- https://github.com/JamesHodgkins/OpenDraft ![GitHub stars](https://img.shields.io/github/stars/JamesHodgkins/OpenDraft?style=flat&label=%E2%AD%90)

### CodeToCAD
Python scripting framework aimed at driving CAD/FEA tools from one API surface.

- https://github.com/CodeToCAD/CodeToCAD ![GitHub stars](https://img.shields.io/github/stars/CodeToCAD/CodeToCAD?style=flat&label=%E2%AD%90)

### Zoo Design Studio (KCL)
Code-and-GUI mechanical CAD using the KCL modeling language and a GPU-accelerated cloud geometry engine, with ML-assisted text-to-CAD. App is open source; the geometry engine is proprietary.

- https://zoo.dev/
- https://zoo.dev/docs/kcl
- https://github.com/KittyCAD/modeling-app ![GitHub stars](https://img.shields.io/github/stars/KittyCAD/modeling-app?style=flat&label=%E2%AD%90)

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
- https://github.com/Open-Cascade-SAS/OCCT ![GitHub stars](https://img.shields.io/github/stars/Open-Cascade-SAS/OCCT?style=flat&label=%E2%AD%90)

### CadQuery
Python parametric CAD on OCCT — fluent API, STEP/STL/AMF/3MF export, CQGI for headless scripts.

- https://cadquery.readthedocs.io/
- https://github.com/CadQuery/cadquery ![GitHub stars](https://img.shields.io/github/stars/CadQuery/cadquery?style=flat&label=%E2%AD%90)

### build123d
Python BREP modeling on OCCT with context-manager (`with`) API; often described as a CadQuery evolution.

- https://build123d.readthedocs.io/
- https://github.com/gumyr/build123d ![GitHub stars](https://img.shields.io/github/stars/gumyr/build123d?style=flat&label=%E2%AD%90)

### pythonocc / OCP
Python bindings to OCCT (OCP is what CadQuery/build123d use).

- https://github.com/tpaviot/pythonocc-core ![GitHub stars](https://img.shields.io/github/stars/tpaviot/pythonocc-core?style=flat&label=%E2%AD%90)
- https://github.com/CadQuery/OCP ![GitHub stars](https://img.shields.io/github/stars/CadQuery/OCP?style=flat&label=%E2%AD%90)

### Manifold
Robust triangle-mesh geometry library with fast, guaranteed-manifold booleans — the Manifold backend in OpenSCAD and the Manifold boolean solver in Blender. C++ / Python / JS (WASM) bindings.

- https://manifoldcad.org/
- https://github.com/elalish/manifold ![GitHub stars](https://img.shields.io/github/stars/elalish/manifold?style=flat&label=%E2%AD%90)

### Truck
Rust B-Rep CAD kernel by RICOS (Japan) — modular crates for NURBS geometry, topology, meshing, and WebGPU rendering.

- https://github.com/ricosjp/truck ![GitHub stars](https://img.shields.io/github/stars/ricosjp/truck?style=flat&label=%E2%AD%90)

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

### CADProps
Browser CAD and mesh inspection for STEP, IGES, STL, OBJ and selected native formats, without installing a desktop viewer. Free guest viewing and measurement; conversion and share-link creation require sign-in. Proprietary web service with server-side file processing; native-format previews and mesh measurements can be approximate.

- https://www.cadprops.com/

### UFF / MDF (test ↔ CAE)
- UFF Dataset 58/55 — modal/FRF interchange (see pyUFF under TAC)
- ASAM MDF/MF4 — measurement logs (see asammdf under TAC)

---

## EDA

Electronic design automation — schematic, PCB layout, and related tools.

### KiCad
Leading free/open-source EDA suite: schematic, PCB, 3D viewer, and large library ecosystem. KiCad 10 (Mar 2026) added design variants and improved high-speed length tuning.

- https://www.kicad.org/
- https://github.com/KiCad
- https://www.kicad.org/blog/2026/03/Version-10.0.0-Released/ — KiCad 10 release notes

### LibrePCB / Horizon EDA
Modern open-source PCB design with integrated library workflows.

- https://librepcb.org/ — https://github.com/LibrePCB/LibrePCB ![GitHub stars](https://img.shields.io/github/stars/LibrePCB/LibrePCB?style=flat&label=%E2%AD%90)
- https://horizon-eda.org/ — https://github.com/horizon-eda/horizon ![GitHub stars](https://img.shields.io/github/stars/horizon-eda/horizon?style=flat&label=%E2%AD%90)

### atopile
Design circuit boards with code (`.ato` language) — reusable modules, constraint-based part selection, and version-controlled hardware; outputs layouts to KiCad.

- https://atopile.io/
- https://github.com/atopile/atopile ![GitHub stars](https://img.shields.io/github/stars/atopile/atopile?style=flat&label=%E2%AD%90)

### Fritzing
Maker-oriented EDA with breadboard view; suited to prototyping and simple PCB fabrication.

- https://fritzing.org/
- https://github.com/fritzing/fritzing-app ![GitHub stars](https://img.shields.io/github/stars/fritzing/fritzing-app?style=flat&label=%E2%AD%90)

### DesignSpark PCB / DipTrace
Free or freemium Windows-friendly PCB tools.

- https://www.rs-online.com/designspark/pcb-software
- https://diptrace.com/

### Autodesk Fusion Electronics (EAGLE successor)
Autodesk EAGLE access ended on 2026-06-07; use Fusion Electronics (imports EAGLE designs/libraries) or migrate to KiCad.

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
- https://github.com/NGSolve/netgen ![GitHub stars](https://img.shields.io/github/stars/NGSolve/netgen?style=flat&label=%E2%AD%90)

### SALOME
Open-source pre/post platform: CAD, meshing (incl. hex), and integration with Code_Aster / other solvers.

- https://www.salome-platform.org/

### ParaView
De-facto open-source scientific visualization for VTK/OpenFOAM/FEA results; Python scripting and large-data pipelines.

- https://www.paraview.org/
- https://github.com/Kitware/ParaView ![GitHub stars](https://img.shields.io/github/stars/Kitware/ParaView?style=flat&label=%E2%AD%90)

### VTK
Visualization Toolkit underlying ParaView and many CAE viewers.

- https://vtk.org/
- https://github.com/Kitware/VTK ![GitHub stars](https://img.shields.io/github/stars/Kitware/VTK?style=flat&label=%E2%AD%90)

### PyVista / pygmsh / meshzoo
Python layers over VTK and Gmsh: streamlined 3D plotting and mesh analysis (PyVista), Gmsh scripting from Python (pygmsh), and a collection of simple meshes for canonical domains (meshzoo).

- https://github.com/pyvista/pyvista ![GitHub stars](https://img.shields.io/github/stars/pyvista/pyvista?style=flat&label=%E2%AD%90)
- https://github.com/nschloe/pygmsh ![GitHub stars](https://img.shields.io/github/stars/nschloe/pygmsh?style=flat&label=%E2%AD%90)
- https://github.com/meshpro/meshzoo ![GitHub stars](https://img.shields.io/github/stars/meshpro/meshzoo?style=flat&label=%E2%AD%90)

### meshio
Python library and CLI (`meshio convert`) to read/write many mesh formats — Gmsh, VTK/VTU, Abaqus, Nastran, Exodus, XDMF and more.

- https://github.com/nschloe/meshio ![GitHub stars](https://img.shields.io/github/stars/nschloe/meshio?style=flat&label=%E2%AD%90)

### MeshPy / PyMesh / smesh
Triangular and tetrahedral mesh generation for Python (MeshPy), geometry processing library for Python (PyMesh), and an OpenCascade-based mesh framework (smesh).

- https://mathema.tician.de/software/meshpy
- http://pymesh.readthedocs.io/en/latest
- https://github.com/tpaviot/smesh ![GitHub stars](https://img.shields.io/github/stars/tpaviot/smesh?style=flat&label=%E2%AD%90)

### Robust-Hexahedral-Re-Meshing / gridder
Structure simplification for hexahedral re-meshing; simple interactive 2D/3D orthogonal grid generator from Los Alamos National Laboratory.

- https://github.com/gaoxifeng/Robust-Hexahedral-Re-Meshing ![GitHub stars](https://img.shields.io/github/stars/gaoxifeng/Robust-Hexahedral-Re-Meshing?style=flat&label=%E2%AD%90)
- https://github.com/lanl/gridder ![GitHub stars](https://img.shields.io/github/stars/lanl/gridder?style=flat&label=%E2%AD%90)

### IsoSurfaceExtraction / glue
Isosurface extraction from regular voxel grids; linked visualizations of scientific datasets across many files.

- https://github.com/mkazhdan/IsoSurfaceExtraction ![GitHub stars](https://img.shields.io/github/stars/mkazhdan/IsoSurfaceExtraction?style=flat&label=%E2%AD%90)
- https://github.com/glue-viz/glue ![GitHub stars](https://img.shields.io/github/stars/glue-viz/glue?style=flat&label=%E2%AD%90)

---

## CAE / FEA

Finite element and multiphysics structural / thermal solvers and frameworks.

### CalculiX + PrePoMax
Abaqus-like open-source 3D structural FEM (ccx/cgx). PrePoMax is a modern Windows GUI preprocessor/postprocessor (OCCT CAD import, Netgen/Gmsh meshing).

- https://www.dhondt.de/ — CalculiX official
- https://github.com/Dhondtguido/CalculiX ![GitHub stars](https://img.shields.io/github/stars/Dhondtguido/CalculiX?style=flat&label=%E2%AD%90)
- https://github.com/calculix
- https://prepomax.fs.um.si/ — PrePoMax
- https://gitlab.com/MatejB/PrePoMax

### FEniCS / FreeFEM / SfePy
PDE/FEM platforms with strong Python (or DSL) interfaces for research and custom physics.

- https://fenicsproject.org/ — https://github.com/FEniCS
- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources ![GitHub stars](https://img.shields.io/github/stars/FreeFem/FreeFem-sources?style=flat&label=%E2%AD%90)
- https://sfepy.org/

### deal.II / MFEM / MOOSE / libMesh
Large-scale C++ FEM libraries (HPC, adaptive mesh, multiphysics).

- https://dealii.org/
- https://mfem.org/
- https://mooseframework.inl.gov/
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh ![GitHub stars](https://img.shields.io/github/stars/libMesh/libmesh?style=flat&label=%E2%AD%90)

### Elmer / Code_Aster
Open multiphysics FEM (Elmer) and EDF’s industrial structural mechanics suite (Code_Aster), often with SALOME-Meca.

- https://www.elmerfem.org/
- https://code-aster.org/

### FrontISTR / MYSTRAN / XC / Goma
Open FEM for large-scale nonlinear structures (FrontISTR), Nastran-like analysis (MYSTRAN), structural design (XC), and free/moving-boundary coupled transport (Goma).

- https://www.frontistr.com/ — https://gitlab.com/FrontISTR-Commons/FrontISTR (main development; GitHub is a mirror)
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN ![GitHub stars](https://img.shields.io/github/stars/dr-bill-c/MYSTRAN?style=flat&label=%E2%AD%90)
- https://github.com/xcfem/xc ![GitHub stars](https://img.shields.io/github/stars/xcfem/xc?style=flat&label=%E2%AD%90)
- https://www.gomafem.com/ — https://github.com/goma/goma ![GitHub stars](https://img.shields.io/github/stars/goma/goma?style=flat&label=%E2%AD%90)

### Lightweight Python FEA
Teaching and 2D structural scripts.

- https://github.com/anastruct/anaStruct ![GitHub stars](https://img.shields.io/github/stars/anastruct/anaStruct?style=flat&label=%E2%AD%90) — 2D structural analysis
- https://github.com/AppliedMechanics-EAFIT/SolidsPy ![GitHub stars](https://img.shields.io/github/stars/AppliedMechanics-EAFIT/SolidsPy?style=flat&label=%E2%AD%90) — 2D FEM
- https://github.com/CALFEM — CALFEM educational FEM
- https://github.com/JorgeDeLosSantos/nusa ![GitHub stars](https://img.shields.io/github/stars/JorgeDeLosSantos/nusa?style=flat&label=%E2%AD%90) — simple structural analysis with FEM

### OpenCourant (formerly OpenRadioss)
Explicit dynamics FEM solver for crash, impact, drop and blast (AGPL-3.0). Siemens retired OpenRadioss and deleted its GitHub repository in Oct 2026; OpenCourant is the community fork with full commit history, hosted under the Rocky Enterprise Software Foundation (RESF).

- https://opencourant.org/
- https://github.com/OpenCourant/OpenCourant ![GitHub stars](https://img.shields.io/github/stars/OpenCourant/OpenCourant?style=flat&label=%E2%AD%90)

### Kratos Multiphysics
BSD-licensed C++/Python framework for parallel multiphysics (structural, fluid, DEM, FSI, contact) with HPC/MPI support.

- https://kratosmultiphysics.github.io/Kratos/
- https://github.com/KratosMultiphysics/Kratos ![GitHub stars](https://img.shields.io/github/stars/KratosMultiphysics/Kratos?style=flat&label=%E2%AD%90)

### FEATool / WELSIM / FEBio
MATLAB/Octave multiphysics toolbox (FEATool), general-purpose engineering simulation UI (WELSIM), and biomechanics-focused nonlinear FEM (FEBio).

- https://www.featool.com/ — https://github.com/precise-simulation/featool-multiphysics ![GitHub stars](https://img.shields.io/github/stars/precise-simulation/featool-multiphysics?style=flat&label=%E2%AD%90)
- https://welsim.com/ — https://github.com/WelSimLLC/WelSim-Apps ![GitHub stars](https://img.shields.io/github/stars/WelSimLLC/WelSim-Apps?style=flat&label=%E2%AD%90)
- https://febio.org/ — https://github.com/febiosoftware/FEBio ![GitHub stars](https://img.shields.io/github/stars/febiosoftware/FEBio?style=flat&label=%E2%AD%90)

### JuliaFEM / NASTRAN-95
Julia-based open FEM for reliable, scalable, distributed analysis (JuliaFEM); NASA's open-sourced NASTRAN-95 FEM solver (historical reference).

- https://github.com/JuliaFEM/JuliaFEM.jl ![GitHub stars](https://img.shields.io/github/stars/JuliaFEM/JuliaFEM.jl?style=flat&label=%E2%AD%90)
- https://github.com/nasa/NASTRAN-95 ![GitHub stars](https://img.shields.io/github/stars/nasa/NASTRAN-95?style=flat&label=%E2%AD%90)

### Voxelyze / CFDEMcoupling / Modelica
Multi-material voxel simulation library for static and dynamic analysis (Voxelyze); coupled CFD-DEM simulation with LIGGGHTS and OpenFOAM (CFDEMcoupling); Modelica Standard Library for 1D/3D mechanical, electrical, thermal, fluid, and control models.

- https://github.com/jonhiller/Voxelyze ![GitHub stars](https://img.shields.io/github/stars/jonhiller/Voxelyze?style=flat&label=%E2%AD%90)
- https://github.com/CFDEMproject/CFDEMcoupling-PUBLIC ![GitHub stars](https://img.shields.io/github/stars/CFDEMproject/CFDEMcoupling-PUBLIC?style=flat&label=%E2%AD%90)
- https://github.com/modelica/Modelica ![GitHub stars](https://img.shields.io/github/stars/modelica/Modelica?style=flat&label=%E2%AD%90)

### PyOP2 / pyamg / OpenBLAS
Numerical building blocks: performance-portable parallel computations on unstructured meshes (PyOP2), algebraic multigrid solvers in Python (pyamg), and an optimized BLAS library (OpenBLAS).

- https://github.com/OP2/PyOP2 ![GitHub stars](https://img.shields.io/github/stars/OP2/PyOP2?style=flat&label=%E2%AD%90) — archived
- https://github.com/pyamg/pyamg ![GitHub stars](https://img.shields.io/github/stars/pyamg/pyamg?style=flat&label=%E2%AD%90)
- https://github.com/OpenMathLib/OpenBLAS ![GitHub stars](https://img.shields.io/github/stars/OpenMathLib/OpenBLAS?style=flat&label=%E2%AD%90)

---

## Commercial-solver scripting & I/O

Libraries and scripts for reading, writing, converting, and automating input / result files of commercial solvers (Nastran, Abaqus, LS-DYNA, ANSA).

### Nastran
Interface library for BDF/OP2/OP4 files (pyNastran); browser for Nastran input decks (nastran-find).

- https://github.com/SteveDoyle2/pyNastran ![GitHub stars](https://img.shields.io/github/stars/SteveDoyle2/pyNastran?style=flat&label=%E2%AD%90)
- https://github.com/setvisible/nastran-find ![GitHub stars](https://img.shields.io/github/stars/setvisible/nastran-find?style=flat&label=%E2%AD%90)

### Abaqus
Build, post-process and plot Abaqus simulations from Python (abapy); input-file parser (AbqParse); Abaqus-to-LS-DYNA keyword converter (abaqus2dyna); type hints for Abaqus/Python scripting (abqpy); automation scripts (abaqus_scripts); ODB post-processing (postPro4Abq, PyQus); ODB-to-VTK conversion (odb2vtk); job status plotter (jobwatch); documentation keyword scraper (Abaqus-Documentation-Scraper).

- https://github.com/lcharleux/abapy ![GitHub stars](https://img.shields.io/github/stars/lcharleux/abapy?style=flat&label=%E2%AD%90)
- https://github.com/crmccreary/AbqParse ![GitHub stars](https://img.shields.io/github/stars/crmccreary/AbqParse?style=flat&label=%E2%AD%90)
- https://github.com/tbhartman/abaqus2dyna ![GitHub stars](https://img.shields.io/github/stars/tbhartman/abaqus2dyna?style=flat&label=%E2%AD%90)
- https://github.com/haiiliin/abqpy ![GitHub stars](https://img.shields.io/github/stars/haiiliin/abqpy?style=flat&label=%E2%AD%90)
- https://github.com/rodrigo1392
- https://github.com/mengomarlene/postPro4Abq ![GitHub stars](https://img.shields.io/github/stars/mengomarlene/postPro4Abq?style=flat&label=%E2%AD%90)
- https://github.com/JorgeDeLosSantos/pyqus ![GitHub stars](https://img.shields.io/github/stars/JorgeDeLosSantos/pyqus?style=flat&label=%E2%AD%90)
- https://github.com/Liujie-SYSU/odb2vtk ![GitHub stars](https://img.shields.io/github/stars/Liujie-SYSU/odb2vtk?style=flat&label=%E2%AD%90)
- https://github.com/jakobgager/jobwatch ![GitHub stars](https://img.shields.io/github/stars/jakobgager/jobwatch?style=flat&label=%E2%AD%90)
- https://github.com/bendeaton/Abaqus-Documentation-Scraper ![GitHub stars](https://img.shields.io/github/stars/bendeaton/Abaqus-Documentation-Scraper?style=flat&label=%E2%AD%90)

### LS-DYNA
Python library for reading binary LS-DYNA result files (qd); fast C/C++/Python reader for binout and d3plot (dynareadout); MATLAB reader and runner (matlab-lsdyna).

- https://github.com/qd-cae/qd-cae-python ![GitHub stars](https://img.shields.io/github/stars/qd-cae/qd-cae-python?style=flat&label=%E2%AD%90) — archived
- https://pypi.org/project/dynareadout/ — PyPI (original GitHub repository no longer available)
- https://github.com/svenholcombe/matlab-lsdyna ![GitHub stars](https://img.shields.io/github/stars/svenholcombe/matlab-lsdyna?style=flat&label=%E2%AD%90)

### ANSA / CalculiX
Python utility library for scripting Beta CAE suite (qd-ansa); automated FEA model building in CalculiX from Python (pycalculix).

- https://github.com/qd-cae/qd-ansa-extension ![GitHub stars](https://img.shields.io/github/stars/qd-cae/qd-ansa-extension?style=flat&label=%E2%AD%90)
- https://github.com/spacether/pycalculix ![GitHub stars](https://img.shields.io/github/stars/spacether/pycalculix?style=flat&label=%E2%AD%90) — archived

### Mesh conversion
Converts finite element mesh files between several formats (FEconv).

- https://github.com/victorsndvg/FEconv ![GitHub stars](https://img.shields.io/github/stars/victorsndvg/FEconv?style=flat&label=%E2%AD%90)

### Abaqus user subroutines
Collections of UMAT / UEL user subroutines and a guide for setting up Abaqus with an Intel Fortran environment.

- https://github.com/jgomezc1/ABAQUS-US ![GitHub stars](https://img.shields.io/github/stars/jgomezc1/ABAQUS-US?style=flat&label=%E2%AD%90)
- https://github.com/ALandauer/ABAQUS_Subroutines ![GitHub stars](https://img.shields.io/github/stars/ALandauer/ABAQUS_Subroutines?style=flat&label=%E2%AD%90)
- https://github.com/WeilinDeng/ABAQUS ![GitHub stars](https://img.shields.io/github/stars/WeilinDeng/ABAQUS?style=flat&label=%E2%AD%90)
- https://github.com/song2001/abaqus-fortran-env-setup ![GitHub stars](https://img.shields.io/github/stars/song2001/abaqus-fortran-env-setup?style=flat&label=%E2%AD%90)

---

## CFD

Computational fluid dynamics solvers and related multiphysics codes.

### OpenFOAM
Most widely used open-source CFD toolbox — flow, heat transfer, reactions, multiphase; strong ecosystem (CfdOF in FreeCAD, etc.).

- https://www.openfoam.com/ — ESI/OpenCFD edition (latest v2606, June 2026)
- https://www.openfoam.com/news/main-news/openfoam-v2606 — v2606 release notes
- https://github.com/OpenFOAM/OpenFOAM-dev ![GitHub stars](https://img.shields.io/github/stars/OpenFOAM/OpenFOAM-dev?style=flat&label=%E2%AD%90)
- https://openfoam.org/ — community edition lineage

### SU2
Multiphysics PDE solver and gradient-based aerodynamic shape optimization.

- https://su2code.github.io/
- https://github.com/su2code/SU2 ![GitHub stars](https://img.shields.io/github/stars/su2code/SU2?style=flat&label=%E2%AD%90)

### Palabos / Lethe / x3d2
Lattice Boltzmann CFD (Palabos); high-order CG CFD–DEM (Lethe); GPU high-order finite-difference CFD (x3d2 / Xcompact3d line).

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://chaos-polymtl.github.io/lethe/ — https://github.com/chaos-polymtl/lethe ![GitHub stars](https://img.shields.io/github/stars/chaos-polymtl/lethe?style=flat&label=%E2%AD%90)
- https://xcompact3d.github.io/ — https://github.com/xcompact3d/x3d2 ![GitHub stars](https://img.shields.io/github/stars/xcompact3d/x3d2?style=flat&label=%E2%AD%90)

### Fire Dynamics Simulator (FDS)
NIST fire-driven flow CFD with Smokeview visualization.

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds ![GitHub stars](https://img.shields.io/github/stars/firemodels/fds?style=flat&label=%E2%AD%90)

---

## Topology optimization

Material layout optimization under loads and constraints.

### OpenLSTO / FEniTop / FreeTO / ToOptiX
Level-set TO (OpenLSTO), FEniCSx parallel TO (FEniTop), MATLAB freeform 3D TO (FreeTO), multiphysics TO with Blender/FreeCAD addons (ToOptiX).

- https://github.com/M2DOLab/OpenLSTO ![GitHub stars](https://img.shields.io/github/stars/M2DOLab/OpenLSTO?style=flat&label=%E2%AD%90)
- https://github.com/missionlab/fenitop ![GitHub stars](https://img.shields.io/github/stars/missionlab/fenitop?style=flat&label=%E2%AD%90)
- https://github.com/ooibhadode/FreeTO ![GitHub stars](https://img.shields.io/github/stars/ooibhadode/FreeTO?style=flat&label=%E2%AD%90)
- https://github.com/Foxelmanian/ToOptix ![GitHub stars](https://img.shields.io/github/stars/Foxelmanian/ToOptix?style=flat&label=%E2%AD%90)

---

## Optimization & DOE

General optimization, design of experiments, and multidisciplinary design frameworks.

### OpenMDAO / pyDOE
High-performance Python platform for systems analysis and multidisciplinary optimization (OpenMDAO); design-of-experiments library (pyDOE).

- https://github.com/OpenMDAO/OpenMDAO ![GitHub stars](https://img.shields.io/github/stars/OpenMDAO/OpenMDAO?style=flat&label=%E2%AD%90)
- https://github.com/pydoe/pydoe ![GitHub stars](https://img.shields.io/github/stars/pydoe/pydoe?style=flat&label=%E2%AD%90)

### CasADi / YALMIP
Symbolic framework for numeric optimization with automatic differentiation (CasADi); MATLAB toolbox for optimization modeling (YALMIP).

- https://github.com/casadi/casadi ![GitHub stars](https://img.shields.io/github/stars/casadi/casadi?style=flat&label=%E2%AD%90)
- https://github.com/yalmip/YALMIP ![GitHub stars](https://img.shields.io/github/stars/yalmip/YALMIP?style=flat&label=%E2%AD%90)

---

## MBD

Multibody dynamics and motion simulation.

### MBDyn / Project Chrono / Simbody / EXUDYN
General-purpose MBD (MBDyn); multiphysics vehicles/robots/granular (Chrono); articulated biomechanics (Simbody); Python/C++ flexible MBD (EXUDYN).

- https://www.mbdyn.org/ — https://public.gitlab.polimi.it/DAER/mbdyn
- https://projectchrono.org/ — https://github.com/projectchrono/chrono ![GitHub stars](https://img.shields.io/github/stars/projectchrono/chrono?style=flat&label=%E2%AD%90)
- https://github.com/simbody/simbody ![GitHub stars](https://img.shields.io/github/stars/simbody/simbody?style=flat&label=%E2%AD%90)
- https://github.com/jgerstmayr/EXUDYN ![GitHub stars](https://img.shields.io/github/stars/jgerstmayr/EXUDYN?style=flat&label=%E2%AD%90)

### OpenSim / Pinocchio
Musculoskeletal dynamics (OpenSim); fast rigid-body dynamics for robotics (Pinocchio).

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio ![GitHub stars](https://img.shields.io/github/stars/stack-of-tasks/pinocchio?style=flat&label=%E2%AD%90)

---

## Test-Analysis Correlation (TAC)

Tools for correlating CAE results with physical tests — measurement data, experimental modal analysis, and model updating.

### Test & simulation data management

#### asammdf
Fast Python reader/writer/GUI for ASAM MDF/MF4 measurement files (automotive/aerospace rigs, CAN/LIN).

- https://github.com/danielhrisca/asammdf ![GitHub stars](https://img.shields.io/github/stars/danielhrisca/asammdf?style=flat&label=%E2%AD%90)
- https://asammdf.readthedocs.io/

#### MDSplus
Hierarchical experiment/simulation data trees; originated in fusion research, used broadly for correlating sim vs. test.

- https://mdsplus.org/
- https://github.com/MDSplus/mdsplus ![GitHub stars](https://img.shields.io/github/stars/MDSplus/mdsplus?style=flat&label=%E2%AD%90)

#### openMDM / odsbox
Eclipse ASAM ODS measurement data management (openMDM); Python ODS REST wrapper (odsbox).

- https://openmdm.org/
- https://github.com/peak-solution/odsbox ![GitHub stars](https://img.shields.io/github/stars/peak-solution/odsbox?style=flat&label=%E2%AD%90)

#### SciDataTool
Unified scientific field storage/postprocessing (time/space/frequency) for comparing sim vs. test signals.

- https://github.com/Eomys/SciDataTool ![GitHub stars](https://img.shields.io/github/stars/Eomys/SciDataTool?style=flat&label=%E2%AD%90)

### Experimental modal analysis (EMA / OMA)

#### pyEMA / sdypy-EMA / pyOMA2 / OpenModal
Modal parameter extraction from FRFs (LSCF/LSFD); SDyPy successor; output-only OMA (SSI/FDD); full-GUI EMA suite.

- https://github.com/ladisk/pyEMA ![GitHub stars](https://img.shields.io/github/stars/ladisk/pyEMA?style=flat&label=%E2%AD%90)
- https://github.com/sdypy/sdypy-EMA ![GitHub stars](https://img.shields.io/github/stars/sdypy/sdypy-EMA?style=flat&label=%E2%AD%90)
- https://github.com/dagghe/pyOMA2 ![GitHub stars](https://img.shields.io/github/stars/dagghe/pyOMA2?style=flat&label=%E2%AD%90)
- https://www.openmodal.com/ — https://github.com/openmodal/OpenModal ![GitHub stars](https://img.shields.io/github/stars/openmodal/OpenModal?style=flat&label=%E2%AD%90)

#### pyFRF / pyUFF
FRF estimators (H1/H2/Hv) from time signals; UFF Dataset 58/55/2411/2412 I/O for CAT ↔ CAE interchange.

- https://github.com/ladisk/pyFRF ![GitHub stars](https://img.shields.io/github/stars/ladisk/pyFRF?style=flat&label=%E2%AD%90)
- https://github.com/ladisk/pyuff ![GitHub stars](https://img.shields.io/github/stars/ladisk/pyuff?style=flat&label=%E2%AD%90)

### Correlation metrics & model updating

#### SDynPy / SMAC
Sandia structural dynamics Python (MAC/COMAC, FRF, curve-fitting); MATLAB modal curve-fitter (SMAC).

- https://sandialabs.github.io/sdynpy/ — https://github.com/sandialabs/sdynpy ![GitHub stars](https://img.shields.io/github/stars/sandialabs/sdynpy?style=flat&label=%E2%AD%90)
- https://github.com/sandialabs/SMAC ![GitHub stars](https://img.shields.io/github/stars/sandialabs/SMAC?style=flat&label=%E2%AD%90)

#### pyFBS
Frequency-Based Substructuring and Transfer Path Analysis — couple measured FRFs with FEA components.

- https://pyfbs.readthedocs.io/
- https://gitlab.com/pyFBS/pyFBS

#### Dakota / PyDynamic
Sandia optimization/UQ/model calibration toolkit; PTB/NPL dynamic measurement uncertainty propagation.

- https://dakota.sandia.gov/ — https://github.com/snl-dakota/dakota ![GitHub stars](https://img.shields.io/github/stars/snl-dakota/dakota?style=flat&label=%E2%AD%90)
- https://pydynamic.readthedocs.io/ — https://github.com/PTBresearch/PyDynamic ![GitHub stars](https://img.shields.io/github/stars/PTBresearch/PyDynamic?style=flat&label=%E2%AD%90)

### Domain-specific validation

#### ROSS / OpenFAST / FEBio
Rotordynamics FEM with measured-response comparison (ROSS); NLR (formerly NREL) wind-turbine aero-servo-elastic validation (OpenFAST); biomechanics V&V (FEBio).

- https://ross.readthedocs.io/ — https://github.com/petrobras/ross ![GitHub stars](https://img.shields.io/github/stars/petrobras/ross?style=flat&label=%E2%AD%90)
- https://openfast.readthedocs.io/ — https://github.com/OpenFAST/openfast ![GitHub stars](https://img.shields.io/github/stars/OpenFAST/openfast?style=flat&label=%E2%AD%90)
- https://febio.org/ — https://github.com/febiosoftware/FEBio ![GitHub stars](https://img.shields.io/github/stars/febiosoftware/FEBio?style=flat&label=%E2%AD%90)

---

## Editors & syntax highlighting

Editor plugins for solver input files.

### Vim
Plugins and lexers for LS-DYNA, Abaqus, and RADIOSS input files.

- https://github.com/gradzikb/vim-lsdyna ![GitHub stars](https://img.shields.io/github/stars/gradzikb/vim-lsdyna?style=flat&label=%E2%AD%90)
- https://github.com/tbhartman/vim-lexer-lsdyna ![GitHub stars](https://img.shields.io/github/stars/tbhartman/vim-lexer-lsdyna?style=flat&label=%E2%AD%90)
- https://github.com/gradzikb/vim-abaqus ![GitHub stars](https://img.shields.io/github/stars/gradzikb/vim-abaqus?style=flat&label=%E2%AD%90)
- https://github.com/gradzikb/vim-radioss ![GitHub stars](https://img.shields.io/github/stars/gradzikb/vim-radioss?style=flat&label=%E2%AD%90)

### Sublime Text
Syntax highlighting for LS-DYNA and Abaqus.

- https://github.com/bendeaton/LS-DYNA-Sublime ![GitHub stars](https://img.shields.io/github/stars/bendeaton/LS-DYNA-Sublime?style=flat&label=%E2%AD%90)
- https://github.com/bendeaton/Abaqus-Sublime ![GitHub stars](https://img.shields.io/github/stars/bendeaton/Abaqus-Sublime?style=flat&label=%E2%AD%90)

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
- https://www.openfoam.com/documentation/overview — OpenFOAM docs
- https://gmsh.info/doc/texinfo/gmsh.html — Gmsh reference
- https://fenicsproject.org/documentation/ — FEniCS docs
- https://calculix.discourse.group/ — CalculiX community forum

### Standards bodies
- https://www.iso.org/committee/54158.html — ISO/TC 184/SC 4 (industrial data, STEP)
- https://www.asam.net/ — ASAM (MDF, ODS, and related test-data standards)
- https://www.nafems.org/ — NAFEMS (engineering simulation community / best practices)

---

## Related lists

- https://github.com/shvyac/awesome-meshless-cae ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90) — meshless / mesh-free CAE tools (SPH, MPS, LBM, MPM, peridynamics, IGA, AI surrogates)
- https://github.com/qd-cae/awesome-CAE ![GitHub stars](https://img.shields.io/github/stars/qd-cae/awesome-CAE?style=flat&label=%E2%AD%90) — CAE frameworks, libraries and software (Abaqus / Nastran / LS-DYNA scripting)
- https://github.com/mlightcad/awesome-cad ![GitHub stars](https://img.shields.io/github/stars/mlightcad/awesome-cad?style=flat&label=%E2%AD%90) — open-source CAD software & libraries
- https://github.com/kimimgo/awesome-ai-cae ![GitHub stars](https://img.shields.io/github/stars/kimimgo/awesome-ai-cae?style=flat&label=%E2%AD%90) — AI-callable CAE/CAD tooling
- https://awesome.re/ — Awesome manifesto

---

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

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
