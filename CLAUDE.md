# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a tutorial/educational project exploring the Muon optimizer, an increasingly popular alternative to Adam/AdamW. The project uses Jupyter notebooks for interactive experimentation and visualization.

## Development Environment

**Package Manager**: Uses `uv` for dependency management (modern Python package manager)

**Python Version**: Requires Python >=3.12

**Core Dependencies**:
- PyTorch (>=2.8.0) - Deep learning framework
- NumPy, Matplotlib, Seaborn - Numerical computing and visualization
- Black - Code formatting

## Common Commands

Install/sync dependencies:
```bash
uv sync
```

Launch Jupyter Lab:
```bash
uv run --with jupyter jupyter lab
```

Format code:
```bash
uv run black .
```

## Project Structure

The main work is in `muon.ipynb`, which contains:
- Mathematical background on optimizers (SGD, Momentum, RMSProp, Adam, AdamW)
- Detailed notation and dimensionality explanations
- Comparison of different optimization approaches
- Implementation/exploration of the Muon optimizer

## TODO

Help me with my notes on the muon optimizer, largely following the derivation iiin https://kellerjordan.github.io/posts/muon/

I want to add:

1) a little section on shampoo and why this is a different class of optimizers

2) Basic muon formulation, and a coarse implementation via either random numpy or randomized pytorch tensors.
   1) Demonstration of orthogonality of the numpy/pytorch tensors via the Newton Shutlz update mechanism
   2) A visually obvious demonstration of AdamW vs Muon with a few update steps on gradient descent on a texture advantageous to Muon
