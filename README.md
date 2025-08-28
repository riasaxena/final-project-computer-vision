# Final Project: Computer Vision 3D Reconstruction

This repository contains the code and resources for a **3D reconstruction pipeline** using computer vision techniques. The project involves camera calibration, point selection, and mesh generation to reconstruct 3D models from multiple images.

---

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [File Structure](#file-structure)
* [Dependencies](#dependencies)
* [License](#license)

---

## Overview

This project demonstrates an **end-to-end 3D reconstruction workflow**:

1. **Camera Calibration**: Calibrate one or more cameras to determine intrinsic and extrinsic parameters.
2. **Point Selection**: Select corresponding points across multiple images.
3. **Mesh Generation**: Generate 3D meshes (`.ply` files) from the selected points.
4. **Visualization**: View snapshots of calibration patterns, intermediate results, and final meshes.

The workflow is orchestrated in `final_project.ipynb`, which integrates calibration, mesh construction, and visualization.

---

## Features

* Camera calibration with stored parameters in `.pickle` files.
* Interactive or automated point selection for 3D reconstruction.
* Generation of 3D meshes (`.ply`) from image data.
* Visualization of calibration and mesh results.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/riasaxena/final-project-computer-vision.git
cd final-project-computer-vision
```

2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

> **Note:** If `requirements.txt` is not included, you may need packages such as `numpy`, `opencv-python`, `trimesh`, and `matplotlib`.

---

## Usage

1. Run the Jupyter notebook:

```bash
jupyter notebook final_project.ipynb
```

2. Follow the notebook to:

   * Calibrate cameras (`calibrate.py`)
   * Select points (`selectpoints.py`)
   * Generate meshes (`meshutils.py`)
   * Visualize results

3. Output meshes are saved as `.ply` files (e.g., `final.ply`).

---

## File Structure

```
final-project-computer-vision/
├── final_project.ipynb      # Main notebook orchestrating workflow
├── calibrate.py             # Camera calibration script
├── selectpoints.py          # Interactive point selection
├── meshutils.py             # 3D mesh generation utilities
├── camutils.py              # Camera helper functions
├── *.ply                    # Generated 3D meshes
├── *.pickle                 # Saved camera calibration parameters
├── snapshots/               # Example images and visualizations
└── final.mlp                # Optional machine learning model file
```

---

## Dependencies

* Python 3.8+
* numpy
* OpenCV (`opencv-python`)
* trimesh
* matplotlib
* pickle (standard library)

Additional packages may be required depending on visualization choices.
