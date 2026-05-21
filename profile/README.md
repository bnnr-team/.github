<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/bnnr-team/.github/main/profile/logo_dark.png" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/bnnr-team/.github/main/profile/logo_light.png" />
    <img alt="BNNR" src="https://raw.githubusercontent.com/bnnr-team/.github/main/profile/logo_dark.png" width="280" />
  </picture>
</p>

<h3 align="center">Bulletproof Neural Network Recipe</h3>

<p align="center">
  <strong>Train &rarr; Explain &rarr; Improve &rarr; Prove</strong>
</p>

<p align="center">
  <strong>BNNR automatically improves your PyTorch vision models using XAI</strong> &mdash; find what your model gets wrong,<br/>
  fix it with intelligent augmentation, and prove the result with structured reports and a live dashboard.
</p>

<p align="center">
  <strong>Already have a trained model?</strong> Run <code>bnnr analyze</code> for metrics, XAI, failure patterns, and recommendations &mdash; no retraining.<br/>
  <a href="https://github.com/bnnr-team/bnnr/blob/main/docs/analyze.md">Model analysis docs</a>
</p>

<p align="center">
  <a href="https://pypi.org/project/bnnr/"><img src="https://img.shields.io/pypi/v/bnnr?color=orange&label=PyPI" alt="PyPI version" /></a>&nbsp;
  <a href="https://pypi.org/project/bnnr/"><img src="https://img.shields.io/pypi/pyversions/bnnr?color=blue" alt="Python versions" /></a>&nbsp;
  <a href="https://pepy.tech/projects/bnnr"><img src="https://static.pepy.tech/personalized-badge/bnnr?period=total&amp;units=INTERNATIONAL_SYSTEM&amp;left_color=BLACK&amp;right_color=GREEN&amp;left_text=downloads" alt="PyPI downloads" /></a>&nbsp;
  <a href="https://github.com/bnnr-team/bnnr/blob/main/LICENSE"><img src="https://img.shields.io/github/license/bnnr-team/bnnr" alt="License" /></a>&nbsp;
  <a href="https://www.bnnr.dev"><img src="https://img.shields.io/badge/docs-bnnr.dev-blue" alt="Docs" /></a>
</p>

<p align="center">
  <a href="https://www.bnnr.dev"><strong>Watch the full demo (with audio) on bnnr.dev</strong></a>
</p>

---

### How it works

| Step | What happens |
|:----:|:-------------|
| **Train** | Start with your PyTorch model and data. BNNR trains a baseline, then iteratively evaluates candidate augmentations — keeping only those that measurably improve performance. |
| **Explain** | OptiCAM, GradCAM, NMF, and CRAFT saliency maps reveal what the model focuses on. Per-class diagnoses expose blind spots and biases invisible to accuracy alone. |
| **Improve** | Intelligent Coarse Dropout (ICD) masks salient regions, forcing the model to learn from context. AICD sharpens focus on key features. Both are XAI-driven and automatic. |
| **Prove** | A structured report with metrics, XAI heatmaps, branch decisions, and before/after comparisons — shareable, auditable, and ready for stakeholders. |

---

### Key features

- **Zero-config CLI** — `bnnr train` and `bnnr quickstart` work without a YAML file; sensible defaults built in
- **Model analysis (`bnnr analyze`)** — full diagnostic report on any trained checkpoint without retraining
- **Auto-Augment Search** — iterative branching strategy that tests augmentations against a baseline
- **Image Classification & Object Detection** — classification, multi-label, and detection (COCO-mini / YOLO) with bbox-aware augmentations and mAP metrics (**v0.3.1**)
- **XAI Explainability** — OptiCAM, GradCAM, NMF, and CRAFT heatmaps with per-class severity and trend analysis
- **ICD & AICD** — XAI-driven augmentations that use saliency maps to mask or focus image regions
- **Real-Time Dashboard** — live monitoring with branch trees, metrics, XAI previews; mobile via QR code
- **Auditable Reports** — structured JSON + static dashboard export for stakeholders

---

### Quick start

```bash
pip install "bnnr[dashboard]"

python3 -m bnnr train --dataset cifar10 --preset light --with-dashboard
```

Interactive wizard:

```bash
python3 -m bnnr quickstart
```

Analyze an existing checkpoint:

```bash
python3 -m bnnr analyze --model checkpoints/best.pt --data cifar10 --output ./analysis_out
```

Python API (advanced):

```python
from bnnr import quick_run, BNNRConfig

result = quick_run(model, train_loader, val_loader, config=BNNRConfig(m_epochs=5, max_iterations=3, device="auto"))
print(result.best_metrics)
```

---

### Repositories

| Repository | Description |
|:-----------|:------------|
| [`bnnr`](https://github.com/bnnr-team/bnnr) | Core library — CLI, training, augmentations, XAI, dashboard |
| [`bnnr-website`](https://github.com/bnnr-team/bnnr-website) | Site at [bnnr.dev](https://www.bnnr.dev) — docs + demo video with audio |

---

### Interactive demos

| Demo | Try it |
|:-----|:------:|
| Classification (STL-10) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/classification/bnnr_classification_demo.ipynb) |
| Multi-Label Classification | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/multilabel/bnnr_multilabel_demo.ipynb) |
| Augmentations Guide | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/bnnr_augmentations_guide.ipynb) |
| Object Detection (YOLO) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/detection/bnnr_detection_demo.ipynb) |
| Bring Your Own Data | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/bnnr_custom_data.ipynb) |

---

### Team

**Mateusz Walo** — Founder & Lead Developer
Architect behind BNNR's core engine, XAI pipeline, and model improvement loop.

**Diana Morzhak** — Software Developer & QA Engineer
Feature development, quality assurance, and end-to-end testing.

**Dominika Zydorczyk** — Community & Communications Specialist
Community outreach, content strategy, and project awareness.

**Zuzanna Saczuk** — Graphic Designer & Brand Lead
Visual identity — logo, neon branding, UI, and assets.

---

<p align="center">
  <a href="https://www.bnnr.dev"><strong>bnnr.dev</strong></a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://pypi.org/project/bnnr/">PyPI</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://github.com/bnnr-team/bnnr">GitHub</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://github.com/bnnr-team/bnnr/discussions">Discussions</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://github.com/bnnr-team/bnnr/issues">Issues</a>
</p>

<p align="center">
  <sub>MIT License &copy; 2025–2026 BNNR Team</sub>
</p>
