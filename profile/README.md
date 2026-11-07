<div align="center">

# MIST Medical

**Open-source toolkits and ready-to-run models for 3D medical imaging — segmentation, foundation-model pretraining, and the automation layered on top of them.**

[![MIST](https://img.shields.io/pypi/v/mist-medical?label=MIST&color=blue)](https://pypi.org/project/mist-medical/)
[![MISFIT](https://img.shields.io/pypi/v/misfit-medical?label=MISFIT&color=blue)](https://pypi.org/project/misfit-medical/)
[![MIST Glioma](https://img.shields.io/pypi/v/mist-glioma?label=MIST%20Glioma&color=blue)](https://pypi.org/project/mist-glioma/)
[![MIST Docs](https://img.shields.io/readthedocs/mist-medical?label=mist%20docs)](https://mist-medical.readthedocs.io/en/latest/)
[![MISFIT Docs](https://img.shields.io/readthedocs/misfit?label=misfit%20docs)](https://misfit.readthedocs.io/en/latest/)
[![License](https://img.shields.io/badge/license-Apache--2.0-lightgrey)](https://github.com/mist-medical/MIST/blob/main/LICENSE)

</div>

Everything in this org runs end-to-end — raw data in, trained models and
evaluated predictions out — with sensible defaults that work out of the box
and a config file for when you need more control. Every tool here runs on a
laptop CPU as well as a multi-GPU cluster (NVIDIA or AMD ROCm); nothing
requires a specific vendor's hardware to get started.

## Projects

| Project | What it does |
|---|---|
| **[MIST](https://github.com/mist-medical/MIST)** | End-to-end 3D medical image segmentation: analyze → preprocess → train → evaluate → predict → postprocess. One config file switches between nnU-Net, MedNeXt, Swin UNETR, and other architectures. |
| **[MIST Glioma](https://github.com/mist-medical/mist-glioma)** | Raw brain MRI to adult glioma segmentation in one command. Takes T1, T2, contrast-enhanced T1, and FLAIR images in DICOM or NIfTI and returns tumor and resection cavity masks in the native image space. Uses our third-place BraTS 2025 model. For research use only. |
| **[MISFIT](https://github.com/mist-medical/MISFIT)** | Pretrains 3D medical imaging foundation models with masked autoencoders. Point it at unlabeled NIfTI volumes and get back an encoder that transfers to segmentation, classification, and retrieval. |
| **[skills](https://github.com/mist-medical/skills)** | Claude Code Agent Skills that give an LLM working knowledge of MIST, MISFIT, and mist-autoresearch, so it can help configure and debug pipelines without re-reading the source every time. |

## Getting started

```bash
# Segmentation (CPU; runs on any machine)
pip install mist-medical

# Segmentation with NVIDIA DALI-accelerated data loading
# (highly recommended on NVIDIA GPUs)
pip install "mist-medical[dali]"

# Foundation-model pretraining
pip install misfit-medical

# Glioma segmentation from raw brain MRI
pip install mist-glioma
```

Try MIST first with the
[end-to-end Colab demo](https://colab.research.google.com/github/mist-medical/MIST/blob/main/examples/mist_heart_demo.ipynb) —
no install, no GPU required. To segment a glioma from raw DICOM images, try the
[MIST Glioma Colab demo](https://colab.research.google.com/github/mist-medical/mist-glioma/blob/main/examples/demo_colab.ipynb)
on a free GPU.

## Contributing

Issues and PRs are welcome on any repo. Each project has its own
`CONTRIBUTING.md`; start there for dev setup and test/lint conventions.

## License

All projects are released under [Apache 2.0](https://github.com/mist-medical/MIST/blob/main/LICENSE).
