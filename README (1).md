# Lung Cancer Detection using VGG19

Deep learning project for lung cancer classification using VGG19
as a feature extractor combined with traditional ML classifiers.

## Problem Statement

Lung cancer is one of the leading causes of cancer-related deaths globally.
Early and accurate detection is critical for improving survival rates.
This project uses transfer learning with VGG19 to extract features from
CT scan images and classifies them using SVM and Random Forest.

## Dataset

IQ-OTH/NCCD Lung Cancer Dataset
- 613 training images
- 72 validation images
- 315 test images
- 4 classes: Adenocarcinoma, Large Cell Carcinoma, Normal, Squamous Cell Carcinoma

## Methodology

    CT Scan Images
          Down
    VGG19 Feature Extraction (512 features)
          Down
    Traditional ML Classifiers
       SVM        Random Forest

## Results

| Model                 | Accuracy | Precision | Recall | F1 Score |
|-----------------------|----------|-----------|--------|----------|
| VGG19 + SVM           | 81.27%   | 81.98%    | 81.27% | 81.24%   |
| VGG19 + Random Forest | 72.70%   | 73.16%    | 72.70% | 72.54%   |

VGG19 + SVM outperforms Random Forest by 8.57% in accuracy.

## Key Findings

- Normal class achieved near perfect classification (99% F1) with SVM
- SVM consistently outperforms Random Forest across all metrics
- VGG19 ImageNet features transfer well to medical imaging
- Adenocarcinoma was the most challenging class to classify

## Prediction Output

The model takes a single CT scan image as input and outputs:
- Predicted cancer type
- Confidence score for each class
- Visual probability bar chart
- Diagnosis recommendation

## Tech Stack

- Python 3.12
- TensorFlow / Keras — VGG19 feature extraction
- Scikit-learn — SVM and Random Forest classifiers
- Matplotlib / Seaborn — visualizations
- Google Colab — development environment

## Setup

Install dependencies:
    pip install tensorflow scikit-learn numpy matplotlib seaborn

## Usage

1. Upload dataset to Google Drive
2. Open lung_cancer_detection.ipynb in Google Colab
3. Mount Google Drive and update dataset path
4. Run all cells
5. Upload a CT scan image when prompted for prediction

## Project Structure

    lung-cancer-detection-vgg19/
    ├── lung_cancer_detection.ipynb
    ├── results.json
    ├── confusion_matrices.png
    ├── model_comparison.png
    └── README.md

## Author

Harsha — Masters in Computer Science
github.com/Harsha123v
