# 🌿 Crop Disease Detection Using Transfer Learning

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange?logo=pytorch)](https://pytorch.org)
[![Google Colab](https://img.shields.io/badge/Run%20on-Google%20Colab-yellow?logo=googlecolab)](https://colab.research.google.com)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![University](https://img.shields.io/badge/LJMU-MSc%20AI%20%26%20ML-red)](https://ljmu.ac.uk)

> **MSc Artificial Intelligence & Machine Learning Thesis**
> Liverpool John Moores University (LJMU) / UpGrad
> Student: Chiranth | ID: PN1196996

---

## 📋 Overview

This research investigates the effectiveness of **Transfer Learning-based CNN architectures** for automated multi-class crop disease classification using the **PlantVillage dataset**.

### 🔬 Research Question
> *Which CNN architecture — ResNet50, VGG16, or DenseNet121 — performs best for classifying crop diseases under transfer learning, and how do data augmentation strategies affect model generalisation?*

### 🌍 Real-World Impact
- India loses over **₹50,000 crore annually** due to crop diseases
- **86% of Indian farm holdings** are smallholder farmers with limited resources
- A mobile app using this trained model could provide **instant, free disease diagnosis** to any farmer with a smartphone

---

## 🗂️ Dataset

| Property | Details |
|---|---|
| **Name** | PlantVillage Dataset |
| **Images** | 54,305 labeled leaf images |
| **Classes** | 38 disease classes |
| **Crops** | 14 crop species |
| **Source** | [Kaggle — abdallahalidev/plantvillage-dataset](https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset) |

---

## 🤖 Models Compared

| Model | Parameters | Key Feature |
|---|---|---|
| **ResNet50** | 25M | Skip connections — prevents vanishing gradient |
| **VGG16** | 138M | Simple uniform architecture — interpretable |
| **DenseNet121** | 8M | Dense connections — efficient feature reuse |

All models are pre-trained on **ImageNet** and fine-tuned on the PlantVillage dataset using full fine-tuning strategy.

---

## ⚙️ Methodology

### Data Split
- **Training:** 70% (~37,800 images)
- **Validation:** 15% (~8,100 images)
- **Test:** 15% (~8,100 images)

### Data Augmentation (Training Only)
- Random horizontal and vertical flipping
- Random rotation (±30°)
- Colour jitter (brightness, contrast, saturation)
- Random resized crop (scale 0.85–1.0)
- Normalisation using ImageNet mean and std

### Training Configuration
| Parameter | Value |
|---|---|
| Optimizer | Adam (β1=0.9, β2=0.999) |
| Learning Rate | 0.0001 |
| Batch Size | 32 |
| Max Epochs | 15 |
| Early Stopping | Patience = 5 |
| LR Scheduler | ReduceLROnPlateau (patience=3, factor=0.5) |
| Regularisation | Dropout (0.5) + L2 Weight Decay (1e-4) |

---

## 📊 Results

> Results will be updated after experiments are complete.

| Model | Accuracy (%) | Precision (%) | Recall (%) | F1 Score (%) |
|---|---|---|---|---|
| ResNet50 | — | — | — | — |
| VGG16 | — | — | — | — |
| DenseNet121 | — | — | — | — |

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com)
2. Upload `Crop_Disease_Detection_Colab.ipynb`
3. Set Runtime → Change Runtime Type → **T4 GPU**
4. Run all cells from top to bottom
5. Upload your `kaggle.json` when prompted in Cell 2

### Option 2 — Local Setup
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/crop-disease-detection-msc.git
cd crop-disease-detection-msc

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

---

## 📁 Repository Structure

```
crop-disease-detection-msc/
│
├── Crop_Disease_Detection_Colab.ipynb   # Main experiment notebook
├── requirements.txt                      # Python dependencies
├── README.md                             # This file
│
├── results/
│   ├── results_table.csv                 # Model performance metrics
│   ├── training_curves.png               # Accuracy & loss curves
│   ├── model_comparison.png              # Side-by-side comparison chart
│   └── confusion_matrix.png              # Confusion matrix heatmap
│
├── docs/
│   └── Research_Guide.docx               # Complete project reference guide
│
└── references/
    └── papers.md                          # All 6 research papers with links
```

---

## 📚 References

| # | Paper | Link |
|---|---|---|
| 1 | Deep Learning-Based Leaf Disease Detection | [MDPI](https://www.mdpi.com/2073-4395/12/10/2395) |
| 2 | Transfer Learning for Multi-Crop Disease | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2589721721000416) |
| 3 | Comprehensive Review of Crop Disease Detection | [Springer](https://link.springer.com/article/10.1007/s10661-024-12454-z) |
| 4 | Federated Learning for Crop Disease | [Nature](https://www.nature.com/articles/s41598-023-46218-5) |
| 5 | Depthwise CNN with Attention Modules | [Frontiers](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2024.1505857/full) |
| 6 | Lightweight Model for Plant Diseases | [Frontiers](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2023.1227011/full) |

---

## 👤 Author

**Chiranth**
- Student ID: PN1196996
- Course: MSc Artificial Intelligence & Machine Learning
- University: Liverpool John Moores University (LJMU) / UpGrad
- Supervisor: Bharti Bisht

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
