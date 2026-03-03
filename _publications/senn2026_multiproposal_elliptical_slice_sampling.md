---
title: "Multiproposal Elliptical Slice Sampling"
collection: publications
category: manuscripts
layout: publication
date: 2026-02-27
venue: 'arXiv'
paperurl: https://arxiv.org/abs/2602.22358
---

## TL;DR
+A multiproposal variant of elliptical slice sampling designed to improve sampling efficiency for Gaussian-prior models.

## Abstract
We introduce Multiproposal Elliptical Slice Sampling, a self-tuning multiproposal Markov chain Monte Carlo method for Bayesian inference with Gaussian priors. Our method generalizes the Elliptical Slice Sampling algorithm by 1) allowing multiple candidate proposals to be sampled in parallel at each self-tuning step, and 2) basing the acceptance step on a distance-informed transition matrix that can favor proposals far from the current state. This allows larger moves in state space and faster self-tuning, at essentially no additional wall clock time for expensive likelihoods, and results in improved mixing. We additionally provide theoretical arguments and experimental results suggesting dimension-robust mixing behavior, making the algorithm particularly well suited for Bayesian PDE inverse problems.

## When to use
+- You want a plug-and-play algorithm to sample the posterior of a Bayesian model with Gaussian priors.
+- Especially useful if you have expensive likelihoods and access to parallel computing resources. 
+- Bonus: robust to mesh refinement if your model is inspired by a PDE inversion problem. 

+## Resources
+- [Paper](https://arxiv.org/abs/2602.22358)
+- [GitHub](https://github.com/guillerminasenn/mess)

