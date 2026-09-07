# Emotion Recognition Using CNN, ResNet-50, and EfficientNet

A facial emotion recognition project comparing a custom CNN against two transfer-learning architectures (ResNet-50 and EfficientNet-B0) across six emotion classes.

## Overview

This project classifies facial images into six emotion categories — **angry, fear, happy, neutral, sad, surprise** — using three different deep learning approaches, and compares their performance and generalization behavior.

## Models

| Model | Architecture Summary | Notebook |
|---|---|---|
| Custom CNN | Three convolutional layers with batch normalization, dropout, and global average pooling, trained from scratch | [Open in Colab](https://colab.research.google.com/drive/1NY2xdXEtihgir-ZmNzsdtVc8bnI4hFKA?usp=sharing) |
| ResNet-50 | Deep residual network, pretrained on ImageNet, fine-tuned with a modified final layer | [Open in Colab](https://colab.research.google.com/drive/1pZfyAu1v6q19xBMIbtJdyYY0RsZJHd9A?usp=sharing) |
| EfficientNet-B0 | Compound-scaled CNN balancing depth, width, and resolution, pretrained and fine-tuned | [Open in Colab](https://colab.research.google.com/drive/1reIyxegzXJX6IfixgqpxsGCPGsG-cj9Q?usp=sharing) |

> Note: These notebooks are hosted on Google Colab. Make sure sharing/view access is enabled if you'd like others to open them. Local copies are also included under [`notebooks/`](./notebooks).

## Libraries & Tools

- **PyTorch / torchvision** — model definition, training, and transfer learning
- **PyTorch ImageFolder** — dataset loading and class structuring
- Standard augmentation pipeline (resize, random rotation, flips, color jitter) and normalization

## Dataset

Images are organized into train / validation / test splits, each divided into six class folders (`angry`, `fear`, `happy`, `neutral`, `sad`, `surprise`), with a roughly balanced class distribution.

## Results

| Model | Train Accuracy | Validation Accuracy | Test Accuracy |
|---|---|---|---|
| ResNet-50 | 95.2% | 55.2% | 55.2% |
| Custom CNN | 63.75% | 38.13% | 38.53% |
| EfficientNet-B0 | 62.75% | 36.0% | 35.07% |

Evaluation includes accuracy curves, confusion matrices, and precision/recall/F1 per class for each model.

## Challenges & Approach

- **Imbalanced/limited data** — addressed with data augmentation
- **Overfitting** — addressed with dropout and regularization
- **Hyperparameter tuning** — addressed via grid search over learning rate and batch size

## Report & Presentation

- Full write-up: [`deeplearningL2.docx`](./deeplearningL2.docx)
- Presentation slides: [`deep_prog.pptx`](./deep_prog.pptx)

## Repository structure

```
.
├── notebooks/
│   ├── resnet50.ipynb
│   ├── custom_cnn.ipynb
│   └── efficientnet.ipynb
├── deeplearningL2.docx
├── deep_prog.pptx
└── README.md
```

## Getting started

1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Open any notebook in `notebooks/` locally (Jupyter) or in Colab, point the dataset path to a facial-emotion image dataset organized into the six class folders, and run.

## Team

- Areen AlAkaleek
- Lujain Yahya
- Huda Shqerat
