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
  Train, explain, improve, and prove PyTorch vision models&nbsp;&mdash;<br/>
  with XAI diagnostics, intelligent augmentation, and a real-time dashboard.
</p>

<p align="center">
  <a href="https://pypi.org/project/bnnr/"><img src="https://img.shields.io/pypi/v/bnnr?color=orange&label=PyPI" alt="PyPI version" /></a>&nbsp;
  <a href="https://pypi.org/project/bnnr/"><img src="https://img.shields.io/pypi/pyversions/bnnr?color=blue" alt="Python versions" /></a>&nbsp;
  <a href="https://github.com/bnnr-team/bnnr/blob/main/LICENSE"><img src="https://img.shields.io/github/license/bnnr-team/bnnr" alt="License" /></a>&nbsp;
  <a href="https://www.bnnr.dev"><img src="https://img.shields.io/badge/docs-bnnr.dev-blue" alt="Docs" /></a>
</p>

---

### How it works

| Step | What happens |
|:----:|:-------------|
| **Train** | Start with your PyTorch model and data. BNNR trains a baseline, then iteratively evaluates candidate augmentations — keeping only those that measurably improve performance. |
| **Explain** | OptiCAM, GradCAM, NMF, and CRAFT saliency maps reveal what the model focuses on. Per-class diagnoses expose blind spots and biases invisible to accuracy alone. |
| **Improve** | Intelligent Coarse Dropout (ICD) masks salient regions, forcing the model to learn from context. Anti-ICD sharpens focus on key features. Both are XAI-driven and automatic. |
| **Prove** | A structured report with metrics, XAI heatmaps, branch decisions, and before/after comparisons — shareable, auditable, and ready for stakeholders. |

---

### Key features

- **Auto-Augment Search** — iterative branching strategy that tests augmentations against a baseline; no manual tuning needed
- **Classification + Detection** — same workflow for both tasks with bbox-aware augmentations that automatically update coordinates
- **XAI Explainability** — OptiCAM, GradCAM, NMF, and CRAFT heatmaps with per-class severity and trend analysis
- **ICD & AICD** — novel XAI-driven augmentations that use saliency maps to intelligently mask or focus image regions
- **8 Novel Augmentations** — texture-rich transforms designed for real-world domains: ChurchNoise, TeaStains, LuxferGlass, ProCAM, DifPresets, Smugs, Drust, and more
- **GPU-Native Speed** — key augmentations run natively on CUDA tensors with optional Kornia integration
- **Real-Time Dashboard** — live monitoring with high-res previews, branch decision trees, per-class metrics, and XAI insights; accessible from your phone via QR code
- **Auditable Reports** — structured JSON reports exportable as static dashboards for regulatory review or stakeholder presentations

---

### Quick start

```bash
pip install "bnnr[dashboard]"
```

```python
from bnnr import quick_run, BNNRConfig

result = quick_run(
    model, train_loader, val_loader,
    config=BNNRConfig(
        m_epochs=5,
        max_iterations=3,
        device="auto",
    ),
)
print(f"Best: {result.best_metrics}")
```

---

### Repositories

| Repository | Description |
|:-----------|:------------|
| [`bnnr`](https://github.com/bnnr-team/bnnr) | Core Python library — training, augmentations, XAI, CLI, and dashboard |
| [`bnnr-website`](https://github.com/bnnr-team/bnnr-website) | Documentation website at [bnnr.dev](https://www.bnnr.dev) |

---

### Interactive demos

| Demo | Try it |
|:-----|:------:|
| Classification (STL-10) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/classification/bnnr_classification_demo.ipynb) |
| Object Detection (VOC) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/detection/bnnr_detection_demo.ipynb) |
| Multi-Label Classification | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/multilabel/bnnr_multilabel_demo.ipynb) |
| Augmentations Guide | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/bnnr_augmentations_guide.ipynb) |
| Bring Your Own Data | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bnnr-team/bnnr/blob/main/examples/bnnr_custom_data.ipynb) |

---

### Team

**Mateusz Walo** — Founder & Lead Developer
Architect behind BNNR's core engine, XAI pipeline, and model improvement loop. Passionate about making neural networks more robust and explainable.

**Diana Morzhak** — Software Developer & QA Engineer
Responsible for feature development, quality assurance, and end-to-end testing — ensuring reliability across classification and detection workflows.

**Dominika Zydorczyk** — Community & Communications Specialist
Drives community outreach, content strategy, and project awareness for BNNR across social channels and developer communities.

**Zuzanna Saczuk** — Graphic Designer & Brand Lead
Creator of BNNR's visual identity — from the molecular logo and neon branding to UI design and all visual assets.

---

<p align="center">
  <a href="https://www.bnnr.dev"><strong>bnnr.dev</strong></a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://pypi.org/project/bnnr/">PyPI</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://github.com/bnnr-team/bnnr">GitHub</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
  <a href="https://github.com/bnnr-team/bnnr/issues">Issues</a>
</p>

<p align="center">
  <sub>MIT License &copy; 2025 BNNR Team</sub>
</p>
