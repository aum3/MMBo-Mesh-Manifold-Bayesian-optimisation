# Altered Packages

This folder contains customised versions of external packages required for the mesh manifold Bayesian optimisation demos.

## Packages

### GeometricKernels
A modified version of the [GeometricKernels](https://github.com/geometric-kernels/GeometricKernels) package that supports meshes of arbitrary dimensions. The original package is limited to 3D meshes; the modifications allow the dimension parameter to be adjusted for higher-dimensional simplicial complexes.

### pymanopt
[Pymanopt](https://github.com/pymanopt/pymanopt) is a Python library for manifold optimisation. Include here if custom modifications are needed.

### robust-laplacians-py
[Robust Laplacians](https://github.com/nmwsharp/robust-laplacians-py) for computing Laplacians on point clouds and meshes. Include here if custom modifications are needed.

## Installation

Each subdirectory should contain the modified package source code. Install them in editable mode so that changes are reflected immediately:

```bash
# Install each package in editable mode
pip install -e ./GeometricKernels
pip install -e ./pymanopt
pip install -e ./robust-laplacians-py
```

## Note

The subdirectories may be empty if the packages are installed directly from PyPI or if the modifications have been merged upstream. Check each demo's requirements for the specific package versions needed.
