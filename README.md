# Lung and Colon Cancer Detection from Histopathology Images

Deep learning pipeline for classifying lung and colon cancer tissue in histopathology images, built for my undergraduate senior design project.

## Overview

- **Classification:** transfer learning with an ImageNet-pretrained **ResNet50** on the [LC25000](https://arxiv.org/abs/1912.12142) dataset (lung and colon tissue, 5 classes).
- **Whole-slide images:** patch extraction from whole-slide images (WSI) and random batch selection for training.
- **Segmentation:** a **U-Net** (128×128 patches) trained on generated tissue masks.

## Repository Structure

| Path | Contents |
|------|----------|
| `LC25000_ResNet50.ipynb` | ResNet50 transfer-learning classifier on LC25000 |
| `CODE/Transfer_learning_to_detect_lung_cancer.ipynb` | Transfer-learning experiments |
| `CODE/UNET_128_CH_01.ipynb`, `CODE/sm_patch_train.py` | U-Net patch segmentation |
| `CODE/WSI_*.ipynb`, `CODE/LCDC_*.ipynb`, `CODE/Mask_CP.ipynb` | Whole-slide patching and mask generation |
| `Model Summary.txt` | Network architecture summary |
| `Proposal/`, `Presentation`, `SDP method.png` | Project proposal, slides, and method diagram |

## Getting Started

Open the notebooks in Jupyter or Google Colab. Training uses TensorFlow/Keras and downloads datasets through the Kaggle API, so add your own Kaggle credentials locally (never commit them).
