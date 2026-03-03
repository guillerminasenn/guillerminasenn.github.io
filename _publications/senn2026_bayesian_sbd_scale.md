---
title: "Bayesian Semi-Blind Deconvolution at Scale"
collection: publications
category: manuscripts
layout: publication
date: 2026-01-14
venue: 'arXiv'
paperurl: https://arxiv.org/abs/2601.09677
---

## TL;DR
Bayesian approach (model + MCMC algorithms) for semi-blind deconvolution that scales to large datasets.

## Abstract
Blind image deconvolution refers to the problem of simultaneously estimating the blur kernel and the true image from a set of observations when both the blur kernel and the true image are unknown. Sometimes, additional image and/or blur information is available and the term semi-blind deconvolution (SBD) is used. We consider a recently introduced Bayesian conjugate hierarchical model for SBD, formulated on an extended cyclic lattice to allow a computationally scalable Gibbs sampler. In this article, we extend this model to the general SBD problem, rewrite the previously proposed Gibbs sampler so that operations are performed in the Fourier domain whenever possible, and introduce a new marginal Hamiltonian Monte Carlo (HMC) blur update, obtained by analytically integrating the blur-image joint conditional over the image. The cyclic formulation combined with non-trivial linear algebra manipulations allows a Fourier-based, scalable HMC update, otherwise complicated by the rigid constraints of the SBD problem. Having determined the padding size in the cyclic embedding through a numerical experiment, we compare the mixing and exploration behaviour of the Gibbs and HMC blur updates on simulated data and on a real geophysical seismic imaging problem where we invert a grid with 300x50 nodes, corresponding to a posterior with approximately 80k parameters.

## When to use
- You need semi-blind deconvolution for large-scale data.
- You are OK with Gaussian image and blur priors.
- Semi-blindness is enforced by hard constraints (exact image observations) on the image, such as well observations in seismic inversion.
- Note: We recommend using Gibbs sampling when enough constraints, and HMC or a combination of both otherwise.

## Resources
- [Paper](https://arxiv.org/abs/2601.09677)
- [GitHub](https://github.com/guillerminasenn/bsbd)
