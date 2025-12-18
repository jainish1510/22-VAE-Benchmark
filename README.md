# Systematic Benchmark of 22 Variational Autoencoder Architectures

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Comprehensive evaluation of 22 VAE architectures, highlighting the trade-off between reconstruction quality and interpolation smoothness.

## 📄 Paper

**On the Quality-Smoothness Duality in Variational Autoencoders: A Systematic Benchmark of Twenty-Two Architectures**

[Read the full paper](./22-VAE-Benchmark.pdf)

## 🎯 Overview

This repository presents a systematic comparison of 22 VAE architectures under unified conditions. It demonstrates a **quality-smoothness duality**: architectures that excel at reconstruction produce discontinuous interpolations, while smooth interpolators sacrifice reconstruction fidelity.

### Key Findings

- Significant performance gap in reconstruction quality and interpolation smoothness
- Strong positive correlation between SSIM and PIQ, showing inverse quality relationship
- Three distinct architectural regimes identified via Pareto frontier analysis

## 🏗️ Architecture

Benchmarking covers 22 VAE variants:

- **Standard & Importance-Weighted:** VAE, IWAE, MIWAE, CIWAE, PIWAE
- **Disentanglement Methods:** β-VAE, β-TCVAE, FactorVAE, Disentangled β-VAE
- **Architecture Variants:** VQ-VAE, HVAE, VAE-IAF, VAE-LinNF
- **Alternative Regularization:** WAE, InfoVAE, RAE-L2, RAE-GP
- **Prior Variants:** VampPrior VAE, SVAE
- **Specialized:** MS-SSIM-VAE, Adversarial Autoencoder (AAE), AE

## 📊 Metrics

- **Perceptual Interpolation Quality (PIQ)** – lower is smoother
- **Interpolation Smoothness Score (ISS)** – lower indicates uniform transitions
- **Interpolation SSIM (I-SSIM)** – higher indicates structural consistency

## 🎯 Practical Recommendations

- **Reconstruction-focused:** VQ-VAE, AE, WAE
- **Interpolation-focused:** VAE-LinNF, SVAE, RAE-GP
- **Balanced:** RAE-GP, RAE-L2, Standard VAE

