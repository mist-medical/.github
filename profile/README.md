<div align="center">

# MIST Medical

**Open-source toolkits for 3D medical imaging — segmentation, foundation-model pretraining, and the automation layered on top of them.**

[![MIST](https://img.shields.io/pypi/v/mist-medical?label=MIST&color=blue)](https://pypi.org/project/mist-medical/)
[![MISFIT](https://img.shields.io/pypi/v/misfit-medical?label=MISFIT&color=blue)](https://pypi.org/project/misfit-medical/)
[![Docs](https://img.shields.io/badge/docs-MIST-brightgreen)](https://mist-medical.readthedocs.io/en/latest/)
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
| **[MISFIT](https://github.com/mist-medical/MISFIT)** | Pretrains 3D medical imaging foundation models with masked autoencoders. Point it at unlabeled NIfTI volumes and get back an encoder that transfers to segmentation, classification, and retrieval. |
| **[skills](https://github.com/mist-medical/skills)** | Claude Code Agent Skills that give an LLM working knowledge of MIST, MISFIT, and mist-autoresearch, so it can help configure and debug pipelines without re-reading the source every time. |

## Getting started

```bash
# Segmentation
pip install mist-medical

# Foundation-model pretraining
pip install misfit-medical
```

Try MIST first with the
[end-to-end Colab demo](https://colab.research.google.com/github/mist-medical/MIST/blob/main/examples/mist_heart_demo.ipynb) —
no install, no GPU required.

## Contributing

Issues and PRs are welcome on any repo. Each project has its own
`CONTRIBUTING.md`; start there for dev setup and test/lint conventions.

## License

All projects are released under [Apache 2.0](https://github.com/mist-medical/MIST/blob/main/LICENSE).
