# cirrus-jhub-images
This repository is where Custom Jupyter images for use with the CISL CIRRUS JupyterHub are maintained and built via GitHub Actions on GitHub Actions Runner scale sets.

Images are built with a matrix strategy across two workflows: **dev** (builds on push to `main` affecting `notebook-images/`, tags as `latest` + short SHA) and **prod** (builds on semver tag push `X.Y.Z`, tags with the release version). Each workflow builds the base image, then the CPU/GPU notebook images, then the TensorFlow/PyTorch GPU images.

| Workflow | Status |
|---|---|
| **Build and push dev images** | ![Dev Build Status](https://github.com/NCAR/cirrus-jhub-images/actions/workflows/dev.yaml/badge.svg) |
| **Build and push prod images** | ![Prod Build Status](https://github.com/NCAR/cirrus-jhub-images/actions/workflows/prod.yaml/badge.svg) |