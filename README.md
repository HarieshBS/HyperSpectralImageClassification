# HyperSpectralImageClassification
# Hyperspectral Image Classification

A complete machine learning pipeline for hyperspectral image (HSI) classification using classical machine learning models, dimensionality reduction, spectral visualization, and dataset benchmarking.

This project is implemented as a Jupyter/Google Colab notebook and supports multiple benchmark hyperspectral datasets including Indian Pines, Pavia University, and Salinas.

---

# Project Overview

Hyperspectral imaging captures information across hundreds of spectral bands instead of standard RGB channels. This enables fine-grained material identification and classification in domains such as:

* Remote sensing
* Agriculture
* Environmental monitoring
* Mineral exploration
* Defense and surveillance
* Medical imaging

This notebook performs:

* Dataset downloading and loading
* Preprocessing and normalization
* Spectral visualization
* Dimensionality reduction using PCA
* 2D embedding visualization using UMAP
* Training multiple machine learning classifiers
* Accuracy benchmarking
* Confusion matrix generation
* Full-scene prediction map creation

---

# Features

## Dataset Support

Supported benchmark datasets:

* Indian Pines
* Pavia University (PaviaU)
* Salinas

Datasets are automatically downloaded from public mirrors.

---

## Preprocessing Pipeline

The notebook includes:

* Flattening hyperspectral cubes
* Label masking
* Feature standardization
* Optional bilateral filtering
* PCA dimensionality reduction

---

## Visualization

Includes rich visual outputs such as:

* False-color hyperspectral composites
* Spectral signature plots
* PCA explained variance plots
* UMAP embeddings
* Accuracy comparison charts
* Confusion matrices
* Prediction maps
* Error maps

---

## Machine Learning Models

The following models are trained and evaluated:

| Model               | Description                            |
| ------------------- | -------------------------------------- |
| Random Forest       | Ensemble tree-based classifier         |
| SVM                 | Support Vector Machine with RBF kernel |
| Logistic Regression | Linear probabilistic classifier        |
| KNN                 | K-Nearest Neighbors classifier         |
| XGBoost             | Gradient boosting classifier           |

---

# Technologies Used

## Core Libraries

* NumPy
* SciPy
* Matplotlib
* scikit-learn
* XGBoost
* UMAP-learn
* OpenCV
* Joblib

---

# Installation

## Clone Repository

```bash
git clone <repository-url>
cd hyperspectral-image-classification
```

---

## Install Dependencies

```bash
pip install numpy scipy matplotlib scikit-learn xgboost spectral umap-learn opencv-python-headless wget joblib
```

---

# Running the Notebook

Open the notebook:

```bash
jupyter notebook hyperspectral_image_classification.ipynb
```

Or upload directly into:

* Google Colab
* JupyterLab
* VS Code Jupyter Extension

---

# Workflow

## 1. Dataset Selection

Select the dataset inside the notebook:

```python
dataset_choice = "indian_pines"
```

Available options:

```python
"indian_pines"
"paviaU"
"salinas"
```

---

## 2. Dataset Download

The notebook automatically downloads:

* Hyperspectral cube (.mat)
* Ground truth labels

from multiple mirror sources.

---

## 3. Data Loading

The notebook:

* Loads MATLAB `.mat` files
* Extracts H × W × B hyperspectral tensors
* Extracts ground-truth labels

Where:

* H = height
* W = width
* B = spectral bands

---

## 4. Preprocessing

The preprocessing stage performs:

* Flattening pixel vectors
* Removing unlabeled pixels
* Standard scaling
* Optional bilateral filtering
* PCA transformation

---

## 5. Spectral Visualization

The notebook visualizes:

* False-color RGB composites
* Spectral signatures of different classes
* PCA variance distribution
* UMAP projections

---

## 6. Model Training

Data is split using stratified train/test splitting.

Each model is:

* Trained
* Evaluated
* Timed
* Compared using accuracy metrics

---

## 7. Evaluation

Generated evaluation outputs:

* Test accuracy
* Classification report
* Confusion matrix
* Model comparison graph

---

## 8. Prediction Mapping

The best-performing classifier is used to:

* Predict all image pixels
* Generate a full-scene classification map
* Visualize prediction errors

---

# Example Outputs

## False Color Composite

Visual representation of selected spectral bands.

## Spectral Signatures

Plots showing spectral reflectance patterns for different classes.

## PCA Variance Plot

Explained variance retained across principal components.

## UMAP Projection

2D visualization of high-dimensional spectral data.

## Classification Map

Pixel-wise predicted land-cover classes.

---

# File Structure

```text
.
├── hyperspectral_image_classification.ipynb
├── datasets/
│   ├── IndianPines/
│   ├── PaviaU/
│   └── Salinas/
└── README.md
```

---

# Performance Notes

* PCA significantly reduces computation cost.
* UMAP computation may take longer on large datasets.
* XGBoost and SVM generally provide high classification accuracy.
* Bilateral filtering improves smoothness but increases preprocessing time.

---

# Future Improvements

Potential enhancements include:

* Deep learning architectures (CNN, 3D CNN, HybridSN)
* Transformer-based hyperspectral models
* Spatial-spectral feature fusion
* Hyperparameter optimization
* Real-time inference
* Model export and deployment
* Attention mechanisms
* Semi-supervised learning

---

# Applications

This project can be extended for:

* Crop monitoring
* Forest classification
* Urban mapping
* Water quality analysis
* Geological surveys
* Precision agriculture
* Environmental change detection

---

# Authors

* Gaurav Gali
* BS Hariesh

---

# License

This project is intended for academic and research purposes.

---

# Acknowledgements

Public benchmark datasets sourced from:

* University of the Basque Country (UPV/EHU)
* Figshare dataset mirrors

---

# References

## Datasets

* Indian Pines Dataset
* Pavia University Dataset
* Salinas Dataset

## Libraries

* scikit-learn
* XGBoost
* UMAP-learn
* OpenCV

---

# Quick Start

```bash
pip install numpy scipy matplotlib scikit-learn xgboost spectral umap-learn opencv-python-headless wget joblib
```

```bash
jupyter notebook hyperspectral_image_classification.ipynb
```

Select dataset:

```python
dataset_choice = "indian_pines"
```

Run all notebook cells.
