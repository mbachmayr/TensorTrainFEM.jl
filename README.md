# TensorTrainFEM

Example [Julia](https://julialang.org/) code for <https://arxiv.org/abs/1802.09062>. This package implements the multilevel tensor train decompositions of preconditioned finite element matrices and provides driver routines for solvers that rely on the separate [TensorTrains](https://github.com/mbachmayr/TensorTrains.jl) package.

To install the package, run `using Pkg; Pkg.add("https://github.com/mbachmayr/TensorTrainFEM.jl.git")`.

In addition to basic routines for assembling tensor representations from <https://arxiv.org/abs/1802.09062> in the main module, the following submodules provide driver routines for tests:
- `Poisson`, test routines for 1D and 2D Poisson problems, using `TensorTrains.Solvers`
- `Multiscale`, test routines for a 1D problem with oscillatory coefficient, using `TensorTrains.Solvers`.
- `PoissonAMEn`, test routines for 1D and 2D Poisson problems, using `TensorTrains.TTPy` (using external dependency [ttpy](https://github.com/oseledets/ttpy)).
- `MultiscaleAMEn`, test routines for a 1D problem with oscillatory coefficient, using `TensorTrains.TTPy` (using external dependency [ttpy](https://github.com/oseledets/ttpy)).