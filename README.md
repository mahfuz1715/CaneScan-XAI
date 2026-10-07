# CaneScan-XAI

### Explainable Ensemble Deep Learning for Sugarcane Leaf Disease Classification

CaneScan-XAI is an explainable deep learning framework for automated sugarcane leaf disease classification. The study combines transfer learning, attention mechanisms, weighted ensemble learning, Grad-CAM visual explanations, and a lightweight Streamlit prototype to support accurate and interpretable disease recognition.

The work was **accepted and presented at the 5th IEEE International Conference on Robotics, Automation, Artificial-Intelligence and Internet-of-Things (RAAICON 2026)**.

---

## Overview

The project investigates how pretrained CNN models can be improved through attention and ensemble learning while keeping the final predictions interpretable.

The full workflow includes:
- evaluation of pretrained CNN backbones,
- SE and CBAM attention mechanisms,
- weighted soft-voting ensembles,
- Grad-CAM-based explainability,
- and a Streamlit-based research prototype.

The experiments were conducted on a merged sugarcane leaf dataset containing **9,269 images across 14 classes**.

---

## Research Highlights

- **14-class** sugarcane leaf disease classification
- **9,269** total images from two public datasets
- Baseline models: Xception, InceptionV3, DenseNet201
- Attention-enhanced models using SE and CBAM
- Weighted soft-voting ensemble
- Grad-CAM visual explanations
- Streamlit research prototype
- Best ensemble accuracy: **97.20%**

---

## Model Performance

### Baseline Models

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Xception | 94.72% | 0.9489 | 0.9472 | 0.9464 |
| InceptionV3 | 90.62% | 0.9198 | 0.9062 | 0.9095 |
| DenseNet201 | 90.19% | 0.9201 | 0.9019 | 0.9029 |

### Attention and Ensemble Results

| Configuration | Accuracy |
|---|---:|
| Xception + SE | 95.04% |
| Xception + CBAM | 94.50% |
| InceptionV3 + SE | 94.07% |
| InceptionV3 + CBAM | 95.15% |
| Baseline Ensemble | 97.09% |
| SE-based Ensemble | 96.34% |
| **CBAM-based Ensemble** | **97.20%** |

The final CaneScan-XAI ensemble achieved:

- **Accuracy:** 97.20%
- **Precision:** 97.37%
- **Recall:** 97.20%
- **F1-score:** 97.22%

---

## Methodology

1. Merge and preprocess the two public sugarcane leaf datasets.
2. Resize images to 224 × 224 pixels.
3. Train Xception, InceptionV3, and DenseNet201 as baseline models.
4. Select the stronger backbones for attention-based experiments.
5. Apply SE and CBAM attention modules.
6. Combine model predictions using weighted soft voting.
7. Use Grad-CAM to visualize regions that influence predictions.
8. Demonstrate the final framework through a lightweight Streamlit application.

---

## Dataset

The final dataset contains **9,269 images** distributed across **14 classes**:

`Banded Chlorosis` · `Brown Spot` · `Brown Rust` · `Dried Leaves` · `Grassy Shoot` · `Healthy Leaves` · `Mosaic` · `Pokkah Boeng` · `Red Rot` · `Rust` · `Sett Rot` · `Smut` · `Viral Disease` · `Yellow Leaf`

The dataset was divided into training, validation, and testing sets using a **70:20:10** split.

> The datasets are not redistributed in this repository. Please refer to the original data sources cited in the paper.

---

## Explainability

Grad-CAM is used to highlight the image regions that contribute most strongly to each prediction.

This adds an interpretability layer to the classification pipeline and helps examine whether the model is focusing on disease-relevant regions rather than relying only on the predicted class label.

---

## Streamlit Prototype

A lightweight Streamlit application was developed to demonstrate the final CaneScan-XAI framework.

The prototype allows a user to:
- upload a sugarcane leaf image,
- receive a predicted disease class,
- view confidence information,
- and inspect a Grad-CAM visualization.

The application is intended for **research and demonstration purposes**.

---

## Repository Structure

```text
CaneScan-XAI/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── baseline experiments
│   ├── attention experiments
│   └── ensemble experiments
├── app/
│   └── Streamlit prototype
└── paper/
    └── README.md
```

The repository is being organized to keep research notebooks, application code, and paper information separate and easy to navigate.

---

## Paper

**Title:**  
*CaneScan-XAI: An Explainable Ensemble Deep Learning Framework for Automated Sugarcane Leaf Disease Classification*

**Conference:**  
5th IEEE International Conference on Robotics, Automation, Artificial-Intelligence and Internet-of-Things (**RAAICON 2026**)

**Status:**  
Accepted and presented.

### Authors

- **Mahfuz Uddin Ahmed**
- Shawna Akter
- Rafid Bin Taher
- Moin Uddin Ahmed

The publisher-formatted paper is not redistributed in this repository. An official DOI or IEEE Xplore link can be added once the final bibliographic record is available.

---

## Citation

Official citation details will be updated when the final bibliographic record is available.

```bibtex
@inproceedings{canescanxai2026,
  title  = {CaneScan-XAI: An Explainable Ensemble Deep Learning Framework for Automated Sugarcane Leaf Disease Classification},
  author = {Ahmed, Mahfuz Uddin and Akter, Shawna and Taher, Rafid Bin and Ahmed, Moin Uddin},
  booktitle = {5th IEEE International Conference on Robotics, Automation, Artificial-Intelligence and Internet-of-Things (RAAICON 2026)},
  year   = {2026}
}
```

---

## Research Scope

CaneScan-XAI is intended as a research framework for explainable plant-disease classification. The current study uses publicly available datasets, so broader field validation under varying lighting, backgrounds, camera conditions, and real-world agricultural environments remains an important direction for future work.
