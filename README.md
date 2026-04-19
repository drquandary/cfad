# CFAD - 3D Gaussian Splatting (Apple Optimization)

Fork of [cliffworkman/cfad](https://github.com/cliffworkman/cfad) with Apple-optimized 3D Gaussian Splatting.

## Overview

This branch integrates [3D Gaussian Splatting](https://github.com/graphdeco-inria/gaussian-splatting) with Apple Silicon optimizations using Metal for GPU-accelerated rendering on macOS devices.

### Features
- Training pipelines optimized for Apple Silicon (M1/M2/M3/M4)
- Metal-based real-time rendering engine
- Compatibility with existing Gaussian Splatting checkpoints
- Support for COLMAP and NeRF++ input formats

## Directory Structure

```
.
├── README.md           # This file
├── requirements.txt    # Python dependencies
├── gsplat/            # Core 3D Gaussian Splatting code
│   ├── train.py        # Training script
│   ├── evaluate.py     # Evaluation script
│   ├── convert.py      # Format conversion utilities
│   └── render/         # Metal rendering engine
├── models/            # Trained model checkpoints
└── (original images)  # Original CFAD image assets
```

## Quick Start

### Installation

```bash
pip install -r requirements.txt
```

### Training

```bash
python gsplat/train.py --source_path /path/to/dataset
```

### Rendering

```bash
python gsplat/render.py --model_path /path/to/trained/model
```

## References

- [3D Gaussian Splatting for Real-Time Rendering of Radiance Fields](https://repo-sam.mpi-inf.tu-dortmund.de/8357142_gaussian_splatting/original_version_paper.pdf) - Kerbl et al. (2023)
- [Inria Gaussian Splatting GitHub](https://github.com/graphdeco-inria/gaussian-splatting)

## License

Same license as the original [cliffworkman/cfad](https://github.com/cliffworkman/cfad) repository.
