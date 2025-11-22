# MNIST Curation Lab – Curated MNIST with IDK Class

This repository contains my submission for **Dataset Curation Lab 1 – MNIST** for the *Applied Hands-On Computer Vision* course.

## 🔍 Overview

In this project I:

- Loaded the MNIST dataset using FiftyOne and PyTorch
- Extracted embeddings using a Modern LeNet-5 CNN
- Visualized the embedding space with **PCA** and **UMAP** in FiftyOne
- Computed a **hardness** score per sample and selected the top 2% most difficult digits
- Relabeled those hard samples as an **IDK (I Don’t Know)** class
- Tagged them as `questionable` in FiftyOne for visual inspection
- Trained an **11-class classifier** (digits 0–9 + IDK)
- Evaluated the model and compared performance on regular vs IDK digits

## 📓 Notebook

The full workflow is implemented in:

- `Lab_Assignment_1_MNISTCuration.ipynb`

You can open it directly in GitHub or run it in Google Colab.

## 📚 Curated Dataset on HuggingFace

The curated version of MNIST (0–9 + IDK) is published as a HuggingFace dataset:

👉 https://huggingface.co/datasets/MJ3099/mnist-curated-idk

The dataset is in `ImageClassificationDirectoryTree` format, with one folder per class:
`0 - zero`, `1 - one`, ..., `9 - nine`, `10 - IDK`.

## 🛠 Dependencies (high level)

- Python 3.10+
- PyTorch
- torchvision
- fiftyone
- umap-learn
- scikit-learn
- huggingface_hub

All necessary installations are included at the top of the notebook.

## 🧪 Reproducing the Results

1. Open the notebook in Google Colab.
2. Run the installation cell (pip installs).
3. Run all cells to:
   - compute embeddings
   - visualize PCA/UMAP
   - curate questionable digits
   - train and evaluate the 11-class classifier
4. Optionally, export and upload the curated dataset to your own HuggingFace account.
