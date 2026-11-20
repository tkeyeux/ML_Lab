# ml-lab

[![Python](https://img.shields.io/badge/python-3.10+-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/pytorch-2.x-red.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Status: Research](https://img.shields.io/badge/status-research-orange.svg)]()

**ml-lab** is a collection of self-contained ML/NN research projects, each with
a full implementation, reproducible benchmarks on public datasets, and a LaTeX
paper.

| Project | Task | Benchmark |
|---------|------|-----------|
| `pinns/` | Solve PDEs with physics-informed networks | PINNacle (20+ PDEs), PDEBench |
| `anomaly/` | Time-series anomaly detection (Transformer, VAE, decorrelation) | SMD, Server Response Time, SWaT |
| `ssl/` | Self-supervised representation learning (contrastive, masked) | CIFAR-10, UCI Time Series |
| `compression/` | Quantization, pruning, knowledge distillation | ImageNet-100, CIFAR-100 |
| `gnn/` | Graph neural networks for node/edge prediction | OGB (ogbn-arxiv, ogbn-proteins) |

All results are reproducible via `make benchmark`. Papers in `paper/` (LaTeX → PDF).

> **Status:** Research. All results are measured on public datasets.

---

## Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                        make benchmark                               │
│                    (regenerates all figures)                        │
└─────────────────────────────────────────────────────────────────────┘
         ▲               ▲                ▲                ▲
         │               │                │                │
┌────────┴─────┐  ┌──────┴──────┐  ┌──────┴──────┐   ┌─────┴──────┐
│    PINNs     │  │   Anomaly   │  │     SSL     │   │Compression │
│  FCNN + PDE  │  │ Transformer │  │ SimCLR/BYOL │   │ INT8, prune│
│  residual    │  │ VAE, R_t    │  │ MAE         │   │ distill    │
└──────────────┘  └─────────────┘  └─────────────┘   └────────────┘
         ▲               ▲                ▲                ▲
         │               │                │                │
┌────────┴───────────────┴────────────────┴────────────────┴───────┐
│                        PyTorch 2.x + CUDA 12                     │
└──────────────────────────────────────────────────────────────────┘
```

---

## Installation

### Requirements

## Quick Start

### Run all benchmarks

## Project Structure

## Papers

## Benchmarks

## Data Sources

| Source | Content | Access |
|--------|---------|--------|
| [PINNacle](https://github.com/NeurIPS-Competitive-Machine-Learning-Research/pinnacle) | 20+ PDE benchmarks | Public |
| [SMD](https://github.com/NGWO99/Anomaly_Detection_Benchmark) | 12-machine server telemetry | Public |
| [OGB](https://ogb.stanford.edu) | ogbn-arxiv, ogbn-proteins | Public |
| [CIFAR-10/100](https://www.cs.toronto.edu/~kriz/cifar.html) | Image classification | Public |
| [UCI ML Repository](https://archive.ics.uci.edu) | Time-series datasets | Public |

---

## Testing

## License

[MIT](LICENSE)

---

## Disclaimer

This project is a **research collection** for educational and scientific purposes.
All data used is publicly available. No proprietary or operational data is involved.
