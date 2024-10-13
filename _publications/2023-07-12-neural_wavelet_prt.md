---
title: "Neural Free‐Viewpoint Relighting for Glossy Indirect Illumination"
collection: publications
category: conferences
permalink: /publication/neural_wavelet_prt
excerpt: 'Learning the PRT using wavelet and Neural Fields. <br /> ![Pipeline](/images/neural_wavelet_prt_pipeline.png "Pipeline")'
date: 2023-07-12
venue: 'EGSR (Journal Track)'
# slidesurl: 'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://arxiv.org/abs/2307.06335'
projecturl: 'https://cseweb.ucsd.edu/~viscomp/projects/EGSR23NeRT/'
codeurl: 'https://github.com/AlstonXiao/neural_wavelet_prt_demo'
citation: 'Raghavan, N., Xiao, Y., Lin, K.-E., Sun, T., Bi, S., Xu, Z., Li, T.-M. and Ramamoorthi, R. (2023), Neural Free-Viewpoint Relighting for Glossy Indirect Illumination. Computer Graphics Forum, 42: e14885. https://doi.org/10.1111/cgf.14885'
---
![Pipeline](/images/neural_wavelet_prt_pipeline.png "Pipeline")
Precomputed Radiance Transfer (PRT) remains an attractive solution for real-time rendering of complex light transport effects such as glossy global illumination. After precomputation, we can relight the scene with new environment maps while changing viewpoint in real-time. However, practical PRT methods are usually limited to low-frequency spherical harmonic lighting. All-frequency techniques using wavelets are promising but have so far had little practical impact. The curse of dimensionality and much higher data requirements have typically limited them to relighting with fixed view or only direct lighting with triple product integrals. In this paper, we demonstrate a hybrid neural-wavelet PRT solution to high-frequency indirect illumination, including glossy reflection, for relighting with changing view. Specifically, we seek to represent the light transport function in the Haar wavelet basis. For global illumination, we learn the wavelet transport using a small multi-layer perceptron (MLP) applied to a feature field as a function of spatial location and wavelet index, with reflected direction and material parameters being other MLP inputs. We optimize/learn the feature field (compactly represented by a tensor decomposition) and MLP parameters from multiple images of the scene under different lighting and viewing conditions. We demonstrate real-time (512 x 512 at 24 FPS, 800 x 600 at 13 FPS) precomputed rendering of challenging scenes involving view-dependent reflections and even caustics.