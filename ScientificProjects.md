+++
title = "Scientific Projects - Steffen Maass' Website"
hascode = true
date = Date(2024, 7, 12)
tags = ["projects", "code"]
+++


# Scientific Projects

\toc

## Modeling and Implementation of Electrocatalytic Processes with Thermodynamically Consistent Double Layers

\twoimagetextblock{/assets/plot1d.png}{/assets/electrochem_image.png}{
    Although electrocatalysis is an important instrument towards a more sustainable economy, the accurate simulation of electrocatalytic processes remains a challenge. 
    The coupling of the polarized electrochemical boundary layers at an electrode-electrolyte interface with the kinetics of the catalytic surface reactions causes difficulties for both the modeling and the numerical simulation.
    A thermodynamically consistent continuum model that resolves the boundary layers together with ab initio methods to estimate model parameters offer a computationally feasible and macroscopically accurate compromise.
    An efficient and accessible implementation may foster the computational screening of electrocatalytic materials and enable further research.
}

## Fast Fourier Transforms
\imagetextblock{/assets/fft_image.png}{
    Fast implementations of discrete Fourier transforms are needed in most scientific software.
    The best algorithms are highly optimized for the specific hardware but are, consequently, more difficult to maintain.
    We implemented high-level code in modern C++ using only standard compilers for the hardware-specific optimization.  
    The source code for the project is hosted in a [repository](https://github.com/smaasz/scicomp-project/) on GitHub.
    ~~~
    <a href="/assets/FFT_report.pdf" download="FFT_Report">[PDF]</a>
    ~~~
}


## Implementation of the Transformer Architecture
\imagetextblock{/assets/transformer_image.png}{
    In this project, I implemented the network architecture _the transformer_ that forgoes recurrence for a (self-) attention mechanism that enables faster training and more accurate machine translation of image captions. The architecture is described in detail and scores for comparison to recurrent neural networks are provided. It is demonstrated that the transformer architecture is competitive with similar RNN implementations with our BLEU score of 33.3 after only half an hour of training.
    ~~~
    <a href="/assets/transformer_report.pdf" download="Transformer_Report">[PDF]</a>
    ~~~
}
