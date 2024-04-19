# PBDS.jl

[![CI](https://github.com/StanfordASL/PBDS.jl/workflows/CI/badge.svg?branch=main)](https://github.com/StanfordASL/PBDS.jl/actions?query=workflow%3ACI)
[![codecov](https://codecov.io/gh/StanfordASL/PBDS.jl/branch/main/graph/badge.svg?token=vnbIkNVIGA)](https://codecov.io/gh/StanfordASL/PBDS.jl)

Julia implementation of Pullback Bundle Dynamical Systems (PBDS) framework for geometrically-consistent, multi-task reactive control on non-Euclidean robot configuration manifolds and task manifolds.

For more details on the PBDS framework, see:

A. Bylard, R. Bonalli, and M. Pavone, "Composable Geometric Motion Policies using Multi-Task Pullback Bundle Dynamical Systems," 2020. [[pdf]](https://arxiv.org/abs/2101.01297)

### Video Introduction
[![Video Introduction](https://user-images.githubusercontent.com/19652890/101411579-11370380-3896-11eb-887a-0ecec2bd9c65.png)](https://youtu.be/-NzsbF5hQ44)

# Setting up Julia
- Follow the instructions on [Julia's official website](https://julialang.org/downloads/).
- For Mac users, switch to the x64 version of Julia using Juliaup as some packages (e.g. `SpecialFunctions`) are not available for ARM.
```bash
juliaup list # List all available versions
juliaup add $x64_VERSION # Add the x64 version
juliaup default $x64_VERSION # Set the default version
```

## Running examples in VS Code
### Installation (done once)
- Install the `Julia` extension for VS Code
- For Mac users, set the default julia to a x64 version using `juliaup` as described above.

### Start Julia REPL
`ctrl+shift+p` then `Julia: Start REPL`

### Load the project
```julia
julia> cd("path/to/my/project/folder")
julia> ]
pkg> activate .
import PBDS
```
Check the status with `st`

### Install any missing package
```julia
julia> ]
(myProjectName) pkg> add $PACKAGE
```

### Troubleshooting
1. `Pkg.add("Plot")` error out
   - Install GR using `pkg> add GR`
