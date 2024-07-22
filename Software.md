+++
title = "Software - Steffen Maass' Website"
hascode = true
date = Date(2024, 7, 12)
tags = ["projects", "code"]
+++

# Software

\toc 

## Simulation of Heterogeneous Catalysis in Julia
I implemented a software package `CatmapInterface.jl` in the programming language [Julia](https://julialang.org/) for integrating the reaction kinetics of heterogeneous catalytic mechanisms into a solver of a macroscopic transport model for electrochemical cells.
The package implements an _interpreter_ for the [CatMAP](https://catmap.readthedocs.io/en/latest/index.html) specification of the microkinetic model that generates a symbolic-numeric ODE-model (see [Catalyst.ReactionSystem](https://docs.sciml.ai/Catalyst/stable/api/#Catalyst.ReactionSystem)).
As an example I used the package to simulate the electrochemical reduction of carbon dioxide dissolved in a supporting electrolyte at a gold surface.
There, I used the developed package to integrate a microkinetic model with rate constants based on quantum chemical calculations with [Quantum ESPRESSO](https://www.quantum-espresso.org/) into a [Voronoi-finite-volume](https://docs.sciml.ai/VoronoiFVM/stable/method/) solver of the transport model.
The package has not yet been published.

## Fast Fourier Transform in Modern C++ [[GitHub repository]](https://github.com/smaasz/fft-moderncpp-project/)
I implemented a depth-first ([Cooley-Tukey](https://en.wikipedia.org/wiki/Cooley%E2%80%93Tukey_FFT_algorithm)) and breadth-first (recursive) version of the _mixded-radix_ fast Fourier transform (FFT).
Details on the algorithm and its complexity can be found the in the [report](https://github.com/smaasz/fft-moderncpp-project/blob/main/fft_report.pdf).
The algorithms are implemented in [C++17](https://en.wikipedia.org/wiki/C%2B%2B17) using the [Standard Template Library (STL)](https://en.wikipedia.org/wiki/Standard_Template_Library).
Both implementations are templates in order to use different complex data types (e.g. `std::complex<float>`).
In addition a command line interface (CLI) is implemented as well as [bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) scripts using [AWK](https://en.wikipedia.org/wiki/AWK) for data post-processing and [gnuplot](http://gnuplot.info/) for creating scientific visualizations.
\\[[GitHub repository](https://github.com/smaasz/fft-moderncpp-project/)\]


## Transformer Architecture in Python with TensorFlow [[Notebook]](https://colab.research.google.com/drive/188j2xybfrcERdoTB7TacKfXvWdAjjZEM?usp=sharing)
I implemented a AI-based machine translation program in Python trained on the [Multi30K dataset](https://aclanthology.org/W16-3210). 
The data pre-processing pipline uses [TensorFlow framework](https://www.tensorflow.org/).
The translation model uses a transformer architecture first proposed by Vaswani et al. in the paper with the title [_Attention is all you need_](https://doi.org/10.48550/arXiv.1706.03762).
The _multi-head attention layer_ is implemeted as a [Tensorflow layer](https://www.tensorflow.org/api_docs/python/tf/keras/Layer) object.
A [Google Colaboratory](https://colab.research.google.com/) notebook with the implementation of the architecture, the pre-processing pipeline, training and testing routines can be run in Google's cloud on a hardware with a GPU.
\\[[Notebook](https://colab.research.google.com/drive/188j2xybfrcERdoTB7TacKfXvWdAjjZEM?usp=sharing)\]
