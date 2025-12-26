# MMBo - Mesh Manifold Bayesian Optimisation

This repository contains demonstrations of Bayesian optimisation on mesh manifolds using geometric kernels. The project showcases how to perform Bayesian optimisation on various manifold structures by discretising them as meshes.

## Project Structure

```
├── 3D demo (Poisson surface reconstruction + BO)/  # 3D sphere demo
├── 4D sphere demo/                                  # 4D hypersphere demo
├── 6D_Demo/                                         # 6D torus demo
└── Altered packages/                                # Customised package dependencies
```

## Demonstrations

### 3D Demo (Poisson Surface Reconstruction + BO)
Demonstrates Bayesian optimisation on a 3D sphere mesh. The mesh is created via Poisson surface reconstruction from a point cloud, and BO is performed on the mesh nodes using a Matérn kernel that respects geodesic distances.

### 4D Sphere Demo
Extends the approach to a 4-dimensional hypersphere using Delaunay triangulation to create the simplicial decomposition.

### 6D Demo
Demonstrates BO on a 3-torus ($\mathbb{T}^3 = S^1 \times S^1 \times S^1$) embedded in 6-dimensional space $\mathbb{R}^6$. The 3-torus is naturally embedded in $\mathbb{R}^6$ via the product of three circles. Uses a custom mesh Laplacian based on the n-dimensional cotangent formula.

## Altered Packages

The `Altered packages` folder is intended for customised versions of the following packages:
- **GeometricKernels**: Modified to handle meshes of arbitrary dimensions
- **pymanopt**: Manifold optimisation library
- **robust-laplacians-py**: Robust Laplacian computation

### Setting Up Altered Packages

To use the altered packages, clone/download the customised package versions into the respective subfolders and install them in editable mode:

```bash
cd "Altered packages/GeometricKernels"
pip install -e .

cd "../pymanopt"
pip install -e .

cd "../robust-laplacians-py"
pip install -e .
```

## Dependencies

The main dependencies include:
- numpy
- scipy
- matplotlib
- plotly
- geometric_kernels
- pymanopt
- kaleido
- rdkit (for chemistry-related examples)

Install via:
```bash
pip install numpy scipy matplotlib plotly geometric_kernels pymanopt kaleido rdkit
```

## Usage

Each demo folder contains Jupyter notebooks and Python scripts. To run:

1. Set up the altered packages (if using custom modifications)
2. Navigate to the desired demo folder
3. Run the main notebook or script (e.g., `Main Demo.ipynb` for 6D demo)

## Key Concepts

- **Mesh Kernels**: Uses Matérn kernels defined on meshes via the Laplace-Beltrami eigendecomposition
- **Bayesian Optimisation**: Performs discrete BO on mesh vertices using Expected Improvement acquisition function
- **Geometric Awareness**: The kernel respects geodesic distances along the manifold rather than Euclidean distances

## References

- [GeometricKernels Package](https://github.com/geometric-kernels/GeometricKernels)
- [Matérn Gaussian Processes on Riemannian Manifolds (Borovitskiy et al., 2020)](https://arxiv.org/abs/2006.10160)
- [Geometry-aware Bayesian optimization in robotics (Jaquier et al., 2022)](https://arxiv.org/abs/2111.01460)
