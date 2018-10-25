# Switch On Safety (SOS)

| **Documentation** | **Build Status** |
|:-----------------:|:----------------:|
| [![][docs-stable-img]][docs-stable-url] | [![Build Status][build-img]][build-url] [![Build Status][winbuild-img]][winbuild-url] |
| [![][docs-latest-img]][docs-latest-url] | [![Coveralls branch][coveralls-img]][coveralls-url] [![Codecov branch][codecov-img]][codecov-url] |

[<img src="examples/FinConjCounterEx.eps" height="240">](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/Finiteness_conjecture_counterexample.ipynb)

This packages implements methods for computing invariant sets using [Sum Of Squares Programming](https://github.com/JuliaOpt/SumOfSquares.jl).
It supports:
* Systems defined in [MathematicalSystems.jl](https://github.com/JuliaReach/MathematicalSystems.jl).
* Hybrid Systems defined in [HybridSystems.jl](https://github.com/blegat/HybridSystems.jl).

It also includes utilities for approximation the [Joint Spectral Radius](https://link.springer.com/book/10.1007%2F978-3-540-95980-9).

## Installation

The package currently requires Julia v1.0, you can download it [here](https://julialang.org/downloads/).
It also needs the latest unreleased versions of JuMP, PolyJuMP and SumOfSquares so once Julia is installed,
launch the REPL an type
```julia
] add JuMP#master
] add PolyJuMP#master
] add SumOfSquares#master
] add https://github.com/blegat/SwitchOnSafety.jl.git
```

## Examples

Example notebooks are available in the [`examples` folder](https://github.com/blegat/SwitchOnSafety.jl/tree/master/examples).
We link them below with the literature.

### Reproducing

The linked notebooks reproduce the results of the following papers:

* [BJP17] B. Legat, R. M. Jungers, and P. A. Parrilo.
[Certifying unstability of Switched Systems using Sum of Squares Programming](https://arxiv.org/abs/1710.01814),
arXiv preprint arXiv:1710.01814, **2017**:
[running example](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/LPJ17.ipynb),
[Example 4.3](http://localhost:8888/notebooks/LPJ17e43.ipynb).

### Exploring

The linked notebooks explores the examples of the following papers using this
package:

* [BTV03] V. D. Blondel, J. Theys and A. A. Vladimirov.
*An elementary counterexample to the finiteness conjecture*,
SIAM Journal on Matrix Analysis and Applications, **2003**. 24, 963-970:
[the counterexample](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/Finiteness_conjecture_counterexample.ipynb).
* [GZ05] N. Guglielmi and M. Zennaro.
*Polytope norms and related algorithms for the computation of the joint spectral radius*.
44th IEEE Conference on Decision and Control, and European Control Conference, **2005**, pp. 3007-3012:
[Section V](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/Finiteness_conjecture_counterexample.ipynb).
* [GZ08] N. Guglielmi and M. Zennaro.
*An algorithm for finding extremal polytope norms of matrix families*.
Linear Algebra and its Applications, **2008**, 428(10), 2265-2282:
[Section 5](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/Finiteness_conjecture_counterexample.ipynb).
* [HMST11] K. G. Hare, I. D Morris, N. Sidorov and J. Theys,
*An explicit counterexample to the Lagarias–Wang finiteness conjecture*.
Advances in Mathematics, **2011**, 226(6), 4667-4701:
[the counterexample](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/Finiteness_conjecture_counterexample.ipynb).
* [PJ08] P. Parrilo and A. Jadbabaie.
*Approximation of the joint spectral radius using sum of squares*.
Linear Algebra and its Applications, Elsevier, **2008**, 428, 2385-2402:
[Example 5.4](https://github.com/blegat/SwitchOnSafety.jl/blob/master/examples/PJ08e54.ipynb).

## How to cite

For the `soslyapb` and `sosbuildsequence` functions, cite:
```latex
@InProceedings{legat2016generating,
  author    = {Legat, Beno\^{\i}t and Jungers, Rapha\"{e}l M. and Parrilo, Pablo A.},
  title     = {{G}enerating unstable trajectories for {S}witched {S}ystems via {D}ual {S}um-{O}f-{S}quares techniques},
  booktitle = {Proceedings of the 19th International Conference on Hybrid Systems: Computation and Control},
  year      = {2016},
  series    = {HSCC '16},
  pages     = {51--60},
  publisher = {ACM},
  acmid     = {2883821},
  doi       = {10.1145/2883817.2883821},
  isbn      = {978-1-4503-3955-1},
  keywords  = {joint spectral radius, path-complete lyapunov functions, sum of squares programming, switched systems},
  location  = {Vienna, Austria},
  numpages  = {10},
  timestamp = {2016.02.18},
  url       = {http://doi.acm.org/10.1145/2883817.2883821},
}
```

For the `getis` and `fillis!` functions, cite:
```latex
@InProceedings{legat2018computing,
  author   = {Beno\^it Legat and Paulo Tabuada and Rapha\"el M. Jungers},
  title    = {Computing controlled invariant sets for hybrid systems with applications to model-predictive control},
  year     = {2018},
  volume   = {51},
  number   = {16},
  pages    = {193--198},
  note     = {6th IFAC Conference on Analysis and Design of Hybrid Systems ADHS 2018},
  doi      = {https://doi.org/10.1016/j.ifacol.2018.08.033},
  issn     = {2405-8963},
  journal  = {IFAC-PapersOnLine},
  keywords = {Controller Synthesis, Set Invariance, LMIs, Scalable Methods},
  url      = {http://www.sciencedirect.com/science/article/pii/S2405896318311480},
}
```

[docs-stable-img]: https://img.shields.io/badge/docs-stable-blue.svg
[docs-latest-img]: https://img.shields.io/badge/docs-latest-blue.svg
[docs-stable-url]: https://blegat.github.io/SwitchOnSafety.jl/stable
[docs-latest-url]: https://blegat.github.io/SwitchOnSafety.jl/latest

[build-img]: https://travis-ci.org/blegat/SwitchOnSafety.jl.svg?branch=master
[build-url]: https://travis-ci.org/blegat/SwitchOnSafety.jl
[winbuild-img]: https://ci.appveyor.com/api/projects/status/afm00qxhh89f8drm/branch/master?svg=true
[winbuild-url]: https://ci.appveyor.com/project/blegat/switchedsystems-jl/branch/master
[coveralls-img]: https://coveralls.io/repos/blegat/SwitchOnSafety.jl/badge.svg?branch=master&service=github
[coveralls-url]: https://coveralls.io/github/blegat/SwitchOnSafety.jl?branch=master
[codecov-img]: http://codecov.io/github/blegat/SwitchOnSafety.jl/coverage.svg?branch=master
[codecov-url]: http://codecov.io/github/blegat/SwitchOnSafety.jl?branch=master
