# SimpleHypergraphs.jl

*A simple hypergraphs package for the Julia programming language.*

| **Documentation** | **Build Status** |
|---------------|--------------|
|[![][docs-stable-img]][docs-stable-url] <br/> [![][docs-latest-img]][docs-dev-url]<br/>[**tutorial**][tutorial-url] | [![Build Status][travis-img]][travis-url]  [![Coverage Status][codecov-img]][codecov-url] <br/> Linux and macOS |


## Installation instructions
### Prerequisites for plotting
`Simplehypergraphs` uses the Python's [hypernetx](https://github.com/pnnl/HyperNetX) library so if you want the plotting to work you need to install it first. In Julia command line REPL press `]` for the Julia package manager and run:
```
(v1.5) pkg> add PyCall Conda
```
Now press *backspace* to exit the package manager and run the following installation code:
```julia
using PyCall
using Conda
Conda.runconda(`install matplotlib --yes`)
Conda.runconda(`install networkx --yes`)
run(`$(PyCall.python) -m pip install hypernetx`)
```
For plotting we also use the Jupyter notebook. The installation instructions are [here](https://github.com/JuliaLang/IJulia.jl#installation)
### Installation
In Julia command line REPL press `]` for the Julia package manager and run:
```
(v1.5) pkg> add SimpleHypergraphs
```
## Documentation

- [**Tutorial**][tutorial-url] &mdash; for a quick start with the library see our Jupyter Notebook tutorial (raw `*.ipynb` version can be also [downloaded][tutorial-raw])
- [**STABLE**][docs-stable-url] &mdash; **documentation of the most recently tagged version.**
- [**DEV**][docs-dev-url] &mdash; **documentation of the development version.**
- [**A Game of Thrones use case**][got-url] &mdash; check out how you can exploit the library to gather insights into real-world networks through a case study of the Game of Thrones TV series (raw `*.ipynb` version can be also [downloaded][got-raw])





[docs-latest-img]: https://img.shields.io/badge/docs-latest-blue.svg
[docs-stable-img]: https://img.shields.io/badge/docs-stable-blue.svg
[docs-dev-url]: https://pszufe.github.io/SimpleHypergraphs.jl/dev
[docs-stable-url]: https://pszufe.github.io/SimpleHypergraphs.jl/stable
[tutorial-url]: https://nbviewer.jupyter.org/github/pszufe/SimpleHypergraphs.jl/blob/master/tutorials/basics/SimpleHypergraphs_tutorial_v4.ipynb
[got-url]: https://nbviewer.jupyter.org/github/pszufe/SimpleHypergraphs.jl/blob/master/tutorials/basics/A%20case%20study%20-%20Game%20of%20Thrones.ipynb

[tutorial-raw]: https://github.com/pszufe/SimpleHypergraphs.jl/raw/master/tutorials/basics/SimpleHypergraphs_tutorial_v4.ipynb
[got-raw]: https://github.com/pszufe/SimpleHypergraphs.jl/raw/master/tutorials/basics/A%20case%20study%20-%20Game%20of%20Thrones.ipynb

[travis-img]: https://travis-ci.org/pszufe/SimpleHypergraphs.jl.svg?branch=master
[travis-url]: https://travis-ci.org/pszufe/SimpleHypergraphs.jl

[codecov-img]: https://coveralls.io/repos/github/pszufe/SimpleHypergraphs.jl/badge.svg?branch=master
[codecov-url]: https://coveralls.io/github/pszufe/SimpleHypergraphs.jl?branch=master
