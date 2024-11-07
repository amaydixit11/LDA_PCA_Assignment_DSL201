# DSL201 - Assignment 3 - Linear Discriminant Analysis (LDA) and Principal Component Analysis (PCA)

This repository contains the implementation and analysis of Linear Discriminant Analysis (LDA) and Principal Component Analysis (PCA) as part of Assignment 3 for DSL201.

## Overview

This assignment covers the following:

1. **LDA for Classification**: Using the MNIST dataset to implement a one-vs-rest classification with Linear Discriminant Analysis and comparing the performance of a k-Nearest Neighbors (k-NN) classifier before and after LDA transformation.
2. **PCA for Dimensionality Reduction**: Applying PCA (Karhunen-Loève Transform) to reconstruct face images from the faces94 dataset, illustrating the impact of varying the number of principal components on image quality.

## Contents

- **LDA Analysis**: Implementing LDA for dimensionality reduction and k-NN accuracy comparison on MNIST data.
- **PCA Analysis**: Using PCA to compress and reconstruct face images, visualizing reconstructed images with different numbers of principal components.

## LDA Experimentation

- **Dataset**: A subset of the MNIST dataset containing digits 0-4.
- **Preprocessing**: Images are flattened and normalized.
- **LDA Transformation**: One-vs-Rest LDA is applied to enhance class separability.
- **k-NN Comparison**:
  - Baseline k-NN accuracy: `99.02%`
  - Accuracy after LDA: `96.11%`

#### Key Findings

LDA enhanced class separability for certain digits (e.g., 0 and 2), but k-NN performance did not improve after applying LDA, possibly due to the complexity of MNIST data and limitations of LDA for non-linear patterns.

## PCA Experimentation

- **Dataset**: Faces from the faces94 dataset.
- **Preprocessing**: Images converted to grayscale, resized to 100x100 pixels, and flattened.
- **Reconstruction Quality**: Images reconstructed using 5, 10, 25, 40, and 50 principal components.

#### Reconstruction Observations

| Components | Image Quality                      |
| ---------- | ---------------------------------- |
| 5          | Basic structure, lacks detail      |
| 10         | Moderate; faint facial features    |
| 25         | Recognizable face with fair detail |
| 40         | High; clear facial features        |
| 50         | Near-original fidelity             |

## Conclusion

1. **LDA**: Effective for visualizing class separability but may not always improve classifier performance on complex datasets.
2. **PCA**: Provides significant compression potential while preserving key image features, making it ideal for storage and computational efficiency.

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Run the Jupyter notebooks to execute the experiments for both LDA and PCA.

## Requirements

- Python 3.x
- Required libraries: `scikit-learn`, `matplotlib`, `numpy`, `cv2`
