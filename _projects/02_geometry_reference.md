---
layout: page
title: Geometry-Consistent Reference Framework
description: Representation-consistent reference definition for simulation-based dimensional XCT.
img: assets/img/project_geometry_reference.png
importance: 2
category: xray-imaging
related_publications: false
---

## Overview

Simulation-based dimensional XCT requires a reference that is consistent with the actual geometric representation entering the forward model. This project investigates how CAD-to-mesh tessellation changes the represented geometry before image formation begins.

## Key contributions

- Implemented a custom **STEP- and STL-based ray-intersection tool** using an open-source CAD geometry kernel.
- Calculated X-ray penetration thickness for B-rep and tessellated geometries.
- Quantified representation differences across controlled tessellation levels.
- Developed a geometry-consistent reference framework to distinguish **input-geometry bias** from subsequent imaging, reconstruction, surface-determination, and measurement effects.

## Methods & tools

**OpenCASCADE · STEP / STL · ray intersection · Python · XCT metrology · surface analysis**
